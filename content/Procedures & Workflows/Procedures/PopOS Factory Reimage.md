---
tags:
---

---

Below I’ll give you a reliable, repeatable way to leave the machine in a _true_ out-of-box state for the next owner (so they get the user-creation flow). There are two safe methods: **(A) do it from a Live USB / recovery environment (cleanest)** or **(B) do it from the installed system by creating a second temporary admin account**. Pick one — both end with the same result: **no human accounts remaining**, so GNOME’s initial/OOBE runs on first boot. References about GNOME Initial Setup and the Pop!_OS recovery flow are at the end. ([ArchWiki](https://wiki.archlinux.org/title/GNOME_Initial_Setup?utm_source=chatgpt.com "GNOME Initial Setup - ArchWiki"))

---

# Quick summary (TL;DR)

1. Install Pop!_OS and create a temporary account (installer requires it). ([support.system76.com](https://support.system76.com/articles/install-pop/?utm_source=chatgpt.com "Installing Pop!_OS - System76 Support"))
    
2. Remove that temp account **and** any AccountsService records so the system has _no_ human users (UID ≥1000). That causes GNOME Initial Setup to run at next boot. ([ArchWiki](https://wiki.archlinux.org/title/GNOME_Initial_Setup?utm_source=chatgpt.com "GNOME Initial Setup - ArchWiki"))
    
3. Verify `gnome-initial-setup` is present / enabled (it normally is). Boot to confirm OOBE.
    

---

# Full step-by-step — METHOD A (recommended: Live USB / recovery)

This is the cleanest because you’re not logged in as a user while deleting them.

1. Make a Pop!_OS installer USB (or use the system’s Recovery partition). Boot the machine from the USB and choose **Try Demo Mode** (don’t install). System76 docs on recovery are useful if you prefer that route. ([support.system76.com](https://support.system76.com/articles/pop-recovery/?utm_source=chatgpt.com "Recovery Partition - System76 Support"))
    
2. Open a terminal in the live session and find the installed root partition:
    

```bash
lsblk -f
# note the partition that contains the Pop!_OS root (e.g. /dev/nvme0n1p2 or /dev/sda2)
```

3. Mount and chroot into the installed system (replace `/dev/nvme0n1p2` with the correct device):
    

```bash
sudo mkdir /mnt/inst
sudo mount /dev/nvme0n1p2 /mnt/inst
for d in dev proc sys run; do sudo mount --bind /$d /mnt/inst/$d; done
sudo chroot /mnt/inst /bin/bash
```

4. Inside the chroot: list “human” users (UID ≥ 1000):
    

```bash
awk -F: '$3 >= 1000 && $1 != "nobody" {print $1, $3}' /etc/passwd
```

You should see the temp username you created during install.

5. Remove the temp user(s) and their home (example username `seller`):
    

```bash
# remove user and home
userdel -r seller   # (or: deluser --remove-home seller)
# remove lingering AccountsService entry (makes GDM forget the user)
rm -f /var/lib/AccountsService/users/seller
```

(If you removed more than one temp user, repeat for each.)

6. Verify no human users remain:
    

```bash
awk -F: '$3 >= 1000 {print $1, $3}' /etc/passwd || echo "no human users found"
```

7. Make sure `gnome-initial-setup` is installed (it usually is on Pop!_OS):
    

```bash
apt update
apt policy gnome-initial-setup
# install if missing:
apt install -y gnome-initial-setup
```

8. Exit chroot, unmount, reboot:
    

```bash
exit
for d in run sys proc dev; do sudo umount /mnt/inst/$d; done
sudo umount /mnt/inst
reboot
```

On next boot the GNOME out-of-box flow (language, timezone, user creation, etc.) should run for the buyer, just like a new machine. ([ArchWiki](https://wiki.archlinux.org/title/GNOME_Initial_Setup?utm_source=chatgpt.com "GNOME Initial Setup - ArchWiki"))

---

# Full step-by-step — METHOD B (if you prefer to operate from the installed system)

Use this if you don’t want to use a Live USB:

1. After install (you’ve created `seller`), create a second temporary admin user:
    

```bash
sudo adduser cleanup
sudo usermod -aG sudo cleanup
# set a password for cleanup when prompted
```

2. Log out and log in as `cleanup`.
    
3. Delete the original temp user and its AccountsService record:
    

```bash
sudo userdel -r seller
sudo rm -f /var/lib/AccountsService/users/seller
```

4. Verify there are no UID≥1000 users:
    

```bash
awk -F: '$3 >= 1000 {print $1, $3}' /etc/passwd
```

Only `cleanup` (and perhaps other service accounts) should show. Then remove `cleanup` the same way:

```bash
sudo userdel -r cleanup
sudo rm -f /var/lib/AccountsService/users/cleanup
```

5. Ensure `gnome-initial-setup` is installed (see Method A step 7), then reboot. GNOME OOBE should run for the next boot.
    

---

# Extra cleanups (optional, for a more “factory” feel)

- Remove leftover logs and package cache:
    
    ```bash
    sudo apt clean
    sudo rm -rf /var/log/*      # careful: removes logs
    ```
    
- Remove SSH host keys if you want them regenerated (buyers usually don’t care):
    
    ```bash
    sudo rm -f /etc/ssh/ssh_host_*
    ```
    
    they will be re-generated on next boot by `sshd` (or manually via `dpkg-reconfigure openssh-server`).
    
- If you want the machine-id regenerated:
    
    ```bash
    sudo rm -f /etc/machine-id
    sudo systemd-machine-id-setup
    ```
    
    (Not required for resale, but sometimes done by OEMs.)
    

**Warning:** _double-check device names (`/dev/…`) before running destructive commands (`rm -rf`, `userdel -r`). Those commands permanently delete data._

---

# Troubleshooting notes / gotchas

- GNOME initial setup runs when _no human users_ exist (GDM detects absence of user accounts). If it doesn’t trigger, check `/var/lib/AccountsService/users/` and remove any stray files there. ([ArchWiki](https://wiki.archlinux.org/title/GNOME_Initial_Setup?utm_source=chatgpt.com "GNOME Initial Setup - ArchWiki"))
    
- There are a few reported Pop!_OS / GNOME bugs where initial-setup behaves oddly (shows up even when users exist, or gets stuck). If you hit that, regenerating/removing AccountsService files and ensuring `gnome-initial-setup` is installed/unenabled tweaks it. See upstream/GitHub discussion. ([GitHub](https://github.com/pop-os/pop/issues/2878?utm_source=chatgpt.com "Pop! OS New user prompt is launched on startup or reboot #2878"))
    

---

# References / reading

- Pop!_OS installation / recovery docs (how to use the recovery partition or create installer USB). ([support.system76.com](https://support.system76.com/articles/install-pop/?utm_source=chatgpt.com "Installing Pop!_OS - System76 Support"))
    
- GNOME Initial Setup (runs when there are no existing users; vendor customization options). ([ArchWiki](https://wiki.archlinux.org/title/GNOME_Initial_Setup?utm_source=chatgpt.com "GNOME Initial Setup - ArchWiki"))
    
- AccountsService (stores per-machine user data under `/var/lib/AccountsService/users/`). Removing that file helps GDM/initial-setup behave as expected. ([help.gnome.org](https://help.gnome.org/admin/system-admin-guide/stable/session-user.html.en?utm_source=chatgpt.com "Configure a user default session"))
    

---


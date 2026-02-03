---
tags:
---

---

## **Technician Workflow (Simple + Reliable)**

1. **Install a clean Windows 11 Pro** (from official Microsoft media)
    
    - Boot from USB.
        
    - When setup asks for OOBE (user creation), press **`Ctrl` + `Shift` + `F3`** → system will reboot straight into **Audit Mode** as the built-in Administrator.
        
2. **In Audit Mode:**
    
    - **Connect to the internet.**
        
    - Run **Windows Update** until _all_ updates are installed (this pulls drivers automatically from Microsoft’s catalog and Lenovo’s Windows Update channel).
        
    - Reboot and re-check Windows Update and Lenovo Vantage until no new updates appear.
        
    
	    ⚠️ Important: **Do not manually download or install drivers** unless absolutely required
    
3. **Light Customization (Optional, but safe):**
    
    - Set wallpaper, taskbar layout, power settings, etc.
        
    - **Do not** remove any built-in Windows apps (Calculator, Mail, Xbox, etc.) — let the consumer decide.
        
    - Do not install third-party software (AV, management agents, etc.) — they can break Sysprep.
        
4. **Generalize the Image:**
    
    - Open `C:\Windows\System32\Sysprep\Sysprep.exe`.
        
    - Choose:
        
        - **Enter System Out-of-Box Experience (OOBE)**
            
        - **Generalize** (checked)
            
        - **Shutdown**
            
    - Click OK. The PC shuts down, leaving a clean, generalized image ready to capture.
        
5. **Capture & Deploy:**
    
    - Boot into your deployment infrastructure (MDT/WDS/PXE/Clonezilla/etc.).
        
    - Capture the image.
        
    - Deploy to other Laptops
        
6. **When consumer powers on:**
    
    - They’ll get **the full OOBE** (choose region, account, etc.)
        
    - Windows will keep **all its default apps** for Windows 11 (Mail, Calendar, Xbox, etc.).

---

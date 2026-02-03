#Imaging #Customization

---

### ✅ Step-by-Step: Enable Dark Mode (if `Personalize` key is missing)

#### 📍 1. Navigate to the key:
```
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes`
```

#### 📍 2. Right-click on `Themes` ➜ select **New** ➜ **Key** ➜ name it:
```
`Personalize`
```
#### 📍 3. Inside the new `Personalize` key:

- Right-click in the right pane ➜ **New ➜ DWORD (32-bit) Value**
	    
    - Name it: `SystemUsesLightTheme` ➜ set the value to `0`
        
- Again, create:
	    
    - `AppsUseLightTheme` ➜ set the value to `0`
        
---

### 💡 Repeat the Same for Default User Profile

To make this apply to **all new user accounts**, also create the same keys and values under:

```
`HKEY_USERS\.DEFAULT\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize`
```

➡️ If `.DEFAULT\...Themes` doesn't have a `Personalize` key either:

- Right-click on `Themes` ➜ **New ➜ Key** ➜ name it `Personalize`
    
- Add `AppsUseLightTheme` and `SystemUsesLightTheme` with value `0`
---

### 🔄 Optional: Automate it with PowerShell

Run the following in **PowerShell as Administrator** (from Audit Mode):
```
# Create the registry keys and set Dark Mode
$paths = @(
  "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize",
  "Registry::HKEY_USERS\.DEFAULT\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize"
)

foreach ($path in $paths) {
    if (-not (Test-Path $path)) {
        New-Item -Path $path -Force | Out-Null
    }
    Set-ItemProperty -Path $path -Name AppsUseLightTheme -Value 0 -Type DWord
    Set-ItemProperty -Path $path -Name SystemUsesLightTheme -Value 0 -Type DWord
}
```
---
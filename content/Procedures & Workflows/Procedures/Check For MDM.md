#Testing 
## 🔍 **1. Check for Autopilot/MDM Enrollment**

# 🔒 Checking for MDM in Audit Mode

**Purpose:**  
To verify if a device is enrolled in **Mobile Device Management (MDM)** while in **Audit Mode**.  
This ensures the device can be resold or repurposed without management restrictions.

---

## 🛠 Tools Needed
- The device (powered on, in **Audit Mode**)  
- Internet connection (if needed for verification)  

---

## 📋 Steps

1. **Boot into Audit Mode**  
   - Power on the device.  
   - At the OOBE (Out-of-Box Experience) screen, press:  
     - `Ctrl + Shift + F3`  
   - Device will restart into **Audit Mode** automatically.

2. **Check MDM Enrollment**  
   - Open **Command Prompt** (Run as Administrator).  
   - Enter the following command:  
	```powershell
		dsregcmd /status
	```  
   - Look for the following fields:  
     - `AzureAdJoined`  
     - `DomainJoined`  
     - `MDMUrl`  

3. **Interpret Results**  
   - If **AzureAdJoined = YES** → Device is Azure AD joined.  
   - If **DomainJoined = YES** → Device is on a local/domain network.  
   - If **MDMUrl** is populated → Device is enrolled in **MDM**.  
   - If all values show **NO / Empty** → Device is **not MDM enrolled**.

4. **Record Findings**  
   - Mark results in your testing sheet or Obsidian note.  
   - Example:  
     - `MDM: Not enrolled` ✅  
     - `MDM: Enrolled` ❌ (flag for supervisor)

---

You can also check:

- **Settings → Accounts → Access work or school** (will show if connected).
    
- **Event Viewer → DeviceManagement-Enterprise-Diagnostics-Provider** logs for enrollment attempts.
	- Access the event Viewer and location of logs
		- Win + R and enter eventvwr.msc
		- Applications and Services Logs → Microsoft → Windows → DeviceManagement-Enterprise-Diagnostics-Provider

---
## ✅ Pass / ❌ Fail Criteria
- **Pass:** Device shows **no MDM enrollment** (all fields clear).  
- **Fail:** Device shows **any MDM enrollment** (requires escalation).

---

## ⚠️ Notes
- Devices enrolled in MDM **cannot** be resold without proper removal.  
- If enrolled, escalate to supervisor for processing.  
- Always confirm using **Audit Mode** to avoid OOBE limitations.  

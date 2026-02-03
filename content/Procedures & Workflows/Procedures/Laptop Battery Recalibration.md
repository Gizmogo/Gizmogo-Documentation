---
tags:
  - Battery
  - Procedure
---

---

# Laptop Battery Recalibration Procedure

**Category:** Procedure  
**Author:** Seven  
**Last Updated:** 2025-09-04  
**Applies to:** Laptops with removable or embedded lithium-ion batteries

---

## Overview
This procedure explains how to recalibrate a laptop battery. Recalibration helps the system more accurately measure the battery’s charge and health, especially if the percentage readings are inconsistent or inaccurate.  

---

## Prerequisites
- [ ] Laptop charger  
- [ ] Access to system BIOS or battery management software (if applicable)  
- [ ] Stable environment (avoid high temperatures during discharge)  

---

## Steps
1. **Fully charge the battery**  
   - Connect the laptop to its power adapter.  
   - Charge the battery until it reaches **100%**.  
   - Leave it plugged in for an additional **2 hours** to ensure the cells are fully topped off.  

2. **Enable battery discharge**  
   - Disconnect the power adapter.  
   - Set the system to prevent sleep/hibernation (adjust power settings temporarily).  
   - Use the laptop on battery power until it shuts down automatically due to low charge.  

3. **Let the battery rest**  
   - Leave the laptop powered off for **at least 5 hours** (overnight is recommended).  
   - This ensures the battery is fully depleted.  

4. **Recharge without interruption**  
   - Reconnect the power adapter.  
   - Charge the battery uninterrupted to **100%** again.  
   - Do not use the laptop heavily during this cycle if possible.  

---

## Verification
- Check the system’s battery indicator (Windows Battery Report, macOS System Report, or OEM battery utility).  
- Battery percentage should now align more closely with actual charge capacity.  
- Note: This process does **not improve battery health**, only reporting accuracy.  

---

## Troubleshooting
| Symptom | Possible Cause | Solution |
|---------|----------------|----------|
| Battery does not reach 100% | Battery wear or calibration failure | Check battery health with OEM diagnostic tool. Replace if below 80% capacity. |
| Laptop shuts off abruptly at high percentage | Severe battery degradation | Replacement recommended. |
| Recalibration has no effect | Battery controller or firmware issue | Update BIOS/firmware; test with OEM utilities. |

---

## References / Related Notes
- [[Battery Health Testing Procedure]]  
- [[Laptop Power Troubleshooting]]  
- Manufacturer documentation for battery care

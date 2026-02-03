---
tags:
  - Troubleshooting
---

# Laptop Battery Troubleshooting
---
**Category:** Troubleshooting  
**Author:** Seven  
**Last Updated:** 2025-09-04  
**Applies to:** Laptops with lithium-ion batteries  


## Overview
---
This document lists common laptop battery issues, their likely causes, and recommended solutions. Use this guide when recalibration does not resolve the issue or when symptoms indicate deeper hardware problems.

## Common Issues
---
### 🔋 Battery Not Charging
| Symptom | Possible Cause | Solution |
|---------|----------------|----------|
| Battery stuck at certain % (e.g., 60%) | Battery protection setting enabled | Check OEM software (Lenovo Vantage, Dell Power Manager, etc.). Disable "Battery Conservation Mode" if longer runtime is needed. |
| Battery not detected | Loose connection or faulty battery | Reseat battery if removable. For embedded batteries, check connector. Replace if necessary. |
| Charger connected but no charging | Faulty charger or charging port | Test with known-good charger. Inspect port for damage. Replace as required. |

### ⚡ Short Runtime / Fast Drain
| Symptom | Possible Cause | Solution |
|---------|----------------|----------|
| Laptop dies quickly after full charge | Battery wear (low capacity) | Run battery health check (Windows: `powercfg /batteryreport`). Replace if design capacity < 80%. |
| Battery drains while laptop is off | BIOS or firmware issue | Update BIOS/EC firmware. Disable "Fast Boot" if enabled. |
| High background usage | OS or software consuming power | Check Task Manager/Activity Monitor. Optimize or repair OS. |

### 🌡️ Overheating or Swelling
| Symptom | Possible Cause | Solution |
|---------|----------------|----------|
| Battery gets hot during charge/discharge | Overload or failing cells | Stop using immediately. Replace battery. |
| Battery casing swollen | Gas buildup inside cells | Hazardous. Do **not** puncture. Replace and dispose per e-waste guidelines. |
| Laptop case bulging | Severe swelling | Power off and remove battery if safe. Replace immediately. |

### 🖥️ Inaccurate Charge Reporting
| Symptom | Possible Cause | Solution |
|---------|----------------|----------|
| % jumps up/down unexpectedly | Battery controller miscalibrated | Perform [[Laptop Battery Recalibration]]. |
| Battery shows 100% but dies quickly | Capacity degraded | Replace battery. |

## References / Related Notes
---
- [[Laptop Battery Recalibration]]  
- [[Laptop Power Troubleshooting]]  
- Manufacturer battery service manuals

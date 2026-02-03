#Defects 

## GPU Overheating
#### 🚨 Why This Might Be Happening

### 1. **Improper GPU Workload Allocation**

- Stress test may be **targeting the iGPU instead of the dGPU**.
    
- If the dGPU is idle, the iGPU may be doing all the graphics work.
    
- The iGPU shares the CPU's thermal envelope and cooling, so it heats up fast.
    

### 2. **Cooling System Prioritization**

- Zephyrus G14 is tuned to cool the **CPU and dGPU** more aggressively than the iGPU.
    
- The iGPU may not benefit from full fan curves or dedicated cooling paths.
    

### 3. **Power Profiles or BIOS/Firmware Settings**

- ASUS Armoury Crate might have a profile that:
    
    - Disables or limits the dGPU (e.g., Eco Mode).
        
    - Prioritizes battery or quiet performance at the expense of heat.
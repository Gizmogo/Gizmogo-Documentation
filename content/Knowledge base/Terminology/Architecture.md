---
tags:
  - x86-64
  - ARM64
  - Terminology
---

| Architecture | Tag     |
| ------------ | ------- |
| #x86-64      | AMD64   |
| #ARM64       | ARM64v8 |

>[!Info]
A CPU’s **architecture** is basically its “design blueprint” — it defines how the CPU fetches, decodes, and executes instructions, and what those instructions look like.
>
There are quite a few types, but they mostly fall into **a few common families**. I’ll break them down into **categories** and give a short description for each.

### **1. Common Instruction Set Architectures (ISA)**

These are the _most recognized_ CPU designs you’ll see in computers, phones, and embedded devices.

|Architecture|Key Traits|Common Uses|
|---|---|---|
|**x86** (Intel 8086, x86-64)|Complex Instruction Set Computing (**CISC**) — many instructions, some doing multi-step operations|PCs, laptops, many servers|
|**ARM**|Reduced Instruction Set Computing (**RISC**) — fewer, simpler instructions but very fast and power-efficient|Smartphones, tablets, some laptops (Apple M-series)|
|**RISC-V**|Open-source RISC architecture, highly customizable|Research, embedded systems, emerging CPUs|
|**PowerPC**|RISC design, once common in Macs and game consoles|Older Macs, IBM servers, legacy systems|
|**MIPS**|RISC design, very simple and widely used in embedded systems|Routers, IoT devices|

---

### **2. Architectural Design Philosophies**

Regardless of brand, most CPUs follow one of these styles:

1. **CISC (Complex Instruction Set Computer)**
    
    - Many instructions, some very complex.
        
    - Example: **x86**
        
    - Goal: Reduce the number of lines of code by having instructions do more work.
        
2. **RISC (Reduced Instruction Set Computer)**
    
    - Fewer instructions, all simple and fast.
        
    - Example: **ARM, RISC-V, MIPS**
        
    - Goal: Keep hardware simple, rely on software to do more.
        

---

### **3. Parallelism & Specialization Types**

Some architectures have special tweaks:

- **VLIW (Very Long Instruction Word)** – Executes multiple simple instructions in one cycle (e.g., Itanium).
    
- **Superscalar** – Can run multiple instructions at once by having several execution units.
    
- **Multicore** – Multiple CPU cores in one chip for parallel processing.
    
- **SIMD / Vector Architectures** – Process multiple data points in one instruction (good for graphics, AI).
    

---

### **4. Specialty / Legacy Architectures**

- **SPARC** – RISC CPU for servers and workstations (Oracle, Sun Microsystems).
    
- **Z/Architecture** – IBM mainframe CPUs.
    
- **6502** – Famous 8-bit CPU used in the NES, Commodore 64.
    
- **Motorola 68000** – Used in early Macs, arcade machines, and consoles like Sega Genesis.
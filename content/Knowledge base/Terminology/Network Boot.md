---
tags:
  - Terminology
---
## Network Boot (PXE Boot)

Network boot is the process of starting a computer without using a local storage device (like a hard drive or SSD). Instead, the computer loads its operating system or boot image directly from a server over the network.

This is typically done using **PXE (Pre-boot Execution Environment)**, which allows the computer’s network interface card (NIC) to communicate with a boot server right after the system powers on.

**Key points your technicians should know:**

- **Purpose:** Commonly used for deploying operating systems, running diskless workstations, or performing automated installations.
    
- **Requirements:** A PXE-capable NIC, DHCP server, and a TFTP/boot server providing the boot image.
    
- **Advantages:** Centralized management, faster mass deployments, no need for local media.
  
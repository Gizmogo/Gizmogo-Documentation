---
tags:
  - Workflow
---

---
1. [[Prepare device for PXE Boot]] 
2. [[Network boot]] the device and login to WipeOS
3. Enter the DeviceID into the Account Field located at Information Requirements
4. At the same location on Notes input the device's color and cosmetics
5. Procced to the diagnostics sub menu and select all available hardware for testing
6. Start the hardware diagnostics and follow all prompts until testing if finished
7. move over to the Gizmogo admin page and procced to Uncheck List under Quality Inspection Management in Order Management
8. Inter the DeviceID into the Device ID field, search, and click on check for your device
9. Associate order device and select your device
10. Click Get WipeOS quality inspection information, this should fill out most of the required information into the fields below
11. Color, Evaluation Level, and product Note must be filled by hand for the time being, use a template like [[Laptop Details]], additional templates can be found under the templates folder
12. IMPORTANT, for now all items must go to bargain for verification purposes Choose tags for reason of results, if no issues choose "Inspection: Passed"
13. In Custom notes, only copy DETAILS, CONDITIONS, and NOTES from product note leaving out the TEST and QUOTE sections
14. Double check all fields before submitting checking for discrepancies, after submitting move back to WipeOS
15. Procced to either the Disks or the NVMe sub menu, or both depending on what hardware the device is equipped with, select the disk to be wiped and select NIST SP 800-88r1 Clear (1-pass) with verify Wipe at 10%
16. Fill out Smart test, block size format, and filesystem partition format as needed or if needed
17. Next we need to reinstall an OS (Operating System) which can be done in the Imaging sub menu
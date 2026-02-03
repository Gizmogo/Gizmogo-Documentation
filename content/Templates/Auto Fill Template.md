---
tags:
  - Template
---

## Common Laptops Reference
---

```
[DETAILS]
Model: machine.machine.system.model
Device S/N: machine.machine.system.serial
Motherboard S/N: machine.machine.motherboard.serial
Battery health: machine.machine.batteries.[0].degradation
Drive health: machine.machine.storage.[0].smart_log.ssd_lifetime_remaining

[CONDITION]
Grade: 
Cosmetics: 
BIOS Lock: 
MDM Enrollment: 

[TESTS]
CPU: machine.job.diagnostics.cpu.result
Motherboard: machine.job.diagnostics.motherboard.result
Memory: machine.job.diagnostics.memory.result
Drives: machine.job.diagnostics.disk.result
Ethernet: machine.job.diagnostics.ethernet.result
Wi-Fi: machine.job.diagnostics.wifi.result
Keyboard: machine.job.diagnostics.keyboard.result
Display: machine.job.diagnostics.display.result
Battery: machine.job.diagnostics.battery.result
Microphone: machine.job.diagnostics.microphone.result
Speakers: machine.job.diagnostics.speakers.result
Webcam: machine.job.diagnostics.webcam.result
USBs: machine.job.diagnostics.usb.result

[Additional Details]
product key: machine.machine.system.product_key
WipeOS note: machine.machine.notes

[NOTE]


[QUOTE]

```

## Apple Laptops

```
[DETAILS]
Model: Apple machine.machine.apple.nice_name **machine.machine.apple.year**
Part Number: machine.machine.apple.a_model machine.machine.apple.emc machine.machine.apple.order_number
Device S/N: machine.machine.system.serial
Motherboard S/N: machine.machine.motherboard.serial
Battery health: machine.machine.batteries.[0].degradation
Drive health: machine.machine.storage.[1].smart_log.ssd_lifetime_remaining

[CONDITION]
Grade: 
Cosmetics: 
BIOS Lock: 
MDM Enrollment: 
Activation Lock:

[TESTS]
CPU: machine.job.diagnostics.cpu.result
Motherboard: machine.job.diagnostics.motherboard.result
Memory: **machine.job.diagnostics.memory.result**
Drives: **machine.job.diagnostics.disk.result**
Ethernet: **machine.job.diagnostics.ethernet.result**
Wi-Fi: 
Keyboard: **machine.job.diagnostics.keyboard.result**
Display: **machine.job.diagnostics.display.result**
Battery: **machine.job.diagnostics.battery.result**
Microphone: 
Speakers: 
Webcam: **machine.job.diagnostics.webcam.result**
USBs: **machine.job.diagnostics.usb.result**

[Additional Details]
WipeOS note: machine.machine.notes

[NOTE]


[QUOTE]

```
---
draft: false
---

> **Purpose**:
> To establish a standardized process for inspecting, testing, grading, and documenting the condition of video game consoles prior to resale, refurbishment, or recycling.

> **Scope**:
> Applies to all incoming game consoles including PlayStation, Xbox, Nintendo, and retro systems.

> **Audience**:
> QA technicians, warehouse staff, refurb/testing teams.

> [!note]
> This procedure is intended for **post-receipt testing** and does not cover customer-facing intake steps.

## 🧰 Tools & Equipment

- OEM power cables and adapters (model-specific)
- HDMI cables (tested & verified working)
- Display monitor (1080p minimum)
- Controller(s) compatible with console
- USB charging/data cables
- Internet access (Wi‑Fi + Ethernet if applicable)
- Game disc(s) or digital test account
- Cleaning supplies (microfiber cloth, compressed air, IPA 70%+)
- External storage (if required for testing)

> [!tip]
> Always verify that accessories used for testing are known working units to avoid false failures.

## 📥 Receiving Device

- Scan Device ID into System Admin Page
- Associate Device
- Verify model & brand
- Inspect packaging contents
- Confirm accessories included (power cable, remote, etc.)
- Check storage capacity

> [!warning]
> Do not power on devices showing signs of liquid damage or severe corrosion.

## ⚡ Power Test

### Initial Power Test

1. Connect OEM power cable.
2. Connect HDMI to testing monitor.
3. Power on console.

### Verify

- Power LED behavior
- Boot screen appears
- No unusual sounds (clicking, grinding fan)

> [!danger]
> If console does not power on, attempt alternate power cable. If still no power, classify as "No Power" and stop further testing.

## 🕹️ Setup

- Pair or connect controller.
- Complete initial setup (if required).
- Log into internal test account.

> [!important]
> Always sign in using **test accounts only**. Never use personal accounts.

## 🔎 Physical Inspection

### Exterior Condition Check

- Cracks or structural damage
- Deep scratches or cosmetic wear
- Missing screws or tamper signs
- Vent blockage (dust accumulation)

### Port Inspection

- HDMI port
- USB ports
- Power input
- Ethernet port
- Controller sync ports

### Controller Inspection

- Cracks or structural damage
- Deep scratches or cosmetic wear
- Missing screws or tamper signs
- Material build up
- Charging port

> [!caution]
> Any physical defect affecting usability must be documented and flagged.

## 🎮 Functional Testing Checklist

### 🖥️ System

#### Display Output

- Check resolution output
- Confirm no flickering
- Verify color accuracy

#### System Navigation

- Navigate menus
- Open settings
- Check storage info
- Confirm Wi-Fi connection

> [!failure]
> Any freezing, artifacting, loud fan surging, or overheating must be recorded and graded accordingly.

#### Storage & Drive Test

- Disc drive accepts/ejects smoothly (if applicable)
- Install small test game (if digital)
- Insert physical disc (if applicable)
- Game loads successfully
- Verify read speed
- Confirm no unusual noise
- Audio output clear

> [!bug]
> Disc read failures must be tested with at least two known-working discs.

### 🎮 Controller & Input 

#### Button Test

- Test all buttons
- D-pad
- Analog sticks (check drift)
- Vibration function

#### Wireless Connectivity

- Sync controller
- Test Bluetooth stability
- Check battery charging

## 🌡️Stress & Thermal Test

- Run a graphics-intensive game
- Monitor for overheating
- Listen for excessive fan noise
- Ensure ventilation
- Surface temperature should remain within acceptable range

> [!fail]
> Automatic shutdown during stress test should be recorded and marked as over heating

## 📶 Connectivity & Network

- Connect to Wi-Fi
- Perform system update check
- Test online login capability
- Access online store (if permitted).

> [!warning]
> If console is banned from online services, document status immediately.

## 🔄 Factory Reset (Post‑Test)

1. Navigate to system settings.
2. Select full factory reset.
3. Confirm removal of all accounts and data.
4. Verify device returns to initial setup screen.

> [!important]
> All consoles must be factory reset after testing.

## 📝 Documentation

- Record test results in internal system.
- Log failures with clear notes.
- Assign final condition grade.

>[!info]
> Utilize standard [[Device Conditions#Game Consoles|Device Conditions]] for grading

>[!note]
>Utilize [[Game Console Details]] for a template to record test results, documentation, and notes


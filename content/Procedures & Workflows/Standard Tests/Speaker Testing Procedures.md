# SOP: Testing Speakers, Smart Speakers & Audio Devices

> **Purpose**  
> Establish a standardized, repeatable process for testing speakers, smart speakers, and related audio devices to ensure accurate grading, quality control, and consistent customer outcomes.

> **Scope**  
> Applies to all wired speakers, Bluetooth speakers, smart speakers, soundbars, and voice‑assistant–enabled audio devices.

> **Audience**  
> QA technicians, warehouse staff, refurb/testing teams.

---

## 1. Pre‑Test Preparation

> [!info] Required Environment
> - Quiet testing area (minimal background noise)
> - Stable Wi‑Fi network (2.4 GHz & 5 GHz available)
> - Clean power source and surge protection

### 1.1 Tools & Equipment
- Test smartphone (iOS + Android preferred)
- Test tablet or laptop
- Known‑good AUX cable
- Known‑good power cable
- Wi‑Fi credentials
- Test audio files (bass, mids, highs, white noise)
- Voice command test script

### 1.2 Device Intake Check
- Verify model & brand
- Record serial number (if available)
- Inspect packaging contents
- Confirm accessories included (power cable, remote, etc.)

> [!warning] Intake Failure Rule
> If the device shows **physical damage affecting functionality**, skip testing and flag as **Non‑Functional / As‑Is**.

## 2. Physical Inspection

### 2.1 Exterior Condition
- Check speaker grille for dents or tears
- Inspect housing for cracks or separation
- Verify buttons/knobs are present and responsive
- Check ports for debris or corrosion

> [!tip]
> Cosmetic wear is acceptable if **audio and smart features function normally**.

### 2.2 Power Verification
- Plug device into power
- Confirm power indicator lights
- Power cycle device twice

## 3. Basic Audio Function Test

### 3.1 Wired Audio Test (If Applicable)
- Connect via AUX / line‑in
- Play test audio track
- Verify:
  - No distortion
  - Balanced left/right output
  - No crackling at low & high volume

### 3.2 Bluetooth Audio Test
- Pair with test phone
- Stream music for **at least 2 minutes**
- Walk 10–15 feet away to test signal stability

> [!failure]
> Dropouts, static, or pairing failures = **Audio Defect**.

## 4. Smart Speaker / Voice Assistant Test

### 4.1 Initial Setup
- Factory reset device
- Install required companion app
- Complete device setup on Wi‑Fi

> [!important]
> Always sign in using **test accounts only**. Never use personal accounts.

### 4.2 Microphone & Voice Recognition
Test the following commands:
- "What time is it?"
- "Set volume to 50%"
- "Play music"
- "Stop"

Verify:
- Wake word detection
- Accurate command execution
- Microphone responsiveness from 6–10 feet

### 4.3 Smart Features Validation
- Wi‑Fi stability (no disconnects)
- App control responsiveness
- Multi‑room / casting (if supported)

> [!warning]
> If the device **cannot connect to Wi‑Fi**, downgrade to **Smart Features Not Working**.

## 5. Sound Quality Evaluation

### 5.1 Frequency Test
Play test tones and verify:
- Bass: no rattling or buzzing
- Midrange: clear vocals
- Treble: no piercing or distortion

### 5.2 Volume Stress Test
- Increase volume gradually to max
- Play audio for 60 seconds

> [!failure]
> Any shutdowns, distortion, or speaker cut‑outs = **Fail**.

## 6. Controls & Connectivity

### 6.1 Physical Controls
- Power
- Volume up/down
- Mute / mic off

### 6.2 App & Remote Controls (If Applicable)
- Test all major functions
- Verify responsiveness < 1 second delay

## 7. Reset & Data Removal

> [!important]
> All smart devices **must be factory reset** after testing.

Steps:
1. Remove device from test account
2. Perform factory reset
3. Confirm reset by re‑entering setup mode

## 8. Grading & Classification

### 8.1 Functional Grades
![[Device Conditions#Speakers]]

### 8.2 Common Downgrade Reasons
- Distorted audio
- Weak microphone
- Wi‑Fi instability
- Non‑responsive buttons

## 9. Documentation & Reporting

- Record test results in QA system
- Attach photos of damage (if any)
- Log failures with clear notes

> [!success]
> Device is approved only if **all required tests pass**.

## 10. Safety & Handling

- Never open sealed speaker enclosures
- Avoid liquid exposure
- Do not test at max volume for extended periods


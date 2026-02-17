---
draft: false
---

> **Purpose**:
> Standardized process for testing speakers, smart speakers, and related audio devices to ensure accurate grading, quality control, and consistent customer outcomes.

> **Scope**:
> Applies to all wired speakers, Bluetooth speakers, smart speakers, soundbars, and voice‑assistant–enabled audio devices.

> **Audience**:
> QA technicians, warehouse staff, refurb/testing teams.

> [!note]
> This procedure is intended for **post-receipt testing** and does not cover customer-facing intake steps.

## 🧰 Tools & Equipment

- Test smartphone (iOS + Android preferred)
- Test tablet or laptop
- Known‑good AUX cable
- Known‑good power cable
- Wi‑Fi credentials
- Test audio files (bass, mids, highs, white noise)
- Voice command test script

> [!hint] Required Environment
> - Quiet testing area (minimal background noise)
> - Stable Wi‑Fi network (2.4 GHz & 5 GHz available)
> - Clean power source and surge protection
## 📥 Device Intake Check

- Scan Device ID into System Admin Page
- Associate Device
- Verify model & brand
- Inspect packaging contents
- Confirm accessories included (power cable, remote, etc.)

> [!warning]
> Do not power on devices showing signs of battery swelling or severe liquid damage.

## 🔋 Power Verification

- Plug device into power
- Confirm power indicator lights
- Power cycle device twice

> [!failure]
> If the device does **not power on**, mark as *Power Failure

## 📲 Pairing & Setup

- Factory reset the speaker. (if necessary)
- Pair with designated test phone or connect with companion app (if applicable)
- Confirm successful Bluetooth connection. (if applicable)
- Complete initial setup screens. (if applicable)

> [!important]
> Always test devices on a **known-good phone** 
> Always sign in using **test accounts only**. Never use personal accounts.

## 🔎 Physical Inspection

- Record model, size, color, and serial number
- Check speaker grille for dents or tears
- Inspect housing for cracks or separation
- Verify buttons/knobs are present and responsive
- Check ports for debris or corrosion

> [!warning]
> **Severe physical damage** may qualify the device for recycling or damaged evaluation.
## 🔊 Basic Audio Function Test

### Wired Audio Test (If Applicable)

- Connect via AUX / line‑in
- Play test audio track
- Verify:
  - No distortion
  - Balanced left/right output
  - No crackling at low & high volume

### Bluetooth Audio Test (If Applicable)

- Pair with test phone
- Stream music for **at least 2 minutes**
- Walk 10–15 feet away to test signal stability

> [!failure]
> Dropouts, static, or pairing failures = **Audio Defect**.

## 🗣️ Smart Speaker / Voice Assistant Test

### Initial Setup

- Install required companion app
- Complete device setup on Wi‑Fi

> [!important]
> Always sign in using **test accounts only**. Never use personal accounts.

### Microphone & Voice Recognition
Test the following commands:
- "What time is it?"
- "Set volume to 50%"
- "Play music"
- "Stop"

Verify:
- Wake word detection
- Accurate command execution
- Microphone responsiveness from 6–10 feet

### Smart Features Validation
- Wi‑Fi stability (no disconnects)
- App control responsiveness
- Multi‑room / casting (if supported)

> [!warning]
> If the device **cannot connect to Wi‑Fi**, downgrade to **Smart Features Not Working**.

## 🎚️ Sound Quality Evaluation

### Sound Profile Evaluation

Test using multiple genres:
- Spoken word / podcast
- Pop / vocal-focused music
- Bass-heavy tracks
- Classical or acoustic music

Evaluate:
- Bass (depth, control)
- Midrange (clarity, vocal presence)
- Treble (detail, harshness)
- Soundstage (width, separation)

> [!note]
> Keep volume at **~60–70%** unless distortion testing is required.

### Distortion & Volume Handling

1. Gradually increase volume.
2. Note the point where distortion begins.
3. Check for channel imbalance or rattling.

> [!danger]
> Do **not** sustain high volume levels for more than 30 seconds.

## 🎛️ Controls & Connectivity

### Bluetooth Performance (Wireless Only)

- Pairing speed
- Connection stability
- Dropouts (static / lag)
- Range test (line-of-sight, ~10 meters)

### Controls & Responsiveness

- Play/pause accuracy
- Volume control
- Touch or button sensitivity
- Voice assistant activation

### App & Remote Controls (If Applicable)

- Test all major functions
- Verify responsiveness < 1 second delay

## 7. 🔁 Reset & Data Removal

> [!important]
> All smart devices **must be factory reset** after testing.

- Unpair from test phone.
- Perform a full factory reset. (if applicable)

> [!success]
> Device is now cleared and ready for fulfillment or next processing step.

## 📝 Documentation

- Record test results in internal system.
- Log failures with clear notes.
- Assign final condition grade.

>[!info]
> Utilize standard [[Device Conditions#Speakers|Device Conditions]] for grading


---
draft: false
---

> **Purpose**:
> Standardized process for testing **headphones and earbuds** for audio quality, functionality, comfort, and overall performance.

> **Scope**:
> Applies to **wired, wireless, over-ear, on-ear, and in-ear devices** received for inspection and testing unless otherwise specified.

> **Audience**:
> QA technicians, warehouse staff, refurb/testing teams.

> [!note]
> This procedure is intended for **post-receipt testing** and does not cover customer-facing intake steps.

## 🧰 Tools & Equipment

- Test device (smartphone, tablet, or computer)
- Reference audio files (lossless preferred: WAV/FLAC)
- Streaming apps (Spotify, YouTube, Apple Music)
- Charging cable / power source

>[!tip] Test Environment
>- Quiet room with minimal ambient noise.
>- Seated, relaxed posture.
>- Stable internet connection. (for wireless testing)

> [!warning]
> Avoid noisy environments unless explicitly testing noise cancellation or call quality.

## 📥 Receiving Device
- Scan Device ID into System Admin Page.
- Associate Device.
- Verify model & brand
- Copy [[Standard Details]] into note section for documentation as you proceed with testing.
- Use [[AirPods Details]] for apple devices.

> [!warning]  
>- Do not power on devices showing signs of battery swelling or severe liquid damage.
>- Always disinfect used units before handling

## 🔋 Power & Charging Test

- connect the device to a charger.
- Confirm charging status.
- Power on device.
- Ensure device is sufficiently charged for testing.

> [!failure]
> If the device does **not power on**, mark as *Power Failure

## 📲 Pairing & Setup

- Factory reset the device. (if necessary)
- Pair with designated test phone or connect with companion app (if applicable)
- Confirm successful Bluetooth connection. (if applicable)
- Complete initial setup screens. (if applicable)

> [!tip]
> Always test devices on a **known-good phone** 
> Always sign in using **test accounts only**. Never use personal accounts.

## 🔎 Physical Inspection

- Record model, color, and serial number
- Inspect casing for scratches, dents, or separation
- Inspect headband and earcups or ear tips

> [!warning]
> **Severe physical damage** may qualify the device for recycling or damaged evaluation.

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

## 📶 Connectivity

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

## 🔄 Factory Reset (Post‑Test)

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
> Utilize standard [[Device Conditions#Headphones|Device Conditions]] for grading


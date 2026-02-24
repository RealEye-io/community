# How Webcam Eye-Tracking Works

This article explains the technology behind RealEye.io's webcam-based eye-tracking — how gaze is estimated, what affects accuracy, and how the data is processed.

---

## Overview

Traditional eye-tracking requires specialised infrared hardware costing thousands of dollars. Webcam eye-tracking replaces that hardware with computer vision and machine learning, using the participant's existing webcam to estimate where on the screen they are looking.

RealEye.io runs entirely in the browser — no software installation is required for participants.

---

## The Eye-Tracking Pipeline

### 1. Webcam access

With the participant's permission, the browser requests access to their webcam using the standard `getUserMedia` Web API. The video stream is processed locally in the browser — it is not streamed to RealEye.io servers in real time.

### 2. Face and eye detection

A computer vision model detects the participant's face and locates the eye regions within each video frame. This step is robust to typical variations in lighting and head position, but can fail in very poor conditions (darkness, strong backlighting, face obscured).

### 3. Gaze estimation

A machine learning model takes the detected eye region and maps it to a point on the screen. This model is trained on large datasets of known gaze positions paired with webcam images.

### 4. Calibration

To personalise the model for each participant (accounting for their unique eye physiology, webcam angle, and environment), a **calibration phase** is run at the start of each study. The participant looks at a series of dots on the screen, and the model is fine-tuned using this reference data.

Calibration typically takes 30–60 seconds and significantly improves accuracy.

### 5. Data recording

Once calibration is complete and the study begins, gaze coordinates (x, y screen position) are sampled at regular intervals (typically ~10 Hz for webcam-based tracking). These coordinates are timestamped and stored alongside stimulus timing data.

---

## Accuracy and Limitations

Webcam eye-tracking is less precise than dedicated hardware eye-trackers. Typical accuracy is within **1–3 degrees of visual angle**, which corresponds to roughly 2–5 cm on a standard monitor at normal viewing distance.

**Factors that improve accuracy:**
- Good, even lighting on the participant's face
- High-resolution webcam (720p or higher)
- Participant sitting still and centred in the frame
- Glasses-free or anti-reflective lenses

**Factors that reduce accuracy:**
- Low light or strong back-light
- Highly reflective glasses
- Significant head movement during the study
- Very low-resolution webcam

For research purposes, webcam eye-tracking is well-suited to tasks where approximate gaze patterns matter (e.g., comparing attention across regions) rather than tasks requiring sub-pixel precision.

---

## Privacy and Data Handling

- The webcam video stream is **processed locally** in the participant's browser
- Only the computed gaze coordinates (not the raw video) are sent to RealEye.io servers, unless the study is configured to record video
- Participants must explicitly consent to webcam access before the study begins
- Data handling complies with GDPR — see the [Privacy Policy](https://www.realeye.io/privacy-policy/) for details

---

## Further Reading

- [Getting Started](getting-started.md) – Set up your first study
- [FAQ](../../FAQ.md) – Common questions about accuracy, participants, and data
- [GitHub Discussions](https://github.com/RealEye-io/community/discussions) – Ask the community or the RealEye.io team

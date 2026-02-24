# Frequently Asked Questions

A collection of common questions about the [RealEye.io](https://www.realeye.io) Eye-tracking Platform. Can't find your answer here? Ask in [GitHub Discussions](../../discussions/categories/q-a) or contact us at **support@realeye.io**.

---

## General

### What is RealEye.io?

RealEye.io is a remote, webcam-based eye-tracking platform. It lets researchers run eye-tracking studies on participants anywhere in the world using only a standard webcam — no specialised hardware needed.

### How accurate is webcam eye-tracking?

Webcam eye-tracking accuracy depends on the participant's camera quality, lighting conditions, and calibration. RealEye.io achieves accuracy comparable to other remote eye-tracking solutions, typically within 1–2 degrees of visual angle under good conditions. It is best suited for tasks where approximate gaze data is sufficient (e.g., heatmaps, general attention patterns).

### What browsers and devices are supported?

RealEye.io works in modern desktop browsers (Chrome, Firefox, Edge, Safari). Participants must use a device with a webcam. Mobile devices are not currently supported for data collection.

### Is RealEye.io GDPR compliant?

Yes. RealEye.io is built with GDPR compliance in mind. Participants are informed about data collection, and their consent is obtained before a study begins. Please review our [Privacy Policy](https://www.realeye.io/privacy-policy/) for full details.

---

## Studies & Stimuli

### What types of stimuli can I test?

RealEye.io supports the following stimulus types:

- **Images** – Static screenshots, mockups, or designs
- **Websites** – Live URLs loaded in an embedded iframe
- **Videos** – Uploaded video files
- **5-Second Tests** – Show an image for 5 seconds, then collect impressions

### How many participants do I need?

For quantitative heatmap data, we generally recommend a minimum of **30–40 participants**. For qualitative insights, smaller groups can still provide useful signals. The right sample size depends on your research goals.

### Can I recruit participants through RealEye.io?

Yes. RealEye.io integrates with research panels so you can recruit participants directly. You can also share your study link with your own participant pool.

### Can I set up Areas of Interest (AOIs)?

Yes. After collecting data, you can define AOIs on your stimuli to analyse fixation counts, gaze duration, and time-to-first-fixation for specific regions.

---

## Data & Analysis

### What data does RealEye.io collect?

For each participant, RealEye.io records:

- Gaze coordinates over time (x, y positions on the stimulus)
- Fixations and saccades
- Webcam video (optionally, depending on study settings)
- Survey and task responses (if included in the study)

### Can I export raw data?

Yes. Raw gaze data can be exported in CSV format from the study results panel for further analysis in tools like R, Python, or Excel.

### How long is data retained?

Data retention depends on your subscription plan. Please check your account settings or contact support for details.

---

## Account & Billing

### Is there a free plan?

Yes. RealEye.io offers a free tier with limited participants per study. Paid plans unlock higher participant limits, advanced features, and priority support. See the [Pricing page](https://www.realeye.io/pricing/) for current options.

### How do I upgrade or cancel my plan?

You can manage your subscription from within your RealEye.io account dashboard, or contact **support@realeye.io** for assistance.

---

## Technical

### Why is calibration failing for some participants?

Common causes include:

- Poor lighting (too dark, or strong backlight behind the participant)
- Glasses with reflective lenses
- The participant's face is too far from or too close to the camera
- Low-resolution or obstructed webcam

Advise participants to sit in a well-lit environment facing the light source, with their face centred in the webcam frame.

### Can I embed a RealEye.io study in my own website?

Study links can be shared directly with participants. Embedding options may vary by plan — contact support for guidance on custom integrations.

### I found a bug. How do I report it?

Please open a [Bug Report](../../issues/new?template=bug_report.yml) using the issue template. Include as much detail as possible to help us reproduce and fix the problem quickly.

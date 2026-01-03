# AuraSense AR 🛰️ 
**Spatial Navigation for the Visually Impaired**

[![Unity](https://img.shields.io/badge/Unity-2022.3%20LTS-black?logo=unity)](https://unity.com/)
[![Platform](https://img.shields.io/badge/Platform-Android-green?logo=android)](https://www.android.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

AuraSense AR is an Augmented Reality (AR) accessibility tool designed to help visually impaired individuals navigate indoor environments. By converting spatial data into real-time audio and haptic feedback, the app creates a "sensory bridge" for the user.

---

## 🚀 Key Features

- **3D Sonar Feedback:** Uses ARCore Raycasting to detect obstacles and maps distance to audio pitch. As you get closer to an object, the pitch rises.
- **Haptic Proximity Alerts:** The device vibrates when an obstacle is within a "Critical Zone" (less than 0.5 meters).
- **Inclusive UI:** Built with the **UI Accessibility Plugin (UAP)** to support Screen Readers (TalkBack).
- **Voice Assistant:** A double-tap gesture activates a Speech-to-Text loop for hands-free status updates.

---

## 🛠️ Tech Stack

- **Engine:** Unity 2022.3.x LTS
- **AR Framework:** AR Foundation (Google ARCore)
- **Accessibility:** UI Accessibility Plugin (UAP)
- **Programming:** C#

---

## 📥 Installation

1. Go to the [Releases](YOUR_RELEASE_LINK_HERE) section of this repository.
2. Download the `AuraSense_v1.apk`.
3. Transfer the file to your Android device.
4. Enable "Install from Unknown Sources" in your Android settings and install the app.

> **Note:** Requires an ARCore-compatible Android device running Android 7.0 or higher.

---

## 🧠 How it Works (Logic Flow)

The application uses a **Sense-Process-Respond** loop:
1. **Sense:** `ARRaycastManager` shoots a ray from the center of the camera.
2. **Process:** The script calculates the distance ($d$) from the camera to the hit point.
3. **Respond:** The audio frequency is adjusted using:
   `audioSource.pitch = Mathf.Lerp(maxPitch, minPitch, distance / maxRange);`



---

## 📂 Project Structure

- `/Assets/Scripts/Core`: Main AR and Sonar logic.
- `/Assets/Scripts/Accessibility`: TTS/STT and UI Focus logic.
- `/Builds`: Contains the compiled APK file.
- `/Documentation`: Technical diagrams and user manuals.

---

## 👤 Author
- **[Ramya S]**
- [www.linkedin.com/in/
ramya-sathaiyan-046694318]



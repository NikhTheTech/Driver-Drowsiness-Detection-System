

# Driver Drowsiness Detection System 🚗💤

A real-time **Driver Drowsiness Detection System** built with **OpenCV, Dlib, NumPy, and Pygame**.
This project uses facial landmark detection to monitor a driver's eye aspect ratio (EAR) and triggers an alarm if drowsiness or sleepiness is detected.

---

## 📌 Features

- Real-time face and eye detection using **dlib’s 68 facial landmarks**
- Calculates **Eye Aspect Ratio (EAR)** to detect blinking, drowsiness, and sleepiness
- Plays an **alarm sound** when the driver is sleepy
- Displays live **video feed with status overlay** (ACTIVE, DROWSY, SLEEPY)
- Lightweight and runs on most machines with a webcam


---

## 🛠️ Tech Stack

* **Python** (>= 3.13)
* **OpenCV** – for video processing and image handling
* **Dlib** – for face detection and facial landmark extraction
* **NumPy** – for mathematical operations
* **Pygame** – for playing the alarm sound

---

## 📂 Project Structure

```
Driver-Drowsiness-Detection/
│
├── shape_predictor_68_face_landmarks.dat  # Pre-trained dlib model
├── alarm.wav                              # Alarm sound file
├── drowsiness_detection.py                # Main script
└── README.md                              # Project documentation
```

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```
git clone https://github.com/NikhTheTech/Driver-Drowsiness-Detection-System.git
cd Driver-Drowsiness-Detection-System
```

### 2️⃣ Install Dependencies

Make sure you have Python installed, then run:

```
pip install opencv-python dlib imutils numpy pygame
```

> **Note:**
>
> * `dlib` may require **CMake** and **Visual Studio Build Tools** (on Windows) or `brew install cmake` (on macOS).
> * Download `shape_predictor_68_face_landmarks.dat` from [dlib’s model repository](http://dlib.net/files/) and place it in the project folder.

---

## ▶️ Usage

Run the script:

```
python drowsiness_detection.py
```

* **Press `ESC`** to exit the program.
* The system will display your webcam feed with status indicators:

  * 🟢 **ACTIVE** – Driver is awake and alert
  * 🔵 **DROWSY** – Driver is starting to feel sleepy
  * 🔴 **SLEEPY** – Driver is falling asleep (alarm plays)

---

## 📊 How It Works

1. Detects face using **dlib’s frontal face detector**
2. Extracts **eye landmarks** using `shape_predictor_68_face_landmarks.dat`
3. Calculates **Eye Aspect Ratio (EAR)**

   * EAR drops when eyes are closed
   * If closed for several frames → considered **drowsy/sleepy**
4. Plays alarm sound if the driver is not responding

---

## 🚀 Future Improvements

* Add **yawn detection** using mouth landmarks
* Deploy as a **mobile app** or **Raspberry Pi solution**
* Improve accuracy with **CNN-based blink detection**
* Add **night-mode support** with IR cameras

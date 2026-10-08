# Crowd-Sense

## Real-Time Crowd Density Monitoring and Early Danger Alerts
[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vedantthakare1/Crowd-Sense/blob/main/crowdsense_improved.ipynb)

Crowd-Sense is a computer-vision based system designed to monitor crowd density in real time and provide early warnings when a zone becomes dangerously crowded.

The system uses a camera feed, a pre-trained YOLO object detection model, and OpenCV to detect and count people across different zones of a video frame.

---

## 🚨 Problem

Crowd incidents can begin when people become densely concentrated in a particular area without being noticed in time.

Traditional CCTV systems mainly provide video that requires continuous human monitoring. They do not automatically identify which area is becoming dangerously crowded or provide an immediate threshold-based warning.

---

## 💡 Our Solution

Crowd-Sense converts ordinary camera footage into a visual crowd-density monitoring system.

### System Pipeline

Camera Feed  
↓  
Person Detection  
↓  
Zone-wise Counting  
↓  
Density Heatmap  
↓  
Danger Alert

The system divides the camera frame into multiple zones and counts the detected people in each zone.

Each zone is assigned a status:

🟢 **Green — Safe**

🟡 **Yellow — Caution**

🔴 **Red — Danger**

When the number of detected people in a zone crosses the configured danger threshold, the system raises a **Danger Zone** alert.

---

## ⚙️ How It Works

1. A video is uploaded to the system.
2. YOLO detects people in each frame.
3. The center point of each detected person is assigned to a zone.
4. People are counted separately for every zone.
5. Each zone is assigned a Green, Yellow, or Red status.
6. A danger alert is displayed when the red threshold is crossed.
7. The processed video can be viewed and downloaded.

---

## 🧠 Technologies Used

- Python
- OpenCV
- YOLO
- NumPy
- Google Colab

---

## ✨ Features

- Real-time person detection
- Zone-wise crowd counting
- Green/Yellow/Red density heatmap
- Configurable crowd thresholds
- Danger Zone alerts
- Video upload support
- Works with different video resolutions
- Processed video output

---

## 🧪 Prototype

The prototype was developed in Google Colab using Python, OpenCV and a pre-trained YOLO model.

It was tested on sample crowd footage to demonstrate zone-wise crowd monitoring and threshold-based danger alerts.

---

## ⚠️ Limitations

The current prototype performs best with medium-sized crowds.

Detection accuracy can decrease when:

- People overlap heavily
- Lighting conditions are poor
- The camera angle is too low
- People are partially hidden behind other people

The current prototype provides threshold-based early warning. It does not yet predict future crowd flow.

---

## 🔮 Future Scope

Future improvements include:

- Crowd-flow prediction from density trends
- Mobile and SMS alerts
- Multi-camera support
- Better models for dense crowds
- Custom zone selection
- Testing at real-world venues

---

## 📁 Project Structure

```text
Crowd-Sense/
│
├── Crowd-Sense.ipynb
├── README.md
└── sample/
---

## 🎥 Demo

The following video demonstrates the Crowd-Sense prototype processing crowd footage, detecting people, counting them by zone, displaying the Green/Yellow/Red density status, and raising a danger alert when the configured threshold is crossed.
[▶️ Watch the Crowd-Sense Demo](./crowdsense_output.mp4)

# 🚁 AI-Powered Precision Spraying Drone for Smart Agriculture

## 🌱 Overview

The **AI-Powered Precision Spraying Drone** is an intelligent agriculture solution developed during the **24-Hour CHIP TO CROP Agritech Hackathon**, organized by Build Club, Presidency University in collaboration with ICAR-IIHR.

This project integrates **Artificial Intelligence, Computer Vision, Embedded Systems, and Drone Technology** to identify crop diseases and perform **targeted pesticide spraying**, reducing chemical wastage and improving farming efficiency.

---

## 📌 Problem Statement

Traditional pesticide spraying methods face several challenges:

* High manual labor requirements
* Direct exposure of farmers to harmful chemicals
* Uneven pesticide distribution
* Excessive pesticide usage
* Increased operational costs

These limitations highlight the need for an automated and precision-based agricultural solution.

---

## 💡 Proposed Solution

The AI-Powered Precision Spraying Drone uses a camera mounted on a drone along with a YOLOv8-based disease detection model to identify infected crop regions in real time.

### Workflow

1. Capture live crop images using the onboard camera.
2. Process images using the trained YOLOv8 model.
3. Detect diseased leaves and affected crop areas.
4. Trigger targeted pesticide spraying only where required.
5. Monitor detections and spraying activity through a web dashboard.

---

## ✨ Key Features

* 🔍 Real-time crop disease detection
* 🎯 Precision pesticide spraying
* 📷 Live camera monitoring
* 🧠 YOLOv8-based AI model
* 🍓 Disease identification from crop images
* 🌐 Web-based monitoring dashboard
* 🖥️ Raspberry Pi deployment
* 🌱 Reduced pesticide wastage
* 👨‍🌾 Enhanced farmer safety

---

## 🛠️ Technology Stack

### Artificial Intelligence & Computer Vision

* YOLOv8
* OpenCV
* Python
* NumPy

### Embedded Systems

* Raspberry Pi
* Pi Camera Module
* Relay Module
* Mini Water Pump and motors

### Web Application

* Flask
* HTML
* CSS
* JavaScript

### Development Tools

* Google Colab
* Roboflow
* GitHub

---

## 📂 Project Structure

```text
AI-Precision-Spraying-Drone/
│
├── AI_model/              # YOLOv8 model files and training notebooks
├── app/                   # Flask web application
├── raspberry_pi/          # Raspberry Pi deployment scripts
├── docs/                  # Project documentation
├── images/                # Project images and screenshots
├── Presentation/          # Hackathon presentation
├── requirements.txt       # Required Python packages
└── README.md
```

---

## 🧠 AI Model Training

The disease detection model was trained using:

* Custom crop disease dataset
* Roboflow for dataset preprocessing
* YOLOv8 for object detection
* Google Colab for training and evaluation

### Training Pipeline

1. Dataset Collection
2. Data Annotation
3. Dataset Augmentation
4. YOLOv8 Training
5. Model Evaluation
6. Raspberry Pi Deployment

---

## 📊 Expected Impact

* Reduce pesticide consumption
* Improve crop health monitoring
* Lower operational costs
* Increase agricultural productivity
* Promote sustainable farming practices

---

## 🔮 Future Scope

* GPS-guided autonomous navigation
* Fully automated spraying mechanism
* Mobile application integration
* Multi-crop disease detection
* Cloud-based monitoring
* Large-scale field deployment
* IoT sensor integration for smart farming

---

## 👥 Team Members

* P. Tejaswini
* Inchara K R
* Sahana Haragapure
* Bharath R K
* K. Sai Krishna
* Varadharajula Nishant

---

## 🏆 Hackathon Details

### CHIP TO CROP – 24 Hour Agritech Hackathon

Organized By:

* Build Club
* Presidency University

In Collaboration With:

* ICAR
* IIHR

---

## 📸 Project Demonstration

Add screenshots, drone images, dashboard images, and detection results in the `images` folder and display them here.

---


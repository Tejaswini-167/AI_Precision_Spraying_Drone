# Project Workflow

## Overview

The AI-Powered Precision Spraying Drone is designed to detect crop diseases in real time and perform targeted pesticide spraying only on affected plants. The system combines Computer Vision, Artificial Intelligence, Raspberry Pi, and Drone Technology to support precision agriculture.

---

## Step 1: Data Collection

The project begins with collecting images of healthy and diseased crop leaves.

### Crops Included
- Bell Pepper
- Potato
- Grape
- Corn

### Disease Classes
- Bell Pepper Bacterial Spot
- Black Rot
- Esca
- Grape Leaf Blight
- Potato Early Blight
- Potato Late Blight
- Healthy Leaf Classes

The collected images form the dataset used for model training.

---

## Step 2: Data Annotation

The images are uploaded to Roboflow for annotation.

### Annotation Process
- Diseased regions are marked using bounding boxes.
- Each image is assigned the correct class label.
- The dataset is split into:
  - Training Set
  - Validation Set
  - Test Set

This prepares the dataset for YOLOv8 training.

---

## Step 3: Model Training

The annotated dataset is trained using YOLOv8.

### Training Environment
- Google Colab
- Python
- Ultralytics YOLOv8

### Training Objectives
- Learn disease patterns
- Improve detection accuracy
- Minimize false detections

The final trained model is exported as:

```text
best.pt
```

---

## Step 4: Model Deployment

The trained model is transferred to the Raspberry Pi.

### Deployment Components
- Raspberry Pi
- Pi Camera Module
- YOLOv8 Model
- OpenCV

The Raspberry Pi becomes the onboard AI processing unit.

---

## Step 5: Live Image Acquisition

During drone operation, the Pi Camera continuously captures images of crop fields.

### Camera Tasks
- Capture live video feed
- Extract frames
- Send frames for AI inference

The captured frames serve as input to the detection model.

---

## Step 6: Disease Detection

Each captured frame is processed by the YOLOv8 model.

### Detection Process
1. Receive image frame
2. Run inference
3. Identify disease class
4. Generate confidence score
5. Draw bounding boxes

### Output
- Disease Name
- Confidence Percentage
- Bounding Box Location

---

## Step 7: Decision Making

The Raspberry Pi analyzes the detection results.

### Logic

If:

```text
Confidence > Threshold
```

Then:

```text
Disease Detected
```

Else:

```text
No Action Required
```

This prevents unnecessary spraying.

---

## Step 8: Precision Spraying

When a disease is detected:

1. Raspberry Pi sends a signal to the spraying mechanism.
2. Relay module activates the pump.
3. Pesticide is sprayed only on affected plants.

### Benefits
- Reduced chemical usage
- Lower operational cost
- Improved crop protection
- Environmentally friendly farming

---

## Step 9: Monitoring Dashboard

A Flask-based web application provides real-time monitoring.

### Dashboard Features

- Live Video Streaming
- Disease Detection Results
- Plant Health Information
- Spray Status Monitoring

Users can observe the drone's operation remotely.

---

## Step 10: Field Operation

The drone continues scanning crops while:

- Capturing images
- Detecting diseases
- Triggering spraying actions
- Updating monitoring data

This creates an automated crop surveillance and treatment system.

---

## System Architecture

```text
Pi Camera
    |
    v
Image Capture
    |
    v
YOLOv8 Disease Detection
    |
    v
Detection Results
    |
    +----------------+
    |                |
    v                v
Flask Dashboard   Spray Decision
                        |
                        v
                 Relay Activation
                        |
                        v
                Precision Spraying
```

---

## Expected Outcome

The proposed system enables:

- Early disease detection
- Targeted pesticide application
- Reduced pesticide waste
- Increased farming efficiency
- Smart agriculture automation

By integrating Artificial Intelligence, Computer Vision, and Embedded Systems, the solution supports modern precision farming practices.
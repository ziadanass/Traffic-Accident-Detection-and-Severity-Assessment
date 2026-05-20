# Real-Time Traffic Accident Detection & Severity Assessment System

An automated, intelligent two-stage deep learning framework designed for real-time traffic accident detection and severity assessment using CCTV surveillance footage. This system integrates lightweight architectures to ensure high-speed processing suitable for automated traffic incident management systems.

## 🚀 Key Features
- **Two-Stage Intelligent Pipeline:** - **Stage 1 (Binary Classification):** Detects whether an accident has occurred or not (Accident vs. Non-Accident) using a tuned **MobileNetV2** backbone.
  - **Stage 2 (Multi-Class Classification):** Evaluates the severity score of the detected accident into three distinct levels: **Minor**, **Substantial**, or **Critical Impact**.
- **Contextual Awareness:** Integrated **YOLOv8-nano** object detection to localize vehicles and provide live traffic scene context (vehicle counts and object tracking).
- **Lightweight & Real-Time Deployable:** Optimized for edge devices and standard monitoring hardware with minimal parameter footprint.

## 📊 Performance & Results
The framework demonstrates high reliability and generalization capabilities:
- **Accident Detection Model (Stage 1):** Achieved an overall accuracy of **~97.9%** on test data.
- **Severity Assessment Model (Stage 2):** Achieved a peak performance of **100%** accuracy on the experimental dataset.
- **Robust Generalization:** Successfully tested on real-world ground-level Egyptian road accident imagery, maintaining a **99.9%** detection confidence.

### Confusion Matrices
The system shows clear class separation without overlap:
- **Model 1 (Binary Classification):** Extremely low False Negative rate ensuring critical accidents are never missed.
- **Model 2 (Severity Assessment):** Clear diagonal alignment showcasing flawless sorting of impact levels.

## 🛠️ Software Stack & Technologies
- **Deep Learning Framework:** TensorFlow & Keras                    
- **Computer Vision:** OpenCV, Ultralytics (YOLOv8)
- **Data Manipulation & Analytics:** NumPy, Scikit-learn
- **Visualization:** Matplotlib, Seaborn
- **Development Environment:** Google Colab / VS Code

**💡 System Workflow Architecture**
**Input: CCTV Video Frame / Image.**

**Pre-processing & Context:** YOLOv8-nano extracts vehicle bounding boxes and labels.

**Stage 1 Binary Classifier:** MobileNetV2 checks for accidents.

**Stage 2 Multi-Class Classifier:** If an accident is detected, MobileNetV2 evaluates severity and plots the confidence distribution dynamically.






## 📁 Repository Structure
```text
├── accident_detection_project.ipynb   # Main Jupyter Notebook with full code pipeline
├── requirements.txt                   # Required Python libraries and frameworks
└── README.md                          # Project documentation


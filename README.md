# 🚗 Driver Distraction Detection System

A comprehensive deep learning-based system to detect and analyze driver distraction through image, video, and document processing, powered by both custom models and LLM integration.

## 🧠 Project Overview

This project was developed as a final year engineering project by our team to tackle the critical issue of driver distraction. We have iteratively improved the approach — from multi-class image classification to a generalized, multi-modal intelligent platform.

## 📌 Key Features

- ✅ Driver state classification using CNNs
- 📉 Model optimization through feature cropping
- 🎥 Video-based temporal analysis for real-time detection
- 📊 Document analysis using LLMs (Gemini 2.0 Flash)
- 🌐 Internet search integration for comparative research
- 💡 Unified platform for image, video, and document input

---

## 🔍 Problem Statement

Detect distracted driving behavior using camera inputs. Originally framed as a 10-class classification task based on in-car camera images, we later reframed the problem for better generalization and real-time applicability.

---

## 🗂️ Datasets Used

1. **[State Farm Driver Distraction Detection Dataset](https://www.kaggle.com/competitions/state-farm-distracted-driver-detection)**  
   - 10 classes (safe driving, texting, reaching, operating radio, etc.)
2. **[Drowsiness Detection Dataset](https://www.kaggle.com/datasets/ismailnasri20/driver-drowsiness-dataset-ddd)**  
   - 2 classes: Drowsy and Alert
3. **[Eye and Mouth Datasets](https://www.kaggle.com/datasets/prasadvpatil/mrl-dataset,https://www.kaggle.com/datasets/davidvazquezcic/yawn-dataset/data)**  
   - Used to reduce input feature size and improve efficiency
4. **[NITYMED Dataset](https://www.kaggle.com/datasets/nikospetrellis/nitymed)**  
   - Used for capturing temporal patterns in driver behavior

---

## 🧪 Approach & Models

### Phase 1: Custom CNN for 10-Class Detection
- Built from scratch, not using pre-trained models.
- Achieved strong training/testing accuracy.
- Generalization was poor in borderline cases.

### Phase 2: Binary Classification
- Reduced to 2-class problem (drowsy vs. alert).
- New architecture designed and trained.
- Improved performance and interpretability.

### Phase 3: Feature-Focused Input
- Eye and mouth crops used for focused classification.
- Achieved computational efficiency and faster inference.

### Phase 4: Temporal Analysis
- Used a video dataset to detect yawning and microsleep.
- Extracted frames → fed to CNN → predictions aggregated.
- Noted ~10s inference lag in real-world tests.

---

## ⚙️ Platform Integration

We built a full-stack platform with the following capabilities:

- 🖼️ **Image & Video Analysis**  
  Uploads are classified using custom models.

- 📄 **Document QA & Summarization**  
  PDF/Docx files can be queried for structured responses using Gemini 2.0 Flash.

- 🌐 **Internet Search Integration**  
  Enables model to compare against web-published research or gather real-time info.

---

## 🌍 Tech Stack

- **Python, TensorFlow/Keras, OpenCV**
- **Hugging Face**
- **Gemini 2.0 Flash** 
- **Grounding With Internet Search** 

---

## 🚀 Future Work

- Improve real-time video inference speed (<3 seconds).
- Robust generalization to unseen real-world data.
- Extend to alerting systems (e.g., haptic/vibration feedback).

---

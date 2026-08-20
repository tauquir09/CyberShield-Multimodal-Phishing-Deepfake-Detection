# 🛡️ CyberShield

### Unified Multi-Modal Authenticity Scoring System for Phishing and Deepfake Detection

CyberShield is an AI-powered cybersecurity platform designed to detect **phishing URLs** and **deepfake facial images** within a single unified system.

The project combines Machine Learning and Deep Learning models with explainable AI techniques to provide not only predictions but also interpretable threat assessments.

CyberShield supports individual URL analysis, deepfake image analysis, combined multi-modal threat detection, explainability, detection history, REST API access, and dashboard visualization.

---

## 🚀 Key Features

* 🔗 Phishing URL Detection
* 🖼️ Deepfake Image Detection
* 🧠 Machine Learning + Deep Learning
* 🔀 Multi-Modal Threat Fusion
* 📊 Unified Threat Score
* 🔍 LIME Explainability for Phishing Detection
* 🔥 Grad-CAM Visualization for Deepfake Detection
* 📈 Detection History Dashboard
* ⚡ FastAPI REST API
* 🎨 Streamlit Web Interface
* 🗃️ SQLite Detection Logging
* 🐳 Docker Support

---

## 🎯 Project Objective

The objective of CyberShield is to build a unified cybersecurity solution capable of detecting multiple forms of digital deception.

Traditional cybersecurity solutions generally handle phishing and manipulated media independently.

CyberShield combines both detection mechanisms and generates a single threat assessment using a weighted multi-modal fusion engine.

The system classifies the final threat into five categories:

* Safe
* Low
* Medium
* High
* Critical

---

# 🏗️ System Architecture

CyberShield follows a three-layer architecture:

### 1. Presentation Layer

Built using **Streamlit**.

The interface provides:

* URL Analysis
* Image Analysis
* Combined Analysis
* Detection Dashboard

### 2. Application Layer

Built using **FastAPI**.

Responsibilities include:

* Input validation
* Model inference
* Multi-modal fusion
* Database logging
* REST API handling
* Structured JSON responses

### 3. Model & Data Layer

Contains:

* Phishing Detection Model
* Deepfake Detection Model
* Feature Extraction
* Fusion Engine
* SQLite Database

---

# 🔗 Phishing Detection

The phishing detection module analyzes URLs using engineered URL-based features.

An ensemble of:

* Random Forest
* XGBoost

is used to classify URLs as either:

```text
Legitimate
```

or

```text
Phishing
```

The model analyzes **15 selected URL features** and generates a phishing risk score.

### Explainability

CyberShield integrates **LIME (Local Interpretable Model-Agnostic Explanations)** to explain which URL characteristics contributed most strongly to a phishing prediction.

---

# 🖼️ Deepfake Detection

The deepfake detection module uses a fine-tuned:

```text
EfficientNetB4
```

Convolutional Neural Network.

The model determines whether an uploaded facial image is:

```text
Real
```

or

```text
Deepfake
```

The model was trained using transfer learning and later fine-tuned for improved performance.

### Explainability

CyberShield integrates **Grad-CAM** to generate heatmaps highlighting the regions of the image that contributed most strongly to the prediction.

---

# 🔀 Multi-Modal Threat Fusion

CyberShield combines phishing and deepfake predictions into a single threat score.

The fusion system uses weighted scoring:

```text
Phishing Weight = 0.55

Deepfake Weight = 0.45
```

The resulting score is classified into:

| Threat Score | Threat Level |
| ------------ | ------------ |
| 0 – 19       | Safe         |
| 20 – 39      | Low          |
| 40 – 59      | Medium       |
| 60 – 79      | High         |
| 80 – 100     | Critical     |

This allows CyberShield to analyze multiple attack vectors simultaneously.

---

# 📊 Model Performance

## Phishing Detection

| Metric        |                  Result |
| ------------- | ----------------------: |
| Test Accuracy |                     92% |
| AUC-ROC       |                  0.9716 |
| Features Used |                      15 |
| Models        | Random Forest + XGBoost |

## Deepfake Detection

| Metric        |         Result |
| ------------- | -------------: |
| Test Accuracy |         96.33% |
| Test AUC      |         0.9941 |
| Model         | EfficientNetB4 |
| Test Images   |         20,000 |

The EfficientNetB4 model was trained using a two-phase transfer learning approach.

---

# 📂 Datasets

## Phishing Dataset

**Web Page Phishing Detection Dataset**

Source:

```text
Kaggle
```

Dataset Size:

```text
11,430 URLs
```

Classes:

```text
5,715 Legitimate
5,715 Phishing
```

---

## Deepfake Dataset

**140K Real and Fake Faces Dataset**

Source:

```text
Kaggle
```

Total Images:

```text
140,000
```

Dataset Split:

```text
Training: 100,000 images
Validation: 20,000 images
Testing: 20,000 images
```

Classes:

```text
Real
Fake
```

---

# 🛠️ Technology Stack

### Programming Language

```text
Python 3.11
```

### Machine Learning

```text
scikit-learn
XGBoost
Random Forest
LIME
```

### Deep Learning

```text
TensorFlow
Keras
EfficientNetB4
Grad-CAM
OpenCV
```

### Backend

```text
FastAPI
Uvicorn
```

### Frontend

```text
Streamlit
Plotly
```

### Database

```text
SQLite
aiosqlite
```

### Deployment

```text
Docker
Docker Compose
```

---

# 📁 Project Structure

```text
CyberShield/
│
├── api/
│   └── main.py
│
├── app/
│   └── app.py
│
├── modules/
│   ├── phishing_module.py
│   ├── deepfake_module.py
│   └── fusion_engine.py
│
├── database/
│   └── logger.py
│
├── models/
│   ├── phishing_model.pkl
│   └── deepfake_model.h5
│
├── screenshots/
│
├── docs/
│   └── CyberShield_Project_Report.pdf
│
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── .env.example
├── .gitignore
└── README.md
```

---

# ⚙️ Installation

## 1. Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/CyberShield-Multimodal-Phishing-Deepfake-Detection.git
```

Move into the project directory:

```bash
cd CyberShield-Multimodal-Phishing-Deepfake-Detection
```

---

## 2. Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔐 Environment Configuration

Create a `.env` file in the project root.

```env
APP_SECRET_KEY=your_private_key

PHISHING_MODEL_PATH=models/phishing_model.pkl

DEEPFAKE_MODEL_PATH=models/deepfake_model.h5

DB_PATH=database/detections.db
```

---

# ▶️ Running CyberShield

CyberShield uses separate FastAPI and Streamlit processes.

## Start FastAPI Backend

Open your first terminal:

```bash
uvicorn api.main:app --host 0.0.0.0 --port 8000 --reload
```

Backend health check:

```text
http://localhost:8000/health
```

---

## Start Streamlit Frontend

Open another terminal:

```bash
streamlit run app/app.py
```

Open:

```text
http://localhost:8501
```

---

# 🐳 Run Using Docker

Make sure Docker and Docker Compose are installed.

Run:

```bash
docker-compose up --build
```

Then open:

```text
http://localhost:8501
```

---

# 🖥️ Application Modules

### URL Analysis

Users can submit URLs for phishing detection.

The system provides:

* Phishing probability
* Risk score
* Threat classification
* LIME explanation

### Image Analysis

Users can upload facial images for deepfake detection.

The system provides:

* Deepfake probability
* Prediction
* Threat score
* Grad-CAM heatmap

### Combined Analysis

Users can submit both:

```text
URL + Image
```

CyberShield combines both results to calculate a unified threat score.

### Detection Dashboard

The dashboard displays:

* Previous detections
* Threat statistics
* Detection history
* Visual analytics

---

# 🌐 REST API

CyberShield also exposes its detection functionality through REST APIs.

Example backend:

```text
http://localhost:8000
```

Health check:

```text
GET /health
```

URL Analysis:

```text
POST /analyze/url
```

Additional endpoints handle deepfake detection, combined analysis, explanations, statistics and detection history.

---

# 🧠 Explainable AI

One of the major goals of CyberShield is making cybersecurity predictions understandable.

### LIME

Used for explaining phishing URL predictions by identifying the most influential URL features.

### Grad-CAM

Used for explaining deepfake predictions by visualizing image regions that contributed to the model decision.

---

# 🔒 Privacy

Uploaded images are processed for inference and are not intended to be permanently stored.

Detection metadata and prediction results are logged using SQLite for dashboard analysis.

---

# 🔮 Future Improvements

Future versions of CyberShield may include:

* Audio deepfake detection
* Voice cloning / vishing detection
* Real-time video deepfake detection
* Browser extension integration
* SIEM integration
* User authentication
* Cloud deployment
* Distributed inference
* Continuous model retraining
* Advanced explainability methods

---

# 📄 Project Report

The complete academic project report is available inside:

```text
docs/CyberShield_Project_Report.pdf
```

---

# ⚠️ Disclaimer

CyberShield was developed as an academic and research-oriented cybersecurity project.

Predictions generated by the system should be treated as supplementary security indicators and should not replace professional security analysis in critical environments.

---

# 🤝 Contributions

Contributions, improvements and suggestions are welcome.

You can:

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a Pull Request

---

# ⭐ Support

If you found this project useful, consider giving the repository a **star ⭐**.

---

## CyberShield

**Machine Learning × Deep Learning × Cybersecurity × Explainable AI**

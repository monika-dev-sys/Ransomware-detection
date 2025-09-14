

# Ransomware Detection System Using Machine Learning

This project implements a Python-based ransomware detection system using honeypot techniques and machine learning. It monitors the system for ransomware-like behavior and uses a trained model to predict and block malicious activity.



## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/monika-dev-sys/ransomware-detector.git
cd ransomware-detector
````

### 2. Install Dependencies

Make sure you have Python 3.8+ installed.

```bash
pip install -r requirements.txt
```

---

## Machine Learning

### Training the Model

Run the following to generate synthetic data and train the Random Forest model:

```bash
python src/train_model.py
```

* Uses `make_classification` from `sklearn.datasets`
* Trained model is saved as `ransomware_model.pkl` using `joblib`

---

### Detection

To run detection on sample input features:

```bash
python src/detector.py
```

**Sample Output:**

```
====== Ransomware Detection ======
Input Features : [10, 0.9, 15, 50]
Prediction     : Ransomware Detected!
==================================
```

You can modify the input in `detector.py` to simulate other scenarios.

---

## Honeypot System

The `honeypot.py` script creates decoy files such as:

* `.docx`, `.jpg`, `.pdf` inside the `honeypot/` directory
* These files are monitored for unauthorized access or modification

---

## Configuration

Edit the `config.json` file to update:

* File paths
* Monitoring thresholds
* Detection sensitivity

---

## Logging

All activity and detection logs are saved in:

```
logs/activity.log
```

---

## Features

* Ransomware detection via machine learning
* Honeypot file deployment
* File system monitoring
* Process blocking (partial/planned)
* Activity logging

---

## Technologies Used

* Python 3.8+
* scikit-learn
* NumPy
* joblib
* VSCode / PowerShell for testing


---



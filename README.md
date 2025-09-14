

# Ransomware Detection System Using Machine Learning

This project implements a Python-based ransomware detection system using honeypot techniques and machine learning. It monitors the system for ransomware-like behavior and uses a trained model to predict and block malicious activity.



##Project Structure

-------------------------------------------------------------------------
├── src/
│   ├── monitor.py           # Monitors the filesystem
│   ├── honeypot.py          # Deploys honeypot files
│   ├── detector.py          # Uses trained ML model to detect ransomware
│   ├── block_process.py     # Terminates suspicious processes
│   ├── train_model.py       # Trains ML model (Random Forest)
│   ├── create_dataset.py    # Generates or prepares dataset for training
├── honeypot/
│   ├── dummy_pdf.pdf
│   ├── fake_doc.docx
│   ├── fake_photo.jpg
├── logs/
│   ├── activity.log         # System logs
├── config.json              # Configuration settings
├── requirements.txt         # Python package requirements
├── 67.js                    # (Optional) External JS - clarify usage
-----------------------------------------------------------------------

 Getting Started

1. Clone the Repository
git clone https://github.com/your-username/ransomware-detector.git
cd ransomware-detector

2. Install Dependencies

Make sure you have Python 3.8+ installed.

bash
pip install -r requirements.txt


Machine Learning

 Training the Model

Run the following to generate synthetic data and train the Random Forest model:

bash
python src/train_model.py


* Uses `make_classification` from `sklearn.datasets`
* Trained model is saved as `ransomware_model.pkl` using `joblib`

Detection

To run detection on input features:

bash
python src/detector.py
```

output

-------------------------------------------------
====== Ransomware Detection ======
Input Features : [10, 0.9, 15, 50]
Prediction     : Ransomware Detected!
==================================
--------------------------------------------------
You can modify the input in `detector.py` to simulate other scenarios.

Honeypot System

The `honeypot.py` script creates decoy files like:

* `.docx`, `.jpg`, `.pdf` in the `honeypot/` directory
* These files are monitored for access or changes



## Configuration

Edit `config.json` to set paths or thresholds for monitoring and detection logic.

Logging

All events and detections are stored in `logs/activity.log`.



 Features

* Ransomware detection via machine learning
* Honeypot file deployment
* File system monitoring
* Process blocking (planned or partially implemented)
* Activity logging

## Technologies Used

* Python 3.8+
* scikit-learn
* NumPy
* joblib
* VSCode / PowerShell for testing







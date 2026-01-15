📱 Mobile CrowdSourcing – Data Trustworthiness Analysis

This project focuses on detecting malicious and trusted users in Mobile CrowdSourcing (MCS) systems using a hybrid machine learning approach.
Mobile CrowdSourcing relies on data collected from users’ smartphones (GPS, sensors, etc.).
However, some users may submit false or low-quality data, which reduces the reliability of the system.
This project aims to identify whether a user’s data is trustworthy or malicious before it is used.

🔍 What Problem Does This Project Solve?

In Mobile CrowdSourcing systems:
Data comes from unknown and uncontrolled users
Some users may:
  Manipulate sensor values
  Submit fake or low-effort data
  Drain system resources
This leads to:
  Poor data quality
  Incorrect analysis results
  Loss of trust in MCS platforms

👉 Goal: Automatically classify users as Trusted (1) or Malicious (0) based on their data.

🧠 Key Idea of the Project

This project uses a hybrid model that combines:
1. Generative Adversarial Networks (GANs)
  Generate realistic synthetic data
  Increase data diversity
  Help the model learn better patterns

2. Random Forest Classifier
  Classifies users as trusted or malicious
  Handles large datasets efficiently
  Provides high accuracy and robustness

By combining GAN-based data augmentation with ensemble learning, the model achieves very high classification accuracy.

📊 Dataset Overview

Source: Generated using the CrowdSenSim simulation tool
Size: ~14,000 records
Features: 13 attributes including:
  Location (latitude, longitude)
  Time-based features (day, hour, minute)
  Device-related metrics (battery requirement, duration)
  Coverage and grid information

Target Variable:

1 → Trusted user

0 → Malicious user


📈 Results Summary
  Logistic Regression Accuracy: ~72%
  Random Forest Accuracy: ~99.8%
  Hybrid GAN + Random Forest Accuracy: ~99.4%

The results show that synthetic data generation significantly improves model performance and robustness.

🧪 Technologies Used
Python
Jupyter Notebook
Pandas, NumPy
Scikit-learn
TensorFlow / Keras
Matplotlib

▶️ How to Run
pip install -r requirements.txt
jupyter notebook Data_MCS.ipynb

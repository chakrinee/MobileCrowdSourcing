📱 Data Trustworthiness in Mobile Crowdsourcing

This repository contains the implementation and experimental analysis for the research project “Data Trustworthiness in Mobile Crowdsourcing”, which focuses on identifying malicious and trusted users in mobile crowd-sensing systems using a hybrid machine learning approach.

The project combines Generative Adversarial Networks (GANs) for synthetic data generation with a Random Forest classifier to improve trust prediction accuracy in mobile crowdsourced datasets.

🧠 Problem Motivation

Mobile Crowd Sensing (MCS) relies heavily on user-generated sensor data from smartphones. While this enables large-scale data collection, it also introduces challenges such as:

Malicious or unreliable user participation

Manipulated or falsified sensor readings

Reduced trust in collected data

Degraded system reliability

Ensuring data trustworthiness is critical for maintaining the integrity and usefulness of MCS applications.

🏗️ Proposed Approach

This project proposes a hybrid model that integrates:

Generative Adversarial Networks (GANs)

Generates realistic synthetic data

Enhances data diversity and robustness

Helps expose the model to a wider range of real-world scenarios

Random Forest Classifier

Classifies users as Trusted or Malicious

Provides high accuracy and interpretability

Handles large datasets and missing values effectively

The combination of GAN-based data augmentation and ensemble learning improves model performance on unseen data.

📊 Dataset Description

Source: Generated using the CrowdSenSim simulation tool

Size: ~14,000 records (~867 KB)

Attributes: 13 features including

ID, latitude, longitude, day, hour, minute, duration,
remaining time, battery requirement %, coverage,
grid number, legitimacy, on-peak hour


Target Variable:

Legitimacy = 1 → Trusted user

Legitimacy = 0 → Malicious user

Synthetic data is generated using GANs excluding the legitimacy label and later classified using the trained model.

⚙️ Methodology Overview

Dataset preprocessing and feature selection

Class imbalance handling using SMOTE

Baseline evaluation using Logistic Regression

Training a Random Forest classifier

GAN-based synthetic data generation

Combining real and synthetic datasets

Final classification using the hybrid model

📈 Experimental Results

Logistic Regression Accuracy: ~72%

Random Forest Accuracy (baseline): ~99.86%

Hybrid GAN + Random Forest Accuracy: ~99.4%

Additional evaluation includes:

Feature importance analysis

Confusion matrix

Precision, recall, and F1-score metrics

The results demonstrate that GAN-based data augmentation significantly improves robustness and prediction accuracy.

🧪 Technologies Used

Python 3.11

Jupyter Notebook

Pandas & NumPy

Scikit-learn

TensorFlow / Keras

Matplotlib / Seaborn

🚀 How to Run the Project
git clone https://github.com/chakrinee/MobileCrowdSourcing.git
cd MobileCrowdSourcing
pip install -r requirements.txt
jupyter notebook

Open the notebook from the notebooks/ directory to reproduce the experiments.


📜 License

This project is intended for academic and research purposes only.

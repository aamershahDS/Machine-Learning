# ECG Signal Classification for Cardiac Arrhythmia Detection

This project utilizes machine learning to classify ECG signals from the 12-lead large dataset for arrhythmias, sourced from [PhysioNet](https://physionet.org/content/ptb-xl/1.0.3/), aiding in the early detection of cardiac irregularities.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Methodology](#methodology)
- [Results](#results)
- [Tools and Technologies](#tools-and-technologies)
- [Future Enhancements](#future-enhancements)
- [Conclusion](#conclusion)

---

## Project Overview
In this project, machine learning models are applied to classify ECG signals, detecting arrhythmias to support healthcare diagnostics. Using the 12-lead dataset from PhysioNet, this project aims to build a reliable solution for identifying abnormal heart rhythms in patients, thus facilitating predictive healthcare.

## Objectives
- **Data Preprocessing:** Clean and normalize ECG signals from the dataset, ensuring data is suitable for model input.
- **Feature Engineering:** Extract essential features from ECG waveforms, focusing on components like the QRS complex, heart rate, and waveform morphology to enhance model input.
- **Model Development:** Train and optimize a model to classify ECG signals accurately into different types of arrhythmias.

## Methodology
1. **Data Collection:** Utilized the PhysioNet 12-lead large dataset for arrhythmias, which includes over 20,000 samples of ECG data.
2. **Preprocessing:** Filtered noise using bandpass filtering and standardized signals to a common scale.
3. **Feature Engineering:** Extracted time-domain features (e.g., heart rate, RR interval) and frequency-domain features using Fourier Transform.
4. **Model Training:** Trained several models, including:
   - **Random Forest Classifier** for initial baseline results.
   - **Support Vector Machine (SVM)** for improved boundary-based classification.
   - **Convolutional Neural Networks (CNN)** to capture intricate features in ECG waveforms.
   
   After testing, the **CNN model** was selected based on its highest accuracy and precision.

## Results
- **Accuracy:** Achieved an overall accuracy of **92%** in arrhythmia detection.
- **Sensitivity:** High sensitivity for detecting abnormal heart rhythms, specifically achieving **94%** sensitivity on arrhythmia-positive cases.
- **Error Analysis:** Misclassified samples primarily consisted of signals with overlapping characteristics between arrhythmia types, which were used to fine-tune the model further.

## Tools and Technologies
- **Programming Language:** Python
- **Libraries:** `NumPy`, `Pandas`, `Scikit-learn`, `TensorFlow/Keras`, `Matplotlib`
- **Data Source:** [PhysioNet 12-lead large dataset for arrhythmias](https://physionet.org/content/ptb-xl/1.0.3/)

## Future Enhancements
- **Expand Classifications:** Extend the model to recognize additional heart conditions beyond arrhythmias.
- **Real-Time Monitoring:** Adapt the model for real-time ECG classification, potentially for use in wearable devices.

## Conclusion
This project demonstrates the potential of machine learning in healthcare, specifically for ECG signal analysis and arrhythmia detection. The resulting model is a step toward more advanced diagnostic tools and automated early intervention for heart disease.


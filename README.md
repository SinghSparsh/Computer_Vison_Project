﻿# Real-Time Distracted Driver Behaviour Detection Using Computer Vision and Deep Learning Techniques

 # Introduction
Distracted driving is one of the leading causes of motor vehicle accidents and fatalities globally. With the increasing use of smartphones and other distractions in vehicles, drivers often lose focus, resulting in catastrophic accidents. Currently, most vehicles lack advanced systems to monitor the driver's behavior and provide timely warnings if they are distracted, fatigued, or drowsy.

This project aims to develop a Distracted Driving Detection System using computer vision techniques, capable of identifying and mitigating instances of distraction in real-time by analyzing visual cues of the driver’s behavior, such as using a smartphone, drowsiness, or engaging in non-driving-related activities.

#Problem Statement

Driving is a task that demands high levels of concentration. Distractions such as phone usage, drowsiness, eating, or even engaging in conversations while driving can lead to fatal accidents. Despite these risks, most vehicles do not have systems to monitor driver behavior and prevent accidents caused by distractions.

The problem at hand is to develop a robust and accurate real-time system that detects instances of distracted driving. The system will analyze the driver’s behavior through visual input, identifying common distractions and issuing timely warnings or interventions to prevent accidents.

# Objectives

Accurate Detection: Build a reliable system that can detect various forms of distraction, including smartphone use, drowsiness, and non-driving activities.
Real-Time Monitoring: Ensure the system works in real-time, providing immediate feedback to the driver.
Scalable Solution: Develop a solution that can be easily integrated into modern vehicles or external monitoring systems.

# Dataset
We used custom diverse  dataset containing driver behaviors captured in realtime  through images to train the distracted driving detection model. The dataset includes various common distracted behaviors such as:

Phone Use (texting, talking)
Drowsiness (eye closure, yawning)
Reaching for Objects
Looking Around (not focusing on the road)

Key Dataset Characteristics:
Classes: Different distraction categories, such as normal driving, phone use, etc.
Images/Frames: Captured in real-time to mimic real-world scenarios.
Annotations: Labeled data indicating the driver’s activity in each frame.

# Challenges
Developing an effective distracted driving detection system presents several challenges:

Real-Time Processing: The system must process visual data in real-time without causing delays.
Variability in Driver Behavior: Drivers exhibit different behavior patterns, which makes it difficult to generalize a single model to all cases.
Lighting and Environmental Conditions: Lighting changes (day/night), weather, and other conditions can affect the accuracy of visual recognition systems.
False Positives: Minimizing false positives is crucial for an effective warning system.

# Approach and Methodology
To tackle the problem of distracted driving detection, we followed a comprehensive machine learning and computer vision pipeline:

1. Data Collection and Preprocessing
Collected and labeled a dataset consisting of driver images or video frames.
Preprocessed the data by resizing and normalizing the images.
Augmented the dataset with techniques like rotation, flipping, and brightness adjustment to account for different environmental conditions.
2. Feature Extraction
Using Google Mediapipe Holistic or OpenCV, we extracted key facial and body landmarks that serve as input features for distraction detection. This allowed us to:

Track eye movements (for drowsiness detection).
Track hand and head positions (to detect phone use or looking away from the road).
Dimensionality reduction techniques like Principal Component Analysis (PCA) were applied to reduce the complexity of the extracted features, while retaining relevant information for model training.

3. Model Training
We experimented with various machine learning models for distracted driving detection:

Convolutional Neural Networks (CNNs): For image classification tasks.
Multilayer Perceptrons (MLP) and Artificial Neural Networks (ANN): For predicting distractions based on extracted features.
Ensemble Techniques: Combining multiple models like Random Forest and K-Nearest Neighbors to improve accuracy and generalization.
4. Real-Time Detection
The trained model was integrated into a real-time detection system using video streaming or live camera input. OpenCV and Python’s VideoCapture library were used to capture and process video frames in real-time, analyzing driver behavior and raising warnings when distractions were detected.

# Technologies Used
The following technologies and libraries were utilized in this project:

Python: The core programming language.
OpenCV: For real-time video processing and image analysis.
Mediapipe: For extracting facial and body landmarks.
TensorFlow/Keras: For building and training deep learning models.
Principal Component Analysis (PCA): For dimensionality reduction.
Scikit-learn: For traditional machine learning models and evaluation metrics.
Ensemble Techniques: To combine the strengths of multiple models.

# Results
The system was able to successfully detect distracted driving behaviors with high accuracy. Key metrics include:

Accuracy: Achieved up to 98% accuracy in detecting distracted driving activities across various test cases.
Real-Time Performance: The system was able to process video frames at real-time speeds (~30 frames per second), with minimal latency.
False Positive Rate: Maintained a low false positive rate to avoid unnecessary driver interventions.
Performance Summary:
Model	Accuracy (%)	Precision	Recall	F1 Score
Convolutional Neural Network (CNN)	98%	0.97	0.96	0.97
Random Forest	94%	0.93	0.91	0.92
K-Nearest Neighbors (KNN)	92%	0.91	0.89	0.90
Conclusion
This project demonstrates the effectiveness of combining computer vision and machine learning techniques to create a real-time distracted driving detection system. By analyzing visual cues like head movement, hand positioning, and eye-tracking, the system can accurately detect distracted behaviors such as smartphone use, drowsiness, and other activities that divert the driver’s attention from the road.

The system's real-time capabilities allow it to warn drivers immediately, thereby helping to reduce the likelihood of accidents caused by distracted driving.

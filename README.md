Depression Detection by Analyzing EEG Signals Using CNN
Project Overview
Depression is a serious mental health condition that affects millions of people worldwide. Traditional methods of diagnosing depression rely on self-reported symptoms and clinical evaluations, which can sometimes lead to misdiagnoses. Recent advancements in neuroscience and artificial intelligence have enabled the use of EEG (Electroencephalography) signals to analyze brain activity and detect signs of depression.

In this project, I developed a Convolutional Neural Network (CNN)-based approach to classify EEG signals into two categories:

Major Depressive Disorder (MDD) patients
Healthy individuals
The primary goal of this project is to demonstrate that CNNs can be as effective as other state-of-the-art methods when analyzing EEG signals for depression detection. By leveraging deep learning, we can potentially enhance the accuracy, efficiency, and automation of depression diagnosis, reducing reliance on subjective clinical evaluations.

Dataset and Preprocessing
Data Source and Format
The dataset used in this project consists of EEG recordings collected in EDF (European Data Format), a standard format for storing physiological signals. The dataset link is provided in "Dataset.txt".

Data Collection and Processing Steps
EEG Data Acquisition: The dataset was obtained from an open-access EEG database consisting of recordings from individuals diagnosed with Major Depressive Disorder (MDD) and healthy control subjects.
Data Categorization: The dataset was separated into two groups:
MDD Data: EEG signals from individuals diagnosed with Major Depressive Disorder.
Healthy Data: EEG signals from individuals without any known depressive disorder.
Signal Visualization: Each EEG recording was analyzed to generate graphical representations of brain activity. These graphs were stored in two respective folders:
"MDD" folder (for EEG signals of depressed patients)
"Healthy" folder (for EEG signals of non-depressed individuals)
Preprocessing Steps:
Converted EDF files into a structured format for CNN training.
Applied noise filtering and normalization techniques to enhance signal quality.
Split the data into training, validation, and test sets to ensure a robust evaluation.
The preprocessing scripts and raw EEG data can be found in the "Data Read" folder.
Depression Detection Process Using CNN
1. Baseline CNN Model
To begin with, I built a basic CNN model to test the feasibility of using deep learning for EEG-based depression detection.

Initially, I trained a standard CNN architecture using raw EEG signal data.
I then introduced data augmentation techniques to examine their impact on model performance.
The baseline CNN model helped establish a benchmark accuracy, which was later improved with advanced architectures.
2. Experiments with Pre-Trained CNN Models
To explore the effectiveness of CNNs in EEG signal classification, I tested several pre-trained deep learning models available in Keras Applications, including:

VGG16
ResNet50
MobileNet
Xception
EfficientNet
Each model was fine-tuned to optimize its performance for EEG classification. The results were systematically recorded to compare accuracy, training time, and computational efficiency.

The implementations of these models can be found in the "Keras Application Models" folder.

Custom CNN Model for EEG-Based Depression Detection
1. Architecture Design
After evaluating multiple pre-trained CNN architectures, I designed a custom CNN model tailored specifically for EEG signal classification. The model was optimized to extract key features from EEG signals while maintaining computational efficiency.

The custom CNN architecture includes:

Multiple convolutional layers with ReLU activation to extract spatial features.
Batch normalization to stabilize training and improve generalization.
Dropout layers to prevent overfitting.
Fully connected layers for classification.
Softmax activation function to output class probabilities (MDD vs. Healthy).
2. Performance Evaluation
After rigorous testing, my custom CNN model achieved the highest accuracy among all tested models, demonstrating its effectiveness in EEG-based depression detection. The final model and training scripts are available in the "My Custom Model" folder.

Conclusion and Future Scope
This project demonstrates that CNNs can effectively analyze EEG signals to detect depression, making them a viable alternative to traditional clinical methods.

Key Takeaways:
EEG signals provide valuable insights into brain activity patterns associated with depression.
CNN-based deep learning models can automatically extract key features from EEG signals, improving diagnostic accuracy.
A custom CNN model can outperform pre-trained models when optimized for EEG signal classification.
Future Enhancements:
Integrating More EEG Channels: Expanding the dataset to include multi-channel EEG recordings for improved accuracy.
Real-Time Depression Monitoring: Developing a real-time system for depression detection using wearable EEG devices.
Hybrid Deep Learning Models: Combining CNNs with LSTMs or Transformer models to capture both spatial and temporal dependencies in EEG signals.
This research has the potential to significantly contribute to the field of AI-driven mental health diagnostics, paving the way for automated, early-stage depression detection using deep learning.
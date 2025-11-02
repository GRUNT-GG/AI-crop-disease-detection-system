🌱 AI-BASED PLANT DISEASE RECOGNITION SYSTEM
⭐ Project Overview
This project implements a highly accurate and efficient AI-Based Plant Disease Recognition System 1to address the Agricultural Detection Gap 2222—the delay between infection and intervention. By leveraging Transfer Learning (TL) 33and the optimized EfficientNetB4 architecture 44, the system provides rapid, objective diagnosis for 39 distinct disease and healthy states across multiple crops5555555.

💻 Technical Stack and Setup
The project is anchored in TensorFlow/Keras and utilizes a Google Colab/GPU environment for accelerated training.

1. Dependencies
 The key libraries include:
 TensorFlow/Keras
 EfficientNet
 Python 102.
 Data Integrity and Pipeline
 The system was designed for multi-class classification with 39 distinct labels
 Data was subjected to a stratified split to ensure the ratio of classes was maintained across the training, validation, and test sets
 The pipeline was optimized using the .cache().prefetch(buffer_size=AUTOTUNE) sequence to drastically reduce I/O wait times
 Input images are standardized to 160 x 160 times

🧠 Model Architecture and Training

The core solution utilizes Transfer Learning with the EfficientNetB4 base, which prioritizes high parameter efficiency
1. Model Construction
 Base Model: EfficientNetB4 was instantiated with pre-trained 'imagenet' weights

Classification Head: Built using the Functional API 17, including a GlobalAveragePooling2D layer (for robustness against feature location variations) and a final Dense prediction layer sized to 39 units

🚀 Deployment and Future Utility

The project successfully developed a scalable, high-utility diagnostic model21. The MVP was demonstrated on a web interface called PHASAL
Final Utility: Provides diagnosis (e.g., "Apple_Black_rot"), identifies the causal pathogen, and delivers direct, actionable treatment recommendations
Future Scope: Focuses on converting the model to TFLite via 8-bit quantization for Mobile/Edge Deployment 24242424, implementing Localization (Segmentation) to calculate Disease Severity Index (DSI) 25, and developing an Integrated Agricultural Marketplace.

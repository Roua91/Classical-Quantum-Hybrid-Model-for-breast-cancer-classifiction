# Hybrid Classical-Quantum Model for Breast Cancer Detection

Breast cancer is one of the most common and deadly cancers affecting women worldwide, making early and accurate detection crucial for effective treatment. Machine learning and deep learning techniques have made significant progress in medical image analysis, particularly in classifying breast cancer from ultrasound images. However, these methods can struggle with the complexity and size of medical datasets. Quantum computing, which offers a new way to handle and process large amounts of data more efficiently, could be a game-changer in this field.

In this project, we explore how **hybrid quantum transfer learning** can enhance the classification of breast cancer from ultrasound images. Our approach involves combining a classical deep learning model (ResNet50) with different types of quantum circuits. By integrating quantum computing into traditional transfer learning, we aim to improve the model's accuracy and performance in handling complex data.

The project uses four main models:

1. **[ResNet50 (Conventional Transfer Learning)](https://github.com/Roua91/Classical-Quantum-Hybrid-Model-for-breast-cancer-classifiction/blob/main/ResNet50_97%25.ipynb)**:  
   A pre-trained deep learning model that has proven effective in feature extraction for various image classification tasks. This model serves as the baseline for comparing quantum-enhanced models.  
   - **Accuracy**: 97.69%  
   - **Computational Efficiency**: Most efficient model in terms of resource usage.

2. **[Q1: Simple Quantum Circuit (SQC)](https://github.com/Roua91/Classical-Quantum-Hybrid-Model-for-breast-cancer-classifiction/blob/main/Q1_Hybrid_model_94%25.ipynb)**:  
   This model uses a basic quantum circuit with a Hadamard gate to create a superposition state, followed by rotations on the Y-axis to encode input data. The goal of this model is to explore how simple quantum operations can improve classification accuracy.  
   - **Accuracy**: 94.62%  
   - **Computational Efficiency**: Moderate efficiency, slower than ResNet50.

3. **[Q2: Entangled Quantum Circuit (EQC)](https://github.com/Roua91/Classical-Quantum-Hybrid-Model-for-breast-cancer-classifiction/blob/main/Q2_Hybrid_model_97%25.ipynb)**:  
   In addition to the Hadamard gate and Y-axis rotations, this model includes a C-NOT gate to create entanglement between qubits. The EQC introduces more complex quantum interactions, aiming to improve the model's learning capabilities.  
   - **Accuracy**: 96.92%  
   - **Computational Efficiency**: More resource-intensive than ResNet50, but offers a good balance of performance and accuracy.

4. **[Advanced Quantum Circuit (AQC)](https://github.com/Roua91/Classical-Quantum-Hybrid-Model-for-breast-cancer-classifiction/blob/main/Q3_Hybrid_model_95%25.ipynb)**:  
   This model takes the EQC further by adding phase shift gates and controlled-Z gates to explore deeper quantum state spaces and create more intricate entanglement patterns. The goal is to see if these more complex quantum operations lead to better performance.  
   - **Accuracy**: 95.38%  
   - **Computational Efficiency**: The most resource-intensive model, but still less accurate than EQC.


### Objectives of the Study

1. **To compare and evaluate the effectiveness of quantum transfer learning against conventional transfer learning** for classifying breast cancer on ultrasound images.
   
2. **To identify the most effective quantum circuit design** for this classification task, exploring the impact of different quantum architectures like SQC, EQC, and AQC.

3. **To analyze the models' performance** in terms of accuracy, sensitivity, specificity, and computational resource efficiency.


### Final Results
The results of the study show that integrating quantum circuits into transfer learning models can improve classification accuracy. The **Entangled Quantum Circuit (EQC)** stood out as the best-performing quantum model, achieving higher accuracy than both the Simple Quantum Circuit and the Advanced Quantum Circuit. However, the **ResNet50** model remained the most computationally efficient, making it the best choice for situations where computational resources are limited.

Overall, this project highlights the potential of quantum-enhanced models in medical data analysis, particularly in improving breast cancer detection from ultrasound images. While quantum computing offers promising improvements in accuracy, traditional models like ResNet50 still hold advantages in terms of speed and resource use.


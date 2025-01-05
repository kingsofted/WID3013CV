# **Predictive X-Ray Classification Using AI**

---

## **Table of Contents**  
1. [Introduction](#introduction)  
2. [Abstract](#abstract)  
3. [Methodology](#methodology)  
4. [Results](#results)  
5. [Discussion](#discussion)  
6. [Conclusion](#conclusion)  
7. [References](#references)  

---

## **1. Introduction**  
- Implementation of multi-disease classification for chest X-rays
- Based on DenseNet201 architecture
- How AI increase the efficieny of doctors


---

## **2. Abstract**  


---

## **3. Methodology**  

### **Dataset**  
- **Source**: Kaggle dataset curated by Omkar Manohar Dalvi.  
- **Classes**:  
  - Bacterial Pneumonia  
  - COVID-19  
  - Tuberculosis  
  - Viral Pneumonia  
  - Normal  
- **Splits**: Training (6054), Validation (2016), Testing (2025).  
- **Data Augmentation**: Techniques like zoom and shift transformations were applied to ensure robust training.

### **Model**  
- **Architecture**: DenseNet201 pre-trained on ImageNet, with additional dense layers tailored for classification tasks.  

---

## **4. Results**  


---

## **5. Discussion**  

### 5.1 Interpretation of Results
The DenseNet201-based model demonstrated strong learning capabilities, as evidenced by a consistent decrease in training loss across epochs. Validation accuracy stabilized between **87% and 89%**, indicating robust generalization despite mild overfitting, as suggested by the gap between training and validation metrics. The test accuracy of approximately **84%**, alongside a test loss of **0.41**, closely aligns with validation trends, reinforcing the model's stability.

Confusion matrix analysis shows high accuracy for classes such as **“Normal,” “Tuberculosis,”** and **“Corona Virus Disease”** but highlights misclassifications between **“Bacterial Pneumonia”** and **“Viral Pneumonia”**, likely due to similar visual features. The classification report supports this trend, with high precision and recall for **“Corona Virus Disease” (89%)**, moderate values for **“Viral Pneumonia” (79%)**, and lower precision and recall for **“Tuberculosis” (65%)**, attributed to class imbalance or limited representation. The weighted average **F1-score of 84%** corroborates the model's overall strong performance.

---

### 5.2 Limitations
Despite promising results, this study has notable limitations:
- **Class-Specific Feature Diversity**: Limited variability in **“Tuberculosis”** images restricts the model's ability to generalize effectively to diverse cases.
- **Class Overlap**: Significant misclassifications between **“Bacterial Pneumonia”** and **“Viral Pneumonia”** stem from overlapping visual features, such as lung infiltrates, making these classes challenging to differentiate.
- **Dataset Quality**: Some images in the dataset suffer from low quality or improper cropping (e.g., partial lung views), introducing noise and hindering learning.
- **Class Imbalance**: The lower precision and recall for **“Tuberculosis” (65%)** may result from limited intra-class variations in the dataset.
- **Potential Data Leakage**: There is no explicit verification of patient data separation between training and validation sets, which could impact result validity.

---

### 5.3 Potential Improvements
To address these limitations and further enhance performance:
1. **Advanced Data Augmentation**:
   - Incorporate rotation, scaling, and flipping to increase variability and improve generalizability.
2. **Modern Architectures**:
   - Explore state-of-the-art models like **EfficientNet** or optimized **DenseNet** variants for better feature extraction and classification.
3. **Comprehensive Metrics**:
   - Introduce **ROC curves** and **AUC** to provide deeper performance insights and evaluate model capabilities across all classes.
4. **Dataset Enhancements**:
   - Focus on curating a high-quality dataset with diverse and representative samples to reduce misclassifications and improve learning.


---

## **6. Conclusion**  
This paper discusses experiments performed with a DenseNet201-based architecture to detect various lung problems: bacterial pneumonia, viral pneumonia, COVID-19, and tuberculosis. The baseline model of ResNet-50 has been documented to have a better performance compared to the SVM with VGG16 features, and a standalone CNN as ResNet-50 had higher accuracy and macro F1-score.

The DenseNet201 based model has performed well for classes such as ‘Normal’, ‘Tuberculosis’ and ‘Corona Virus Disease’ with a high degree of accuracy.  However, there is misclassification observed between ‘Bacterial Pneumonia’ and ‘Viral Pneumonia’. 

In future area of improvement, data augmentation techniques can be implemented to increase variability of the dataset for generalization purposes. Other architectures like EfficientNet and DenseNet can also be used to improve classification performance. Using other evaluation metrics such as ROC curves and area under the curves can be used to gain detailed insights on the model’s ability to predict each class.

---

## **7. References**  
1. [Omkar Manohar Dalvi, Kaggle X-ray Dataset](https://www.kaggle.com/datasets/omkarmanohardalvi/lungs-disease-dataset-4-types/data) 
2. [DenseNet201: A Convolutional Neural Network for Feature Extraction](https://arxiv.org/abs/1608.06993)  
3. [TensorFlow Documentation: Advanced Model Building](https://www.tensorflow.org/guide/keras/functional)  
4. [Flask and MySQL Integration for Scalable Web Applications](https://flask.palletsprojects.com/en/2.3.x/tutorial/database/)

---

For further details, consult the [ICIP 2024 Submission Guidelines](https://icip2024.org).

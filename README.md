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

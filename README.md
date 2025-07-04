# 🌿 PlantDiseaseClassification

This project aims to automatically detect diseases on plant leaves using image classification techniques. Deep learning methods and transfer learning approaches were used to classify plant diseases from visual data.

---

## 🎯 Project Objective

Timely detection of plant diseases, which are common in agriculture, is crucial for crop productivity and agricultural sustainability. This project aims to develop an AI system that classifies plant diseases based on leaf images.

---

## 🗂️ Dataset Used

- **Dataset Source:** [PlantVillage Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease)  
- The dataset includes various disease types and healthy leaves.  
- Images from 4 different classes were used.  
- All images were resized and normalized before training.

---

## 🔧 Implementation Steps

1. **Data Preparation:**
   - Images were split into `train`, `validation`, and `test` sets.  
   - All images were resized for compatibility with the models.  
   - Data augmentation was applied using `ImageDataGenerator`.

2. **Modeling:**
   - Three different models were used:
     - **Custom CNN:** A model designed from scratch  
     - **VGG16 (Transfer Learning):** Pretrained deep learning model  
     - **EfficientNetB0 (Transfer Learning):** Faster training with fewer parameters  
   - For each model, the `Adam` optimizer and `categorical_crossentropy` loss function were used.

3. **Training Process:**
   - Models were trained on `Google Colab` using GPU support.  
   - Epochs, batch sizes, and learning rates were optimized per model.  
   - Loss and accuracy values were monitored throughout training.

4. **Evaluation:**
   - Training and validation accuracies were compared to monitor overfitting.  
   - Confusion matrix and class-based performance metrics were analyzed.

---

## 🧰 Libraries Used

- Python  
- TensorFlow / Keras  
- OpenCV  
- Matplotlib, NumPy  
- Scikit-learn

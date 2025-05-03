# BME450 Project

## Title
**Bone Fracture Detection in X-ray Images using Convolutional Neural Networks**

## Team Members
- Alison Mae Steele (ams0925)
- An My Nguyen (anmynguyen)
- Dana Titus (dtitus03)

## Project Description

We implemented and compared several convolutional neural network (CNN) architectures for binary classification of X-ray images as either *fractured* or *not fractured*.

### Dataset
We used the **Bone Fracture Multi-Region X-Ray Data** dataset from Kaggle, which contains 10,580 labeled images organized into training, validation, and test folders. The images were already rotated in some cases, reducing the need for additional data augmentation. All images were converted to grayscale and resized to 224×224 or 28×28 depending on the model architecture.

---

## Files

- `1_Layer_CNN.ipynb`  
  Implements a simple 1-layer CNN trained on a small subset (100 training/testing images). Used to observe model behavior on limited data. Accuracy stayed around 50%, indicating the model did not learn meaningful features.

- `2_Layer_CNN.ipynb`  
  Defines and trains a 2-layer CNN using both a partial dataset and the full dataset. This model showed strong generalization with test accuracy reaching 98% on the full dataset.

- `Res_net18_.ipynb`  
  Fine-tunes a pretrained ResNet-18 model for the binary classification task. Performance was strong (test accuracy ~92%), but the model showed a wider train-test loss gap, suggesting less generalization than the 2-layer CNN.

---

Each notebook is mostly self-contained and typically includes:
- Data loading and preprocessing
- Model definition
- Training and evaluation loops
- Accuracy/loss visualization
- Final evaluation via ROC curve 

> **Note:**  
> The `1_layer_cnn.ipynb` file does not include the final evaluation steps due to the model's limited performance and use of a very small dataset. It was intended as an initial exploration of learning behavior on limited data.


## Summary
The 2-layer CNN provided the best balance between simplicity, speed, and performance. While ResNet-18 offered high accuracy, it did not significantly outperform the custom model and was more sensitive to data quality. The 1-layer CNN was unable to learn effectively on small datasets.


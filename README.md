# BME450-project


# Title
Bone fracture detection in X-ray images

# Team members
Alison Mae Steele (ams0925), An My Nguyen (anmynguyen), Dana Titus (dtitus03)

# Project description

a. Dataset: MURA Bone X-ray Dataset by Stanford Machine Learning Group  
https://stanfordaimi.azurewebsites.net/datasets/3e00d84b-d86e-4fed-b2a4-bfe3effd661b

b. Basic version: 
 - Objective: Start with small subset of 10-30 X-ray images manually selected from the MURA dataset
 - Task: Build a simple 3-layer CNN to classify images as fracture (abnormal) or normal
 - Focus areas: 
    - Preprocessing – resize and normalize grayscale images
    - Model understanding – evaluate early training behavior (overfitting, loss curves, etc.) with such a small dataset
    - Baseline comparison – optionally compare CNN results with a baseline logistic regression model using image flattening 

c. Advanced version: 
 - Dataset scale: Use a larger portion of the dataset – hundreds of images covering multiple body parts (e.g. wrists, elbows, fingers)
 - Enhancements:
   - Implement data augmentation (rotations, flips, contrast adjustments) to improve generalization
   - Introduce transfer learning using a pre-trained model (e.g. ResNet50) fine-tuned on X-ray data
   - Apply Grad-CAM or heatmaps to visualize the model’s focus areas when predicting fractures
   - 
  - Optionally, explore multi-label classification if distinguishing different types of fractures (if labeled appropriately) 

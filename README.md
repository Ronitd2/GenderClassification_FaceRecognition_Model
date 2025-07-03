# Gender Classification & Face Matching

This project addresses two core facial analysis tasks :

##  Task A: Gender Classification

A binary classification task where the model learns to predict whether a given face image belongs to a **male** or **female**. The dataset is divided into training and validation sets, with each image labeled accordingly.

**Goal:** 
Train a model that accurately classifies gender from face images, focusing on **accuracy**, **generalization**, and **fairness**.



## Task B: Face Matching (Verification) 

A face **verification** task where the objective is to determine if a given distorted face image matches a known identity.

- Each identity has one or more clean reference images.
- Distorted test images must be matched to these identities.

**Goal:**  
Build a system that determines whether a distorted image:
-  **Positively matches** a known identity (`label = 1`)
-  **Does not match** any known identity (`label = 0`)

This task requires handling distortions and generalizing to identities not seen during training.

---
## Task-A Details
## Gender Classification - ResNet50 with PyTorch

This project implements a deep learning model for binary gender classification using facial images. The goal is to classify faces as either male or female.

### Overview

- The model is built using **PyTorch** and leverages a **pretrained ResNet50** architecture from torchvision.
- Only the fully connected (FC) layers are fine-tuned; the rest of the model's parameters are frozen to speed up training and prevent overfitting.
- The final classification layer is replaced with a custom head tailored for binary output (2 classes).

### Data Handling

- Training and validation data are loaded using PyTorch's `ImageFolder` and `DataLoader`.
- Images are augmented using transformations like resizing, normalization, horizontal flipping, and color jittering to improve generalization.
- The model is trained and validated on separate datasets to monitor performance.

### Training

- The model is optimized using the **Adam optimizer** and **cross-entropy loss**.
- Training is conducted over multiple epochs, with metrics like accuracy and loss reported for both training and validation sets.
- After training, evaluation is performed using classification reports and a confusion matrix.

### Evaluation Results

- **Accuracy:** 92%
- **Precision:** 91%
- **Recall:** 92%
- **F1-Score:** 91%

### Technologies Used

- Python
- PyTorch
- torchvision
- scikit-learn (for evaluation)
- seaborn & matplotlib (for visualization)



# Gender Classification & Face Matching

This project addresses two core facial analysis tasks using machine learning:

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


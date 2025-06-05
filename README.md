# Rice Leaf Disease Classification with Deep Learning

This project focuses on classifying rice leaf diseases using four pre-trained Convolutional Neural Network (CNN) models via transfer learning: **MobileNet**, **Xception**, **VGG16**, and **VGG19**. The implementation is done using Keras and TensorFlow, and performance is compared using multiple evaluation metrics.

## Dataset

The dataset used in this project was obtained from Kaggle:

** Dataset:** 
[Rice Leaf Disease Image Dataset – Kaggle](https://www.kaggle.com/datasets/nirmalsankalana/rice-leaf-disease-image)

- Total Images: 5,932  
- Image Format: RGB, 224x224 resolution  
- Classes:  
  - Bacterial Blight  
  - Blast  
  - Brown Spot  
  - Tungro  

The dataset was split into 80% training and 20% testing with balanced class distributions.

## Models Used

The following pre-trained CNN architectures were fine-tuned using transfer learning:

- MobileNet  
- Xception  
- VGG16  
- VGG19  

Each model's top layers were customized with a Flatten layer, Dense layers, and Dropout, followed by a 4-class softmax output.

## Training Details

- All models trained for **16 epochs**  
- Average training time per model: ~24 minutes on **NVIDIA A100 GPU**  
- Loss Function: `categorical_crossentropy`  
- Optimizer: `Adam`  
- Techniques used: Data Augmentation, EarlyStopping, ModelCheckpoint

## Evaluation Results

| Model     | Accuracy | Precision | Recall | F1-Score |
|-----------|----------|-----------|--------|----------|
| MobileNet | 0.998312 | 0.998315  | 0.998312 | 0.998312 |
| Xception  | 0.989030 | 0.989180  | 0.989030 | 0.989051 |
| VGG16     | 0.891983 | 0.891576  | 0.891983 | 0.891583 |
| VGG19     | 0.859072 | 0.857220  | 0.859072 | 0.857707 |

## Visualizations

- Accuracy & loss graphs for training and validation sets are located in the `plots/` folder.
- Additional visualizations include class-wise performance and confusion matrices.

## Contact
İlhan Emre Adak
Bursa Technical University – Computer Engineering
adak.ie@hotmail.com

Berkan Parlak
Bursa Technical University – Computer Engineering
parlakberkanz@gmail.com


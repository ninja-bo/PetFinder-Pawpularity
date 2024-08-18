# PetFinder-Pawpularity
## 1. Description
###  Objective
The primary goal of this project is to develop a deep learning model that can predict the "Pawpularity" score of pet images. Pawpularity is a metric used by PetFinder.my to gauge the appeal of a pet's photo to online browsers, which can influence the pet's chances of adoption.
```
Training set size: 9912
Test set size: 8

Dataset Info:
Data columns (total 14 columns):
 #   Column         Non-Null Count  Dtype 
---  ------         --------------  ----- 
 0   Id             9912 non-null   object
 1   Subject Focus  9912 non-null   int64 
 2   Eyes           9912 non-null   int64 
 3   Face           9912 non-null   int64 
 4   Near           9912 non-null   int64 
 5   Action         9912 non-null   int64 
 6   Accessory      9912 non-null   int64 
 7   Group          9912 non-null   int64 
 8   Collage        9912 non-null   int64 
 9   Human          9912 non-null   int64 
 10  Occlusion      9912 non-null   int64 
 11  Info           9912 non-null   int64 
 12  Blur           9912 non-null   int64 
 13  Pawpularity    9912 non-null   int64 

Image Dimensions:
Image 1: (405, 720)
Image 2: (1032, 774)
Image 3: (720, 960)
Image 4: (405, 720)
Image 5: (540, 960)

Unique values in categorical columns:
Subject Focus: [0 1]
Eyes: [1 0]
Face: [1 0]
Near: [1 0]
Action: [0 1]
Accessory: [0 1]
Group: [1 0]
Collage: [0 1]
Human: [0 1]
Occlusion: [0 1]
Info: [0 1]
Blur: [0 1]
```

## 2. EDA
![alt text](image/infra.png)
![alt text](image/output.png)
![alt text](image/output-1.png)
![alt text](image/output-2.png)
![alt text](image/output-3.png)
![alt text](image/output-4.png)

## 3 Architecture
- Convolutional Neural Network (CNN) from scratch
- Transfer Learning model using a pre-trained network (e.g., ResNet50)

## 4. Results and Analysis
### 1. Hyperparameter Tuning
![alt text](image-5.png)
Best CNN trial:
  Value: 21.669536590576172
  Params:
    learning_rate: 2.5177669031357237e-05
    batch_size: 32
    num_epochs: 8
    dropout_rate: 0.17956545378570424
![alt text](image-6.png)
Best ResNet trial:
  Value: 20.27841567993164
  Params:
    learning_rate: 0.000837612197307521
    batch_size: 32
    num_epochs: 17
    dropout_rate: 0.1917737187153449
![alt text](image-7.png)
CNN - Best RMSE: 21.6695, Trial: 4
ResNet - Best RMSE: 20.2784, Trial: 5
CNN - Mean RMSE: 27.1082, Std Dev: 7.2910
ResNet - Mean RMSE: 22.4523, Std Dev: 1.2425

## 5. Conclusion
### Key Findings:
- Model Development: Implemented two distinct neural network architectures:
- Hyperparameter Optimization: Utilizing Optuna
- Performance Metric: Focused on minimizing the Root Mean Square Error (RMSE)
### Future Improvements:
- Ensemble Methods: Combining predictions from multiple models could potentially improve overall performance.
- Advanced Architectures: Exploring more recent neural network architectures like - EfficientNet or Vision Transformers might yield even better results.
- Cross-Validation: Implementing k-fold cross-validation could provide a more robust estimate of the model's performance and generalization ability.

## 6. Submission
github: https://github.com/ninja-bodhi/PetFinder-Pawpularity/tree/main
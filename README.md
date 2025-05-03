# MAGIC GAMMA TELESCOPE IMAGE CLASSIFICATION 





## Context

The MAGIC Gamma dataset originates from observations made by the MAGIC (Major Atmospheric Gamma Imaging Cherenkov) telescope, which detects gamma rays in the TeV range. The dataset was developed to classify signals into gamma signals (signal) and hadron-induced signals (background). Gamma signals correspond to electromagnetic showers caused by gamma rays, while background signals arise from hadronic cosmic rays, which create more complex showers.
![](https://github.com/celinexe/Magic_telescope_image_classification/blob/main/images/detection.png)



### Feature Extraction  

This dataset is extracted from Kaggle: https://www.kaggle.com/datasets/abhinand05/magic-gamma-telescope-dataset


The dataset contains 11 features derived from Cherenkov light images captured during atmospheric showers. These features quantify properties of the image shape and energy distribution in the Cherenkov camera.

Key features include:
* Size: Total light intensity (photons) in the image.
* Width & Length: Shape descriptors of the shower image (major and minor axes).
* Asymmetry: Degree of skewness in the light distribution.
* Distance: Distance from the shower axis to the center of the camera.
* Concentration: Ratio of light intensity in the core of the image.
* Leakage: Light fraction that leaks outside the camera's field of view.
* Usage for Classification

![](https://github.com/celinexe/Magic_telescope_image_classification/blob/main/images/Parameters.png)

Gamma and hadron showers produce distinct Cherenkov light patterns:
* Gamma Signals: These are more compact and symmetrical due to their electromagnetic nature.
* Hadron Signals: More elongated, irregular, and asymmetrical due to their hadronic nature.

![](https://github.com/celinexe/Magic_telescope_image_classification/blob/main/images/hadron_VS_gamma_shower.jpg)

  
The extracted features are fed into machine learning models to classify events as either signal (gamma) or background (hadron). By learning the patterns in the features, the model can distinguish the nature of incoming cosmic rays, improving the accuracy of gamma-ray detection in astrophysical studies.

## Quick Overview 

This dataset was almost already cleaned prior to analysis. After conducting a quick Exploratory data analysis (EDA)- including examining the correlation map between each features and selecctionning the most relevant features for training the futur models- I decided to build 5 different models. 

It includes:
- K-Nearest Neighbors
- Logistic Regression
- Decision tree
- XGboost
- Neural Network

For each model, I tried to optimize performance either by adjusting the model's architecture ( e.g, the number of layers in the DNN) or by tuning hyperparameters using Grid Search with Cross-Validation. 

The complete code, along with the detailed comments, visualizations, and all steps of the process is documented in the jupyter notebook. 

Below are the results of the five models. 
In this problem, classifying a background event(h) as signal (g) is worse than classifying a signal event as background.  Therefore, particular attention was paid to minimizing false positives in the background class. I chose to evaluate my model's performance using the AUC and ROC metrics. 

### conclusion 




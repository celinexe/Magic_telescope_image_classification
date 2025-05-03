# MAGIC GAMMA TELESCOPE IMAGE CLASSIFICATION 

MAGIC gamma telescope data 2004
This dataset is extracted from Kaggle: https://www.kaggle.com/datasets/abhinand05/magic-gamma-telescope-dataset




Context of the Dataset:

The MAGIC Gamma dataset originates from observations made by the MAGIC (Major Atmospheric Gamma Imaging Cherenkov) telescope, which detects gamma rays in the TeV range. The dataset was developed to classify signals into gamma signals (signal) and hadron-induced signals (background). Gamma signals correspond to electromagnetic showers caused by gamma rays, while background signals arise from hadronic cosmic rays, which create more complex showers.
![](https://github.com/celinexe/Magic_telescope_image_classification/blob/main/images/detection.png)



Feature Extraction  

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

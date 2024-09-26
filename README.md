# Quantitative Analysis of XAI Visualization [MATLAB]

## Description
Explainable Artificial Intelligence (XAI) plays a vital role in enhancing the transparency, interpretability, and reliability of AI models, especially in fields like healthcare, agriculture, and engineering. Despite its importance, most existing XAI research predominantly relies on qualitative evaluation methods, such as subjective visual assessments of model explanations. These approaches are often inconsistent, lack scalability, and pose challenges in terms of reproducibility and reliability. This study addresses these gaps by presenting a novel quantitative approach for assessing the performance of XAI models. We propose a three-stage framework that comprehensively evaluates deep learning models based on their decision-making accuracy (classification performance) and their ability to identify key features that inform their decisions. To the best of our knowledge, this is the first study to apply a fully quantitative method for evaluating explanations generated by XAI techniques.

## Purpose
We developed this MATLAB toolbox to provide a quantitative evaluation framework for XAI methods, particularly focusing on the assessment of deep learning models' classification performance and feature selection accuracy. Our toolbox enables researchers to quantitatively evaluate explanations generated by XAI technique LIME, without requiring extensive coding expertise. It provides an intuitive interface for performing robust performance evaluations, ensuring consistency, scalability, and reproducibility of results. The toolbox includes customizable evaluation metrics, automated analysis features, and comprehensive tutorials to guide users in using its full capabilities for reliable XAI assessments.

### 1. Instructions

### 2. Installation Instructions
1. Clone or download this repository.
2. Open MATLAB.
3. Add the toolbox folder to your MATLAB path using the following command:
    ```matlab
    addpath(genpath('path_to_toolbox'));
    ```

### 3. Usage Instructions
To use the bulk Grad-CAM and LIME function, run the following command in MATLAB:
```matlab
bulk_gradCAM_LIME_UI;
```

## Features
Here are the features provided by each script:

1. Train and save pre-trained deep learning models


2. LIME Feature Extraction: Extracts and visualizes the most significant features in images, generating both masked and binary masked images that highlight the top n significant features (lime_extract_features.m).
3. Quantitative Analysis: Calculates various quantitative metrics between a binarized image and its corresponding ground truth image (quantitative_evaluation_metrics.m).
4. Overfitting ratio calculation: calculates the overfitting ratio between a target ROI image and an identified ROI image (overfitting_ratio.m)




### Dependencies
Here are the dependencies required for the Explainable AI Toolbox to function correctly:

1. MATLAB Version
   - MATLAB R2020a or later

2. MATLAB Toolboxes
   - Image Processing Toolbox
   - Deep Learning Toolbox
   - Statistics and Machine Learning Toolbox
   - Computer Vision Toolbox
  
## Screenshots:

![LIME_Explanation](https://github.com/user-attachments/assets/4f72d621-2e3c-4112-bab4-74a223d518fd)


![Quantitative_Metrics](https://github.com/user-attachments/assets/bdc248f1-9b0c-445c-880d-3b60c132e797)


![Overfitting_Ratio](https://github.com/user-attachments/assets/e69f1835-ff5f-4171-be65-a07e0246ce48)


## Authors
1. Hari Kishan Kondaveeti, Ph.D
2. Chinna Gopi Simhadri, (Ph.D)

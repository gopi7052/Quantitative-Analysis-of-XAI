# Quantitative Analysis of XAI Visualization [MATLAB]

## Description
Explainable Artificial Intelligence (XAI) plays a vital role in enhancing the transparency, interpretability, and reliability of AI models, especially in fields like healthcare, agriculture, and engineering. Despite its importance, most existing XAI research predominantly relies on qualitative evaluation methods, such as subjective visual assessments of model explanations. These approaches are often inconsistent, lack scalability, and pose challenges in terms of reproducibility and reliability. This study addresses these gaps by presenting a novel quantitative approach for assessing the performance of XAI models. We propose a three-stage framework that comprehensively evaluates deep learning models based on their decision-making accuracy (classification performance) and their ability to identify key features that inform their decisions. To the best of our knowledge, this is the first study to apply a fully quantitative method for evaluating explanations generated by XAI techniques.

## Purpose
We developed this MATLAB toolbox to provide a quantitative evaluation framework for XAI methods, particularly focusing on the assessment of deep learning models' classification performance and feature selection accuracy. Our toolbox enables researchers to quantitatively evaluate explanations generated by XAI technique LIME, without requiring extensive coding expertise. It provides an intuitive interface for performing robust performance evaluations, ensuring consistency, scalability, and reproducibility of results. The toolbox includes customizable evaluation metrics, automated analysis features, and comprehensive tutorials to guide users in using its full capabilities for reliable XAI assessments.

## 1. Instructions
### 1.1 Training and Saving a Pre-trained Deep Learning Model
An image datastore to load images from a specified directory, organizing them into training and validation sets with a 60/40 split. The core of the model is built by loading a pretrained architecture and modifying its final layers to suit the specific number of disease classes in the dataset. This customization involves adding a new fully connected layer, a softmax layer, and a classification layer, enabling the model to output probabilities for each class. To enhance the model’s robustness, data augmentation techniques, such as random horizontal flipping and translations within a specified pixel range, are employed to expand the dataset and reduce the risk of overfitting artificially. The training process utilizes the Adam optimizer with a mini-batch size of 32 and a learning rate of 1e-4, spanning up to 30 epochs. Validation data is monitored throughout the training to track the model's performance. Upon completing the training, the model is saved as a MAT file for future inference. Performance metrics such as accuracy, precision, recall, F1 score, Matthews correlation coefficient (MCC), specificity, and false positive rate (FPR) are computed and displayed, providing a comprehensive overview of the model’s effectiveness in accurately classifying rice diseases.

### 1.2 Extract Top 'n' features using LIME
After training and saving the pre-trained deep learning model, a .mat file is created for further analysis. The Local Interpretable Model-agnostic Explanations (LIME) technique is employed to visualize the model's decision-making process. This involves loading the saved .mat file and extracting the top 'n' significant features that influence the model's predictions. The extracted features are then visualized, and a masked image is generated to highlight these important areas. Subsequently, this masked image is converted into a binarized format, emphasizing the significant features more distinctly for easier interpretation and analysis. This process enhances our understanding of the model's behavior and provides insights into the relevant features contributing to its predictions.

### 1.3 Perform Quantitative Analysis
To assess the similarity between two binary images specifically, the masked binary image of the most significant 'n' features generated by LIME and the ground truth image various quantitative metrics are employed. These metrics include Intersection over Union (IoU), Dice Similarity Coefficient (DSC), Precision, Recall, Matthews Correlation Coefficient (MCC), pixel-wise accuracy, and Mean Absolute Error (MAE). Each of these metrics is utilized to measure the degree of overlap and agreement between the features selected by the model and the ground truth. By applying this comprehensive set of quantitative analyses, we can evaluate the performance of the model and gain insights into the accuracy of the feature extraction process.

### 1.4 Calculate Overfitting Ratio
Overfitting occurs when a pre-trained model learns the training data too well, capturing noise and outliers rather than general patterns. This results in high accuracy on training data but poor performance on unseen data. To quantify overfitting, we introduced the overfitting ratio, defined as the ratio of the total area of pixels outside the identified diseased region to the total area of pixels within the actual ground truth diseased area. This metric reflects how much the model focuses on less significant features relative to the actual diseased area, offering a quantitative measure of overfitting in the model's predictions.


## 2. Installation Instructions
1. Clone or download this repository.
2. Open MATLAB.
3. Add the toolbox folder to your MATLAB path using the following command:
    ```matlab
    addpath(genpath('path_to_toolbox'));
    ```

## 3.Features
Here are the features provided by each script:

1. LIME Feature Extraction: Extracts and visualizes the most significant features in images, generating both masked and binary masked images that highlight the top n significant features (lime_extract_features.m).
2. Quantitative Analysis: Calculates various quantitative metrics between a binarized image and its corresponding ground truth image (quantitative_evaluation_metrics.m).
3. Overfitting ratio calculation: calculates the overfitting ratio between a target ROI image and an identified ROI image (overfitting_ratio.m)


## 4. Dependencies
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

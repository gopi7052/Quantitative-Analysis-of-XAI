# XAI_Quantitative_Analysis [MATLAB]

## Description
Explainable Artificial Intelligence (XAI) is essential for making AI models more transparent, interpretable, and trustworthy. As AI systems are increasingly deployed in critical sectors like healthcare, agriculture, and finance, understanding how these models make decisions becomes crucial to ensure their reliability and fairness. XAI techniques provide insights into the reasoning behind AI decisions, helping users to trust and validate the outputs, particularly in high-stakes applications.
We developed the MATLAB toolbox for Local Interpretable Model-Agnostic Explanations (LIME) provides an intuitive, user-friendly interface for visualizing and analyzing deep learning model explanations. It allows users to adjust parameters, generate LIME visualizations for multiple images, and assess model decision-making. The toolbox facilitates both qualitative and quantitative analysis, offering features to evaluate model performance and decision-making transparency. Users can examine the important features selected by models and conduct in-depth quantitative analysis. Additionally, the toolbox calculates overfitting ratios to more accurately assess the validity of model explanations. 

## Features
Here are the features provided by each script:
### 1. Train and save pre-trained deep learning models
Initially, the code sets up an image datastore to load images from a specified directory, organizing them into training and validation sets with a 60/40 split. The core of the model is built by loading a pretrained architecture and modifying its final layers to suit the specific number of disease classes in the dataset. This customization involves adding a new fully connected layer, a softmax layer, and a classification layer, enabling the model to output probabilities for each class. To enhance the model’s robustness, data augmentation techniques, such as random horizontal flipping and translations within a specified pixel range, are employed to expand the dataset and reduce the risk of overfitting artificially. The training process utilizes the Adam optimizer with a mini-batch size of 32 and a learning rate of 1e-4, spanning up to 30 epochs. Validation data is monitored throughout the training to track the model's performance. Upon completing the training, the model is saved as a MAT file for future inference. Performance metrics such as accuracy, precision, recall, F1 score, Matthews correlation coefficient (MCC), specificity, and false positive rate (FPR) are computed and displayed, providing a comprehensive overview of the model’s effectiveness in accurately classifying rice diseases.

### 2. Extract Top 'n' features using LIME
The MATLAB function _lime_extract_features_ offers a comprehensive and user-friendly interface designed for model interpretation using LIME (Local Interpretable Model-agnostic Explanations). The interface allows users to load a trained deep learning model, select an image for analysis, and choose an output folder for saving results. The layout includes buttons to load the model, select an image, and define the output folder, with additional functionality to adjust the number of top features through a dropdown menu. Upon starting the analysis, the UI displays multiple outputs: the original image, a heatmap with LIME explanations, and a masked image showing the top features. A binary masked image is also generated to visualize significant areas of the input image. These results can be saved as PDF files or images for further review. The UI provides control options for pausing or stopping the process, ensuring flexibility. Overall, the tool helps in understanding which parts of an image are most influential in the model's decision-making process.

![LIME_Explanation](https://github.com/user-attachments/assets/4f72d621-2e3c-4112-bab4-74a223d518fd)

### 3. Quantitative Analysis
This MATLAB function _quantitative_evaluation_metrics_ creates a graphical user interface (UI) for quantitative evaluation metrics in Explainable AI (XAI) analysis. It allows users to load two images: a ground truth image and a masked features image. The UI displays these images side by side and provides a button to calculate evaluation metrics, including IoU, Jaccard similarity, Dice similarity, sensitivity, specificity, precision, F1 score, and Matthew's correlation coefficient (MCC). Metrics are computed based on image comparison and displayed in a panel below the images. The UI enables easy visualization and comparison of image-based quantitative metrics.

![Quantitative_Metrics](https://github.com/user-attachments/assets/bdc248f1-9b0c-445c-880d-3b60c132e797)

### 4. Overfitting ratio
This MATLAB function _overfitting_ratio_ calculates the overfitting ratio between a target ROI image and an identified ROI image. It includes buttons for selecting images, displaying them on axes, and a panel to show metrics. Users select both images, which are resized and displayed in two axes. The "Calculate Metrics" button computes areas, true positives, false positives, and overfitting ratio based on pixel values. The results, including the overfitting ratio and the normalized area outside ROI, are displayed in the panel.

![Overfitting_Ratio](https://github.com/user-attachments/assets/e69f1835-ff5f-4171-be65-a07e0246ce48)


### Dependencies
Here are the dependencies required for the Explainable AI Toolbox to function correctly:

1. MATLAB Version
   - MATLAB R2020a or later

2. MATLAB Toolboxes
   - Image Processing Toolbox
   - Deep Learning Toolbox
   - Statistics and Machine Learning Toolbox
   - Computer Vision Toolbox

## Authors
1. Hari Kishan Kondaveeti, Ph.D
2. Chinna Gopi Simhadri, (Ph.D)

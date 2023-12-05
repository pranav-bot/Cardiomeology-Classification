# Cardiomegaly Classification 

## Overview
The Cardiomegaly Classification system is designed to classify chest X-ray images into categories related to the presence or absence of cardiomegaly. This documentation provides information on the dataset, model architecture, training process, and evaluation metrics.

# Dataset
## NIH CXR8 Dataset
The NIH CXR8 dataset is a collection of chest X-ray images curated by the National Institutes of Health (NIH). It consists of images labeled with various thoracic pathology categories, including cardiomegaly. The dataset is widely used for training and evaluating deep learning models for medical image analysis.

Dataset Link: <a heref="https://nihcc.app.box.com/v/ChestXray-NIHCC">NIH CXR8 Dataset</a>

# Model Architecture
## InceptionV3-Based Convolutional Neural Network (CNN)
The Cardiomegaly Classification model is built upon the InceptionV3 architecture, a deep convolutional neural network that has proven effective for image classification tasks. InceptionV3 is known for its ability to capture complex patterns and features in images through the use of inception modules.

### Model Layers:
<ul>
<li>Input Layer: Accepts chest X-ray images of fixed dimensions.</li>
<li>Inception Blocks: Multiple blocks consisting of parallel convolutional and pooling operations with different filter sizes.</li>
<li>Global Average Pooling Layer: Reduces spatial dimensions and retains important features globally.</li>
<li>Fully Connected Layers: Make predictions based on features extracted by the InceptionV3 backbone.</li>
<li>Output Layer: Produces probability scores for the presence or absence of cardiomegaly.</li>  
</ul>

<ol>
<li>Data Preprocessing: Resizing, normalization, and augmentation of input images.</li>
<li>Model Compilation: loss='binary_crossentropy', optimizer='adam'</li>
<li>Training: Iteratively updating model weights using labeled training data.</li>
<li>Validation: Assessing model performance on a separate validation set to avoid overfitting.</li>
</ol>

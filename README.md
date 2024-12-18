# Semantic-Segmentation-of-Street-Scenes-Using-Deep-Learning

## Overview
This project focuses on semantic segmentation using advanced deep learning architectures. The implementation covers end-to-end processing from data preparation to model training and evaluation. The goal is to classify each pixel of an image into predefined categories using U-Net, Residual U-Net, and SegNet architectures.

## Features
- **Custom Dataset**: Includes 200 training images, 70 validation images, and 150 test images with corresponding segmentation masks.
- **Data Preprocessing**: Resizing, normalization, and augmentation (flipping, rotation, and brightness adjustments).
- **Architectures**: Implements U-Net, Residual U-Net, and SegNet for semantic segmentation.
- **Regularization**: Incorporates dropout and L2 regularization to mitigate overfitting.
- **Results Analysis**: Comprehensive evaluation of models based on validation accuracy.

## Dataset
The `ProjectDataset` folder contains:
- **Training Images**: Images for model training.
- **Validation Images**: Images for model validation.
- **Test Images**: Images for testing the model’s generalization.
- **Segmentation Masks**: Corresponding masks for training and validation.

## Directory Structure
```
Image-Processing-Project/
├── ProjectDataset/
│   ├── Train/
│   ├── Validation/
│   └── Test/
├── saved_models/
├── Test Predictions/
├── image_processing.ipynb
├── Image Processing Project Report.docx
└── README.md
```

## Models Implemented
### 1. U-Net
- Symmetric encoder-decoder architecture with skip connections.
- Achieved highest validation accuracy of **0.6980**.

### 2. Residual U-Net
- Incorporates residual connections for improved gradient flow.
- Best validation accuracy: **0.7027**.

### 3. SegNet
- Pooling indices for upsampling instead of skip connections.
- Lightweight but less accurate compared to U-Net and Residual U-Net.

## Results
Model performance on the validation set:
| Model            | Best Validation Accuracy |
|-------------------|---------------------------|
| U-Net            | 0.6980                    |
| Residual U-Net   | 0.7027                    |
| SegNet           | 0.6302                    |

## Files
- **ProjectDataset/**: Contains all the training, validation, and test images along with segmentation masks.
- **saved_models/**: Directory with trained model weights for U-Net, Residual U-Net, and SegNet.
- **Test Predictions/**: Folder containing model predictions for the test set.
- **image_processing.ipynb**: Jupyter Notebook with the implementation of the project.
- **Image Processing Project Report.docx**: Detailed report documenting the workflow, architectures, and results.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/image-processing-project.git
   cd image-processing-project
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open and run the Jupyter Notebook:
   ```bash
   jupyter notebook image_processing.ipynb
   ```

4. Explore the `saved_models` and `Test Predictions` folders for model outputs.

## Conclusion
This project demonstrates the effective use of deep learning architectures for semantic segmentation. U-Net proved to be the most balanced model, while Residual U-Net excelled in deeper configurations. SegNet offers a lightweight alternative but sacrifices some accuracy. The code and models can be extended for other segmentation tasks with minor adjustments.



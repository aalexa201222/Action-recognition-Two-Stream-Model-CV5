# Action Recognition with CNNs using Transfer Learning and Optical Flow

## Overview
This project explores action recognition in both still images and videos using convolutional neural networks (CNNs). The focus is on applying transfer learning techniques and integrating optical flow data to enhance model performance across two distinct datasets: Stanford 40 (image-based) and HMDB51 (video-based). The project aims to classify actions by leveraging the strengths of different CNN architectures and input modalities.

## Key Features
- **Transfer Learning**: Utilizes pre-trained models to improve learning efficiency and effectiveness.
- **Optical Flow Integration**: Employs optical flow to capture motion information from videos, enhancing the model's ability to recognize dynamic actions.
- **Two-stream Network**: Combines spatial and temporal data streams to create a robust model for action recognition.

## Datasets
- **Stanford 40**: Consists of 9532 images across 40 action categories. We focus on 12 overlapping categories with HMDB51 for this project.
- **HMDB51**: Contains short video clips across 51 action classes with significant intra-class variation.

## Model Architectures
### Frame CNN (Stanford 40)
- **Architecture**: Modified ResNet-18 adjusted to output 12 classes specific to the action categories in Stanford 40.
- **Layers and Hyperparameters**:
  - Input size: 224x224
  - Adam optimizer with a learning rate of 0.001
  - Cross-entropy loss

### HMDB51 – Frames (Transfer Learning)
- Utilizes the pre-trained Frame CNN, fine-tuned on the central frames of HMDB51 video clips.

### HMDB51 – Optical Flow
- **Architecture**: Adapted ResNet-18 for optical flow inputs, processing stacked optical flow fields to capture motion.
- **Input**: Stacked optical flow images (224x224x8)

### Two-Stream Network (HMDB51)
- Integrates Frame and Optical Flow CNNs, fusing outputs via a concatenation layer to leverage both spatial and temporal information.
## Results and Discussion
Each model's performance is evaluated based on accuracy and loss metrics, detailed in the project report. The integration of optical flow and the two-stream architecture are particularly noted for their potential to enhance action recognition performance in complex video scenarios.
## Software and Installation
- **Python 3.6+**: Recommended for all development and testing.
- **PyTorch**: Primary framework used for model development.
- **CUDA GPU**: If available, enables significant speed-up in model training.

## Installation
Clone the repository to your local machine:
git clone [[https://github.com/aalexa201222Action-recognition-Two-Stream-Model-CV5.git](https://github.com/aalexa201222/Action-recognition-Two-Stream-Model-CV5)](https://github.com/aalexa201222/Action-recognition-Two-Stream-Model-CV5)

## Contributors
[Andreas Alexandrou](https://www.linkedin.com/in/andreas-alexandrou-056528242) <br />
Sotiris Zenios

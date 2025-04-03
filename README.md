
# Solar Panel Detection in Satellite Images

This project focuses on detecting solar panels in satellite images, a crucial task for energy monitoring. We employed the SegFormer-b1 model along with data augmentation techniques to develop an effective segmentation model. The initial results demonstrate promise, with a Mean Intersection over Union (IoU) of 0.0133. Future improvements will explore advanced models, larger datasets, and optimized training methods.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Data Preparation](#data-preparation)
- [Model Training](#model-training)
- [Results](#results)
- [Future Work](#future-work)
- [License](#license)

## Overview

Detecting solar panels from satellite imagery is vital for effective energy resource management. This project utilizes the SegFormer architecture, which leverages transformer models for image segmentation, making it suitable for distinguishing solar panels from their background in satellite images.

## Features

- **SegFormer-b1 Architecture**: Utilizes a state-of-the-art segmentation model for accurate detection.
- **Data Augmentation**: Enhances the robustness of the model by generating additional training data.
- **Evaluation Metrics**: Employs Mean IoU to assess model performance.

## Requirements

- Python 3.7 or later
- Pytorch
- torchvision
- NumPy
- OpenCV
- SegFormer dependencies (check the official repository for details)

Install the required libraries using pip:

```bash
pip install torch torchvision numpy opencv-python
```

## Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/atharvapatil1210/solar-detection.git
    cd solar-panel-detection
    ```

2. **Set Up Virtual Environment** (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## Data Preparation

- The dataset should contain satellite images annotated with the locations of solar panels. 
- Organize the dataset into a directory structure that the training script can easily access.
- Apply data augmentation techniques to increase the diversity of the training data, such as:
  - Rotation
  - Flipping
  - Scaling

## Model Training

To train the model, run the following command:

```bash
python train.py --data_dir path/to/dataset --output_dir path/to/save/model
```

Adjust the `data_dir` and `output_dir` parameters to point to your dataset and where you want to save the trained model, respectively.

## Results

The current model achieved a Mean IoU of **0.0133** on the validation set, indicating initial promise. However, this metric highlights significant room for improvement.

## Future Work

- Explore advanced segmentation models that may provide better accuracy.
- Increase the dataset size for more comprehensive training.
- Optimize training processes, including hyperparameter tuning and potentially using transfer learning.

## License

This project is licensed under the MIT License.

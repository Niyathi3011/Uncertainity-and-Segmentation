# Vision and Uncertainty - Image Segmentation

This project focuses on training a vision model for image segmentation and explores techniques such as hyperparameter tuning, data augmentation, and mixup training to improve the model's performance. The project utilizes a dataset for image segmentation and evaluates the model's accuracy and calibration.

## Hyperparameter Choices

The hyperparameters were selected through a systematic experimentation process. The following values were chosen:

- Learning Rate: 0.01
- Momentum: 0.9
- Weight Decay: 0.01
- Batch Size: 64
- Number of Epochs: 50

## Preprocessing

The dataset was preprocessed as follows:

- Images were resized and center cropped to 256x256 pixels.
- Image normalization was applied using mean values [0.485, 0.456, 0.406] and standard deviation values [0.229, 0.224, 0.225].

## Training and Validation Loss Curves

The training and validation loss curves show the model's performance during training. These curves provide insights into convergence and overfitting tendencies.

## Accuracy Metric

The baseline model achieved an accuracy of 79.92% with the chosen hyperparameters. An accuracy vs. epochs plot is included to visualize the model's progress during training.

## Image Segmentation

An example image from the validation dataset is provided, along with its true segmentation and the predicted segmentation obtained from the model. These visualizations demonstrate the model's effectiveness in segmenting objects of interest.

## Confidence Calibration Curve

The confidence calibration curve analyzes the model's confidence in its predictions. It measures the calibration error and determines the accuracy of the model's confidence estimates.

## Expected Collaboration Error

The expected calibration error for the selected hyperparameters is approximately 6.59%. This metric provides insights into the model's calibration and confidence estimation capabilities.

## Data Augmentation

Data augmentation techniques, including RandomRotation and ColorJitter, were employed to increase the diversity and robustness of the training data. The chosen combination of data augmentation techniques resulted in an accuracy improvement of 2.45% (82.45% accuracy) compared to the baseline.

## Mixup Training

Mixup training was implemented with different alpha values (0.2, 0.5, and 0.8) to enhance the model's performance. However, contrary to expectations, mixup training showed a decrease in accuracy compared to the baseline. This behavior may be attributed to spatial misalignment and semantic inconsistencies introduced by mixup.

## Wand Links

Additional details, metrics, and visualizations can be found on the corresponding Weights & Biases (wandb) pages:

- [Baseline Model](https://wandb.ai/alluniyathi/ML-CV-HW2-Baseline)
- [Data Augmentation](https://wandb.ai/alluniyathi/ML-CV-HW2)

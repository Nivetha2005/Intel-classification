# Intel-classification


This project demonstrates the use of TensorFlow and Keras Tuner for image classification. The model uses a Sequential architecture with a pre-trained Xception base, followed by Global Average Pooling, Dense layers, and Dropout for regularization. Keras Tuner is used for hyperparameter optimization.

## Prerequisites

- Python 3.8 or higher
- Anaconda (optional but recommended)
- TensorFlow 2.x
- Keras Tuner
- Matplotlib
- Required libraries (can be installed via `requirements.txt`)

## Installation

1. **Create a Virtual Environment:**
   ```bash
   conda create -n fdsproject python=3.8
   conda activate fdsproject
2. **Install the Required Packages:**
    ```bash
    pip install tensorflow keras-tuner matplotlib
    ```
3. **Run the Script:** Ensure the script is compatible with TensorFlow 2.x. You might encounter deprecation warnings due to changes in TensorFlow's API. The script will still execute but be mindful of the warnings and consider updating the code to the latest API standards.

## Dataset

- The dataset used in this project is from Kaggle: [Intel Image Classification Dataset](https://www.kaggle.com/datasets/puneet6060/intel-image-classification).
- It contains 14,034 images belonging to 6 different classes for training and 3,000 images for validation.
- Images are loaded and processed accordingly before feeding them into the model.


## Model Summary

- **Base Model:** Xception (Pre-trained)
- **Layers:**
  - Global Average Pooling
  - Dense (256 units)
  - Dropout (0.5)
  - Dense (6 units - corresponding to the 6 classes)
- **Total Parameters:** 21,387,566
  - **Trainable Parameters:** 21,333,038
  - **Non-Trainable Parameters:** 54,528

## Training

- The model is trained over 3 epochs.
- Hyperparameters such as `learning_rate`, `dropout`, and `units` are optimized using Keras Tuner's RandomSearch.

## Results

- The training process is monitored, and visualizations are generated for better understanding.
- The model architecture and training progress are saved for future use.

## Visualization

- Various plots are generated to visualize the training process and model performance. These include accuracy, loss, and more.

## Notes

- Ensure that your TensorFlow version is compatible with the codebase to avoid any execution issues.
- It is recommended to address the deprecation warnings by updating the code to use the latest TensorFlow API.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



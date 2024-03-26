
# Gender Classification Model

This repository contains code for training a Convolutional Neural Network (CNN) model to classify gender based on spectrogram images. The model is implemented using TensorFlow and Keras.

## Requirements
- TensorFlow
- scikit-learn
- joblib
- pickle

## Usage

1. First, ensure you have installed all the required libraries mentioned above.

2. Clone this repository:

    ```bash
    git clone https://github.com/yourusername/gender-classification.git
    ```

3. Navigate to the cloned directory:

    ```bash
    cd gender-classification
    ```

4. Run the `gender_classification.py` script:

    ```bash
    python gender_classification.py
    ```

## Description

### Data Loading and Preprocessing

- Spectrogram images are loaded and preprocessed using the `ImageDataGenerator` class from Keras.
- The data is split into training and validation sets.

### Model Architecture

- A CNN model is built using the Sequential API from Keras.
- It consists of multiple convolutional layers followed by max-pooling layers to extract features.
- Dropout regularization is applied to reduce overfitting.
- The output layer uses the sigmoid activation function for binary classification.

### Training

- The model is compiled using the Adam optimizer and binary cross-entropy loss function.
- Training is performed for 10 epochs using the training data.
- Model performance is evaluated on the validation set.

### Model Evaluation

- The trained model is evaluated using the validation generator.
- Test accuracy is printed after evaluation.

## Files

- `gender_classification.py`: Python script containing the model training code.
- `model.joblib`: Saved model using joblib.
- `gender_classification_model.h5`: Saved model using Keras.

## Note

- Make sure to adjust the directories in the code to point to the correct location of your dataset.
- This readme assumes you are using the provided dataset structure. If your dataset structure differs, make appropriate changes to the code.

Feel free to customize and experiment with the code for your specific use case!

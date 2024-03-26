# Female Age Classification Model

This repository contains code for training a neural network model to classify the age group of females based on MFCC (Mel-frequency cepstral coefficients) features extracted from audio data. The model is implemented using TensorFlow and scikit-learn.

## Requirements
- pandas
- librosa
- numpy
- TensorFlow
- scikit-learn
- h5py
- joblib

## Usage

1. Make sure you have installed all the required libraries mentioned above.

2. Clone this repository:

    ```bash
    git clone https://github.com/yourusername/female-age-classification.git
    ```

3. Navigate to the cloned directory:

    ```bash
    cd female-age-classification
    ```

4. Run the `female_age_classification.py` script:

    ```bash
    python female_age_classification.py
    ```

## Description

### Data Loading and Preprocessing

- MFCC features are loaded from a pickle file containing precomputed MFCCs for female audio samples.
- The dataset is loaded from a CSV file containing information about the samples including their paths and age labels.
- Age labels are mapped to three age ranges: teens-twenties, thirties-fifties, and sixties-eighties.
- Error files, if any, are filtered out from the dataset.

### Model Architecture

- A feedforward neural network model is built using TensorFlow's Sequential API.
- It consists of multiple dense layers with ReLU activation functions.
- The output layer uses the softmax activation function for multi-class classification into three age ranges.

### Training

- The model is compiled using the Adam optimizer and sparse categorical cross-entropy loss function.
- Training is performed for 200 epochs.
- The dataset is split into training, validation, and test sets.

### Model Evaluation

- The model is evaluated on the test set.
- Test accuracy is printed after evaluation.

## Files

- `female_age_classification.py`: Python script containing the model training code.
- `label_encoder.pkl`: Pickle file containing the label encoder used for age range encoding.
- `female_age_cnn_model.h5`: Saved model using HDF5 format.
- `female_age_cnn_model.pkl`: Saved model using pickle.
- `female_age_cnn_model.joblib`: Saved model using joblib.

Feel free to customize and experiment with the code for your specific use case!

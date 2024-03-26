# Preprocessing Data and Making Spectrograms

This repository contains code to preprocess the data. The code to preprocess the data uses the numpy and pandas python libraries. The spectrograms are created using the pytorch and librossa Python libraries.

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

## Requirements
- Numpy
- Pandas
- Librossa
- Pytorch
- Matplotlib
- Shutil

##Procedure

### Dataset description
The dataset used is a combination of Common Voice Corpus 2 and 4 from Mozilla Common Voice. The dataset contains audio data from a wide age range of people from both genders. The CSV provided with the data contains the age, gender and the sentence spoken for each individual audio file. 

### Data Cleaning
The CSV was cleaned of any rows containing null data. Audio files were then sorted into two folders of 'male' and 'female' based on gender. 

### Sorting by age
The audio was sorted into three folders based on age group: teens-twenties, thirties-fifties and sixties-eighties.  

### Preprocessing audio and Spectrogram generation
To preprocess the audio, the audio was shortened down to a standard length of 1 second, the amplitude range was normalized, noise reduction was applied and silences were removed. Matplotlib library was then used to extract features from the audio and use them to make and save spectrograms.

### Sorting by gender
The spectrograms were sorted based on their gender and moved to new folders called 'malemelspectrogram' and 'femalemelspectrogram' using shutil functions.




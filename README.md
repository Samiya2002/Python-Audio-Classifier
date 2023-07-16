# Python-Audio-Classifier
# UrbanSound8K Audio Classifier

This repository contains a Python audio classifier built using TensorFlow and Librosa to classify environmental sounds from the UrbanSound8K dataset. The classifier utilizes Mel-frequency cepstral coefficients (MFCCs) as audio features and a fully connected neural network for classification.

## Dataset

The UrbanSound8K dataset consists of 8732 labeled sound excerpts from various urban environments, categorized into 10 classes such as car horn, street music, drilling, etc. Due to the large size of the dataset, it is not directly included in this repository. You can download the dataset from Kaggle using the following link: [UrbanSound8K Dataset on Kaggle](https://www.kaggle.com/chrisfilo/urbansound8k).

Once you've downloaded the dataset, please place it in the `data` directory before running the code.

## Project Structure

The repository is organized as follows:

- `Python_audio_classifier.py`: The main Python script containing the audio classifier implementation.
- `Dataset/`: The directory where the UrbanSound8K dataset should be placed.
- `README.md`: The README file you are currently reading, providing an overview of the project and instructions.

## Requirements

Before running the audio classifier, make sure you have the following dependencies installed:

- Python 3.x
- TensorFlow
- Librosa
- Pandas
- NumPy

You can install the required libraries using the following command:

```bash
pip install tensorflow librosa pandas numpy
```

## Running the Classifier

To run the audio classifier, follow these steps:

1. Download the UrbanSound8K dataset from the Kaggle link mentioned above.
2. Place the dataset in the `data` directory of this repository.
3. Open `audio_classifier.py` and set the correct `data_directory` variable to the path where the UrbanSound8K dataset is located.
4. Run the script:

```bash
python audio_classifier.py
```

The classifier will extract audio features from the dataset, split it into training and testing sets, train the neural network, and evaluate its performance. The final accuracy and classification report will be displayed in the console.

## Making Predictions

To make predictions on new audio files, you can use the provided `print_prediction` function in the script. Simply replace `file_name` with the path to your audio file, and the classifier will predict the class label for that file.

```python
file_name = 'path/to/your/audio/file.wav'
print_prediction(file_name)
```

Please ensure that the audio file is in WAV format for accurate predictions.

## Model Architecture

The audio classifier's neural network architecture consists of three hidden layers with 128, 256, and 256 neurons, respectively, followed by a dropout layer to prevent overfitting. The final layer has 10 neurons, representing the number of sound classes in the dataset. The model uses the softmax activation function to output the class probabilities.

## License

The code in this repository is provided under the MIT License. You are free to use, modify, and distribute it for your projects.

---
By using the provided Kaggle link to download the dataset, users can access the UrbanSound8K dataset and run the audio classifier without the need to upload large files to Git. The README file provides clear instructions on setting up the project, running the code, and making predictions on new audio files. Feel free to modify the README to add any other relevant details or sections that you may find useful for your project.

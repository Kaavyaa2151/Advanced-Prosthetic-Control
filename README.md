#sEMG Signal Processing and Gesture Recognition
This project demonstrates the processing and classification of surface Electromyography (sEMG) signals for gesture recognition. The pipeline includes signal filtering, feature extraction using the Haar wavelet transform, and classification using a K-Nearest Neighbors (KNN) classifier.

##Table of Contents
Introduction
Requirements
Dataset
Usage
Project Description
Results
License
##Introduction
sEMG signals are electrical signals produced by skeletal muscles. These signals can be analyzed to recognize different gestures. This project involves several steps:

Loading and visualizing the raw sEMG signals.
Applying a bandpass filter to remove unwanted frequencies.
Extracting features using the Haar wavelet transform.
Smoothing the transformed signals using a moving average filter.
Classifying the gestures using a KNN classifier.
##Requirements
Python 3.x
NumPy
pandas
matplotlib
scikit-learn
SciPy
You can install the required packages using pip:

pip install numpy pandas matplotlib scikit-learn scipy
##Dataset
Replace 'your_dataset.txt' with the actual path or filename of your sEMG data file. The dataset should be a tab-delimited text file with the first column representing the time and the next eight columns representing the sEMG signals from eight channels.

##Usage
Clone the repository:
git clone https://github.com/your_username/sEMG-gesture-recognition.git
cd sEMG-gesture-recognition
Replace the dataset path in the code:
dataset = pd.read_csv('path/to/your_dataset.txt', delimiter='\t')
Run the script:
python sEMG_gesture_recognition.py
##Project Description
The project involves the following steps:

Load and visualize the dataset: The sEMG signals from eight channels are loaded and visualized to understand the raw data.

Bandpass filtering: A Butterworth bandpass filter is applied to the signals to retain frequencies between 20 Hz and 500 Hz, which are relevant for muscle activity.

Feature extraction using Haar wavelet transform: The filtered signals are transformed using the Haar wavelet transform to extract frequency domain features.

Smoothing using moving average: The transformed signals are smoothed using a moving average filter to reduce noise and highlight underlying patterns.

Classification using KNN: The processed signals are split into training and testing sets. A KNN classifier is trained on the training set and evaluated on the test set. The performance of the classifier is measured using accuracy and a detailed classification report.

##Results
The script prints the accuracy and a classification report, including precision, recall, and F1-score for each class

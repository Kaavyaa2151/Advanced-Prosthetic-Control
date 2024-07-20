EMG Signal Processing and Classification
This repository contains a Python script for processing and classifying electromyography (sEMG) signals using various techniques, including bandpass filtering, Haar wavelet transform, and moving average smoothing. The script performs signal processing and feature extraction, followed by classification using a K-Nearest Neighbors (KNN) algorithm.

Table of Contents
Overview
Requirements
Usage
Data
Results
License
Overview
The provided Python script performs the following tasks:

Load and Process sEMG Data: Reads sEMG data from a specified text file.
Bandpass Filtering: Applies a bandpass filter to remove noise from the signals.
Haar Wavelet Transform: Transforms the filtered signals using Haar wavelet transform.
Moving Average: Applies a moving average to smooth the wavelet-transformed signals.
Visualization: Plots the raw, filtered, and wavelet-transformed signals.
Feature Extraction: Extracts features from the processed signals.
Classification: Uses a K-Nearest Neighbors classifier to classify the signals based on extracted features.
Requirements
Ensure you have the following Python libraries installed:

numpy
pandas
matplotlib
scikit-learn
scipy
You can install the required libraries using pip:

sh
Copy code
pip install numpy pandas matplotlib scikit-learn scipy
Usage
Clone the Repository:

sh
Copy code
git clone https://github.com/yourusername/EMG_signal_processing.git
cd EMG_signal_processing
Modify Dataset Path: Edit the script to include the correct path to your sEMG dataset file. Update the line:

python
Copy code
dataset = pd.read_csv('path_to_your_dataset.txt', delimiter='\t')
Run the Script:

Execute the script using Python:

sh
Copy code
python emg_signal_processing.py
The script will generate plots for raw, filtered, and wavelet-transformed signals, and output the classification results.

Data
Replace 'path_to_your_dataset.txt' with the path to your dataset file. The script expects a tab-delimited file with sEMG signals organized into columns, where each column represents a channel of data.

Results
The script will produce the following outputs:

Plots: Visualizations of raw sEMG signals, filtered signals, Haar wavelet transformed signals, and signals with moving average applied.
Classification Report: Accuracy and detailed classification report for the K-Nearest Neighbors classifier.
License
This project is licensed under the MIT License - see the LICENSE file for details.

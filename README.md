# Arrythmia-Predictor

# INTRODUCTION 
With emergence of wearable products (e.g. Apple Watch and portable EKG machines) that are 
capable of monitoring your heart while at home. As such, I was curious how to build a machine learning algorithm that could detect abnormal heart beats. Here we will use an ECG signal (continuous electrical measurement of the heart) and train 3 neural networks to predict heart arrythmias: dense neural network, CNN, and LSTM.

# DATASET
We will use the MIH-BIH Arrythmia dataset from https://physionet.org/content/mitdb/1.0.0/. This is a
dataset with 48 half-hour two-channel ECG recordings measured at 360 Hz. The recordings have annotations from cardiologists for each heart beat. The symbols for the annotations can be found at https://archive.physionet.org/physiobank/annotations.shtml
# PROJECT DESCRIPTION
Predict if a heart beat from the first ECG signal has an arrhythmia for each 6 second window centered on the peak of the heart beat.

To simplify the problem, we will assume that a QRS detector is capable of automatically identifying the peak of each heart beat. We will ignore any non-beat annotations and any heart beats in the first or last 3 seconds of the recording due to reduced data. We will use a window of 6 seconds so we can compare the current beat to beats just before and after. This decision was based after
talking to a physician who said it is easier to identify if you have something to compare it to.

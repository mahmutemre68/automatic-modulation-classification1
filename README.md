# Wireless Signal Modulation Classification using Machine Learning

This project implements an Automatic Modulation Classification (AMC) system to identify digital modulation types (BPSK, QPSK, 8PSK) from noisy I/Q signals.

## Project Overview
In modern wireless communications (5G/6G) and electronic warfare, identifying the modulation type of a detected signal is crucial. This project simulates a communication channel and uses Machine Learning to classify signals without prior knowledge of channel parameters.

## Tech Stack
* Language: Python 3.12
* Signal Processing: NumPy (I/Q generation, AWGN channel simulation)
* Machine Learning: Scikit-Learn (Random Forest Classifier)
* Visualization: Matplotlib

## Methodology
1.  Data Generation: Synthetic signals are generated for BPSK, QPSK, and 8PSK.
2.  Channel Model: An AWGN (Additive White Gaussian Noise) channel is applied with SNR varying from -5 dB to +15 dB.
3.  Feature Engineering: Raw I/Q samples are flattened and fed into the classifier.
4.  Classification: A Random Forest model (n=100) learns the statistical properties of the constellations.

## Results
* Achieved >90% accuracy at SNR levels above 5 dB.
* Successfully distinguished between high-order modulations (QPSK vs 8PSK) under noisy conditions.
* Confusion matrix analysis shows BPSK is the most robust modulation against noise.

## How to Run
```bash
python main.py

# VoiceGuard — AI Voice Deepfake Detector

Detects AI-generated (deepfake) audio to identify vishing (voice phishing) fraud.

## Results
- Dataset: Fake-or-Real (FoR), 53,000+ audio samples
- Model: Random Forest on MFCC features
- Accuracy: 85.6% | F1 (fake): 0.841

## How it works
1. Extracts 40 MFCC features from each audio file using Librosa
2. Trains a Random Forest classifier (200 trees, class-balanced)
3. Evaluates using F1 score to account for class imbalance

## Tech Stack
Python, Librosa, Scikit-learn, Kaggle

## Phase 2 (in progress)
CNN on Mel Spectrograms using PyTorch — preserving time-axis information
that Phase 1's averaging discards.

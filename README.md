# Overview:
This project was developed as part of my university dissertation. The goal was to build a program capable of detecting moments of laughter in audio recordings, using only sound-based features — with no reliance on visual or contextual cues. The project involved experimenting with various machine learning architectures, including Convolutional Neural Networks (CNNs) and Long Short-Term Memory (LSTM) networks, to determine the most efficient approach.

## Dataset:
The audio dataset used for this project consists of two-person recorded conversations. Each file contains spontaneous speech, silence, and instances of laughter. To train the model effectively:

MFCCs (Mel-Frequency Cepstral Coefficients) were extracted as features from the audio.

Labels were assigned per audio frame:

1 for laughter,

0 for non-laughter (e.g., speech or silence).

## Methodology:
Data Preprocessing:
Raw audio was processed to extract MFCCs and aligned with labeled segments. Preprocessing also included normalizing features and segmenting the data into suitable frames for training.

### Modeling Approaches:
Multiple models were tested, including:

Convolutional Neural Networks (CNNs) for spatial pattern detection in audio frames

LSTM networks for capturing temporal patterns in sound

### Model Training & Evaluation:
Each model was trained on the same preprocessed dataset and evaluated using classification metrics to determine which architecture performed best in detecting laughter.

### Experiment Tracking:
Different configurations, window sizes, and architectures were recorded and compared to identify the most reliable and computationally efficient method.

## Results:
The best-performing model (a CNN) demonstrated strong performance in identifying laughter events in conversation audio. Evaluation metrics such as accuracy, precision, recall, and F1-score were used to assess model quality.

## Tools Used
Python
Chosen for its simplicity and extensive ecosystem, making it ideal for machine learning and audio processing tasks.

Librosa
A powerful audio analysis library used for extracting features like MFCCs, RMS, and mel spectrograms, essential for training the models.

TensorFlow & Keras
Used for building and training deep learning models, including CNN and LSTM architectures.

Matplotlib & Seaborn
Used to visualize model performance through confusion matrices, accuracy/loss graphs, and comparisons, aiding in clear result interpretation.

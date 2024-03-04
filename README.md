# ML-project
The provided code performs audio classification using a neural network model. Let's break down the code step by step:

1. **Data Importation:** The code starts by importing necessary libraries and then mounts Google Drive to access the dataset.

2. **Data Preparation and Exploration:**
   - The UrbanSound8K dataset is loaded from a CSV file.
   - Basic exploratory analysis is performed, including checking the distribution of classes and displaying a random waveform and spectrogram.

3. **Audio Feature Extraction:** Mel-frequency cepstral coefficients (MFCCs) are extracted from audio files. MFCCs capture the spectral characteristics of the sound, providing essential features for classification.

4. **Data Preprocessing:**
   - MFCC features are computed for each audio file and stored in a dataframe.
   - Features are converted into numpy arrays, and class labels are encoded.

5. **Model Building:**
   - A deep neural network model is defined using the Keras Sequential API.
   - The model architecture consists of several dense layers with batch normalization and ReLU activation, followed by a softmax output layer for multi-class classification.

6. **Model Training:**
   - The model is compiled with the Adam optimizer and categorical cross-entropy loss function.
   - Training data is split into training and validation sets.
   - Early stopping and learning rate reduction callbacks are added to prevent overfitting and improve convergence.
   - The model is trained for a fixed number of epochs.

7. **Model Evaluation:**
   - Training and validation loss/accuracy metrics are plotted over epochs to visualize model performance.
   - The model is evaluated on the test set, and the validation accuracy is calculated.
   - A confusion matrix is generated to assess the model's performance on individual classes.

8. **Prediction on Custom Audio File:**
   - Finally, a custom audio file is loaded, and MFCC features are extracted.
   - The model predicts the class label of the custom audio file, and the predicted class is printed.

This code provides a comprehensive pipeline for audio classification using MFCC features and a neural network model, with the ability to evaluate the model's performance and make predictions on new audio samples.

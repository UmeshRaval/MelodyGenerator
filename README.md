# AI Music Generation with Flask

This repository contains a Flask-based web application for generating AI-composed music with melody coherence. The application leverages a deep learning model based on a 3-layer bidirectional LSTM neural network architecture to predict pitch, timing, duration, and velocity of musical notes.

---

## Features
- **Melody Coherence**: Ensures generated music maintains logical musical flow.
- **Deep Learning Model**: Utilizes a 3-layer bidirectional LSTM for robust predictions of musical components.
- **Web Interface**: Built with Flask to provide a user-friendly interface for generating and downloading music.

---

## Dataset
The model is trained on the **MAESTRO Dataset**, which consists of MIDI files representing over 200+ hours of classical piano performances. The dataset provides detailed musical information, enabling high-quality training and generation. Key features extracted from the dataset include:

### 1. Notes
- **Pitch**: The frequency of each note.
- **Duration**: The length of time each note is played.
- **Velocity**: The intensity or volume of each note.
- **Timing**: When each note occurs within the piece.

### 2. Chords
- Automatically extracted from the sequences of notes to understand the harmonic structure of the music.

### 3. Tempo and Time Signatures
- Governs the speed and rhythmic feel of the music, essential for generating compositions in similar styles.

---

## How It Works
1. **Input**: Users can specify parameters such as desired length and style of music.
2. **Processing**: The model uses the extracted features to generate coherent sequences.
3. **Output**: The generated music is saved as a MIDI file for playback or further editing.

**Train the Model:**
1. Train the model on the prepared training dataset, minimizing the combined loss function.
2. Monitor validation loss and adjust hyperparameters (e.g., number of epochs, learning rate).

**Melody Generation:**
1. Start Sequence:

 o Select a random sample from the dataset as the initial melody.

 o Extract and normalize the first few notes as input to the model.

**2. Iterative Prediction:**
 o For each iteration:
 
   Feed the input sequence to the model.
  
   Predict the next note: pitch, step, duration, and velocity.
  
   Calculate start and end times of the generated note using predicted step and
duration.

   Add the predicted note with its start and end times to the generated melody.

   Shift the input sequence by removing the first note and adding the new one.

 o Repeat the prediction and shifting for a desired number of not

 ## Few Visualizations:
 ![image](https://github.com/user-attachments/assets/a4630c61-997d-45c8-b2d8-6c68ea0eaea3)
![image](https://github.com/user-attachments/assets/54678da4-724d-496e-ab5f-b87a35f4f849)

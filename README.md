 

# Conditional Sketch Generation using Deep LSTM

## Overview
This project implements a multi-class conditional sequence generation model using a 3-layer LSTM architecture.  
The model learns to generate stroke-based sketches from the Google QuickDraw dataset using autoregressive sequence modeling.

---

## Key Features
- Multi-class sketch generation
- Delta-encoded stroke sequences
- Sequence truncation & padding (max length = 64)
- 3-layer LSTM (256 hidden units)
- Dropout regularization (0.3)
- Gradient clipping (max norm = 1.0)
- Early stopping for stable training
- MSE loss optimization

---

## Model Architecture

Input:
- One-hot encoded class vector
- Previous stroke sequence (Δx, Δy, pen_state)

Output:
- Predicted next stroke

Loss Function:
- Mean Squared Error (MSE)

Optimizer:
- Adam

---

## Tech Stack
- Python
- PyTorch
- NumPy
- Matplotlib
- Scikit-learn

---

## How to Run

1. Install dependencies:

pip install -r requirements.txt

2. Run:

python main.py

---

## Project Structure

conditional-sketch-lstm/
│
├── src/
├── main.py
├── requirements.txt
├── README.md
└── .gitignore

---

## Future Improvements
- Add Transformer-based architecture
- Add evaluation metrics (sequence similarity)
- Deploy using Streamlit

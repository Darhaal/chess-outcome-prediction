# 🤖 Chess Outcome Prediction

Machine learning project for predicting chess game outcomes using mid-game positions.

## 📌 Problem

Predict:
- White win
- Black win
- Draw

based on board state at move 15.

---

## 🧠 Approach

- Converted chess board into tensor representation (13×8×8)
- Trained deep learning model on Lichess dataset
- Multi-class classification problem

---

## 📊 Results

- Accuracy: ~61%
- Strong performance on win/loss prediction
- Lower performance on draws due to class imbalance

---

## 📓 Notebook

See full implementation and experiments:

`notebook.ipynb`

---

## ⚙️ Tech Stack

- Python
- PyTorch / TensorFlow
- NumPy, Pandas

---

## 🚀 Notes

This project focuses on feature representation and model performance rather than interpretability.

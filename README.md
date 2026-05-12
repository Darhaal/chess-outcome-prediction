# Chess Outcome Prediction Using Early-Game Features

Supervised machine learning project for predicting chess game outcomes using early-game features extracted from Lichess PGN games.

This project was completed at Florida Institute of Technology for MTH 4224 – Intro to Machine Learning.

## Repository Description

Supervised machine learning project predicting chess game outcomes from early-game features extracted from Lichess PGN games.

## Project Overview

The goal of this project is to test whether the final result of a chess game can be predicted from early-game information.

The problem is treated as a multiclass classification task:

- Black win
- Draw
- White win

Instead of using only simple metadata, this project focuses on features extracted from the early chess position and move sequence.

The main question is:

Can machine learning models predict the outcome of a chess game from early-game features?

## Main Idea

Each chess game is parsed from PGN format and converted into a numerical feature vector.

The model only sees early-game information, so the task is difficult. A game can look balanced early and still become decisive later because of mistakes, tactics, or endgame play.

This makes the project useful as a supervised learning experiment, but the model should not be interpreted as a chess engine.

## Data

The dataset comes from publicly available Lichess PGN games.

- Source: Lichess PGN database
- Data format: PGN chess games
- Learning type: supervised classification
- Target: final game result
- Raw PGN files are not included in this repository

Raw Lichess PGN files can be large, so they should be downloaded separately from the original Lichess database if full reproduction is needed.

## Feature Engineering

The raw PGN games are processed using python-chess.

The features are designed to describe the early stage of a chess game.

Main feature groups include:

- material balance
- piece development
- pawn structure
- center control
- king safety
- castling behavior
- checks and captures
- move activity
- Stockfish evaluation
- opening information

The purpose of feature engineering is to convert chess games into a structured numerical dataset that can be used by standard machine learning models.

## Methods

This project compares supervised learning models for multiclass classification.

Possible models include:

- Logistic Regression
- Random Forest
- Support Vector Machine
- XGBoost

The models are evaluated using classification metrics such as:

- accuracy
- precision
- recall
- F1-score
- macro F1-score
- confusion matrix

Macro F1-score is important because draw games are usually harder to classify and may be less frequent than decisive outcomes.

## Explainability

Model interpretation is used to understand which early-game features are most important.

The project includes feature-importance analysis and model interpretation to check whether the model relies on meaningful chess signals such as:

- material advantage
- engine evaluation
- opening-related patterns
- center control
- king safety
- development

This is important because a model can have reasonable accuracy but still learn shortcuts or dataset-specific patterns.

## Main Findings

1. Early-game chess features contain useful information about the final game outcome.

2. Tree-based models are useful for this problem because they can capture nonlinear feature interactions.

3. Material balance and engine evaluation are strong predictive signals.

4. Draw prediction is the hardest part of the classification task.

5. The model should not be treated as a chess engine. It is a machine learning experiment on early-game prediction.

## Files in This Repository

All project files are stored in the root of the repository.

Expected files:

- README.md
- LICENSE
- NOTICE.md
- MTH4224 Project1 Report.ipynb

If the notebook file has a slightly different name, it is still the main project notebook.

## How to View the Project

The easiest way to review the project is to open the Jupyter notebook directly on GitHub.

The notebook contains the code, outputs, plots, and written analysis.

To rerun the notebook locally, open it in Jupyter Notebook or JupyterLab and run the cells in order.

## Reproducibility Notes

This repository is mainly shared as an academic and portfolio project.

To fully rerun the notebook, the user may need to manually install the Python libraries used inside the notebook.

Some experiments may require Stockfish. The Stockfish binary is not included in this repository and must be downloaded separately.

Raw Lichess PGN files are not included because they are large.

## Important Notes

This project is academic and exploratory.

The model does not calculate best chess moves. It only learns statistical relationships between early-game features and final game outcomes in the dataset.

Please do not submit this project as your own academic work.

## License

This project is licensed under the MIT License.

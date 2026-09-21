# Sign Language Flex

A prototype sign-language gesture recognition system that combines flex-sensor data, a machine-learning model, Arduino-based data collection, and a Flutter mobile interface.

> Status: Prototype / academic project

## Overview

This project explores how finger-bending data from flex sensors can be used to recognise a limited set of hand gestures. Sensor readings are collected through an Arduino setup, stored as labelled datasets, and used to train a feed-forward neural network (FNN). A Flutter application was included as the mobile-facing component of the prototype.

The goal is not to translate full sign language, but to demonstrate an end-to-end assistive-technology workflow: sensing, data collection, classification, and presentation in an application.

## My Contribution

I contributed to the development and integration of the prototype, including:

- Collecting and organising labelled flex-sensor readings
- Preparing datasets for gesture classification
- Building and experimenting with a feed-forward neural network in `FNN.ipynb`
- Working with Arduino-based sensor input
- Including a Flutter application layer for displaying or consuming gesture data
- Documenting the project and its technical limitations

## Repository Contents

| File or folder | Purpose |
|---|---|
| `FNN.ipynb` | Notebook for data preparation, model training, and evaluation experiments |
| `a.csv`, `b.csv`, `c.csv`, `d.csv` | Labelled sensor readings for the gestures included in the prototype |
| Arduino / C / C++ files | Firmware or supporting code for reading sensor values |
| Flutter files | Mobile application code for the prototype interface |
| `data_service.dart` | Flutter/Dart service for handling data in the app |

## Supported Gestures

The repository currently contains labelled datasets named `a`, `b`, `c`, and `d`.

Before publishing, replace this table with the **actual gesture meaning** for each label:

| Dataset label | Gesture meaning | Notes |
|---|---|---|
| `a` | [Add actual gesture] | [Add notes] |
| `b` | [Add actual gesture] | [Add notes] |
| `c` | [Add actual gesture] | [Add notes] |
| `d` | [Add actual gesture] | [Add notes] |

## System Design

1. Flex sensors detect bending in the fingers.
2. An Arduino reads and transmits sensor values.
3. Sensor readings are recorded and labelled by gesture.
4. The FNN model is trained on the labelled data.
5. The trained classifier predicts the gesture represented by new sensor readings.
6. The Flutter application provides a mobile interface for the prototype.

## Getting Started

### Requirements

- Python 3.9 or later
- Jupyter Notebook or JupyterLab
- Arduino IDE
- Flutter SDK, if running the mobile application

### Run the Machine-Learning Notebook

```bash
git clone [https://github.com/IreneKorir/Sign-language-Flex.git](https://github.com/IreneKorir/Sign-language-Flex.git)
cd Sign-language-Flex
pip install pandas numpy scikit-learn matplotlib jupyter
jupyter notebook FNN.ipynb
```

Run the notebook cells in order. Confirm and document any additional packages required by the notebook.

### Run the Flutter App

This repository contains Flutter files, but the app structure should be verified before use. If a complete Flutter project is present, run:

```bash
flutter pub get
flutter run
```

## Evaluation

Add the verified results from `FNN.ipynb` here.

| Metric | Result |
|---|---:|
| Number of gesture classes | [Add verified number] |
| Training samples | [Add verified number] |
| Test samples | [Add verified number] |
| Test accuracy | [Add verified result] |
| Evaluation method | [For example: train/test split or cross-validation] |

Avoid reporting training accuracy alone. Report performance on data that the model did not see during training.

## Limitations

- The system recognises only a small predefined gesture set.
- Flex sensors primarily capture finger bending; they may not capture hand orientation, position, motion, or facial expression, which are important in natural sign languages.
- Performance may change across users because hand sizes, sensor placement, calibration, and signing style differ.
- The current prototype should not be presented as a full sign-language translator.
- More participants, more gestures, and real-time testing are needed before practical deployment.

## Future Work

- Add more gesture classes and participants
- Improve sensor calibration and noise filtering
- Test cross-user generalisation
- Export and integrate the trained model into the Flutter application
- Add real-time prediction and accessibility-focused user testing
- Include a larger, well-documented dataset

## Demonstration

Add one of the following:

- A short GIF showing a gesture being recognised
- A 30–60 second demo video linked from YouTube, Google Drive, or LinkedIn
- Screenshots of the Arduino serial monitor, notebook results, and Flutter interface

Example:

```md
[Watch the project demonstration](ADD-YOUR-LINK-HERE)
```

## Ethical Note

This project is an educational prototype. Sign languages are complete natural languages, and a small sensor-based classifier cannot represent the full linguistic richness of sign-language communication.

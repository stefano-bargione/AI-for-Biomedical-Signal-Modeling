# EEG Hyperscanning ERP Classification

This module re-implements classical and deep learning pipelines for single-trial decoding of event-related potentials (ERPs) associated to higher-order socio-affective states (empathy), with a specific focus on the P300 component within a new EEG-based hyperscanning social interaction paradigm, developed under my research collaboration as PhD visiting researcher at Neuroelectrical Imaging and BCI Laboratory [NeiLab](https://www.hsantalucia.it/laboratorio-immagini-neuroelettriche-interfacce-cervello-computer) located in Fondazione Santa Lucia, Rome 

## Core Components

- Single-trial ERP extraction with emphasis on event-related oscillations (EROs)
- Targeted and joint time–frequency decomposition (delta, theta, delta+theta bands)
- Dataset construction for binary and multiclass classification tasks
- Use of:
  - Classical ML classifiers (Logistic Regression, SVM, XGBoost) combined with an [MNE-based sliding-window decoding approach](https://mne.tools/stable/generated/mne.decoding.SlidingEstimator.html) on 1D time-domain EEG representations 
  - Deep neural network architectures based on structured feature map representations:
    - Time–frequency inputs (Hybrid CNN2D-LSTM, BiLSTM, Transformer)
    - Spatial–spectral inputs (CNN3D, Separable Convolutions, Transformer)
  - AI-driven explainability analysis (Grad-CAM)

## Methodological Focus

- Temporal modeling of ERP dynamics
- Spectral feature learning
- Inter-subject variability handling
- Condition generalization across dyadic interaction contexts
- High-dimensional structured biomedical signal modeling

## Research Context

This project investigates how event-related spectral dynamics underlying the P300 component can be embedded into scalable machine learning architectures for socio-affective neural modeling.

It serves as a methodological bridge between task-specific ERP decoding and broader multimodal biomedical representation learning.

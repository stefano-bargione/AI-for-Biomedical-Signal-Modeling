# EEG Hyperscanning ERP Classification

This module re-implements classical and deep learning pipelines for single-trial decoding of socio-affective event-related potentials (ERPs), with a specific focus on the P300 component within a new developed EEG-based hyperscanning social interaction paradigm.

## Core Components

- Single-trial ERP extraction with emphasis on event-related oscillations (EROs)
- Targeted and joint time–frequency decomposition (delta, theta, delta+theta bands)
- Dataset construction for binary and multiclass classification tasks
- Use of:
  - Classical ML classifiers (Logistic Regression, SVM, XGBoost) combined with an [MNE-based sliding-window decoding approach](https://mne.tools/stable/generated/mne.decoding.SlidingEstimator.html) on 1D time-domain EEG representations 
  - Deep neural network architectures based on structured feature map representations:
    - Time–frequency inputs (Hybrid CNN2D-LSTM, BiLSTM, Transformer)
    - Spatial–spectral inputs (CNN3D, Separable Convolutions, Transformer Encoder)
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

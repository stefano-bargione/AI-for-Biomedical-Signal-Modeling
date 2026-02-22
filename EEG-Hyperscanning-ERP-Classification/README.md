# EEG Hyperscanning ERP Classification

This module re-implemented Machine and Deep Learning pipelines adopted in the Motor Intetion Decoding challange for single-trial decoding of socio-affective event-related potentials (ERPs), with a specific focus on the P300 component in newly developed EEG-based hyperscanning social interactive paradigm.

## Core Components

- Single-trial ERP extraction, with focus on multispectral components i.e. event-related oscillations (EROs) 
- Time–frequency decomposition in targeted or joint frequency ranges (delta, theta and  delta + theta bands)
- Datasets Generation for Multiclass and Binary Classification Challanges
- Use of:
-   1) Classical ML classifiers (Logistic Regression, SVM, XGBoost)
-   2) Deep Artificial Neural Network Architectures according to 1D and 2D feature map representation of brain data:
     a) Time-frequency Inputs (Hybrid CNN2D_LSTM, BiLSTM, Transformer)
     b) Spatial-spectral Inputs (CNN3D, Separable Convolutions, Transformer Encoder)
- AI-driven Explainability Data Analysis (i.e., Grad-CAM)

## Methodological Focus

- Temporal modeling of ERP dynamics
- Spectral feature learning
- Inter-subject variability handling
- Condition generalization across dyadic interaction contexts
- High-dimensional structured biomedical signals

## Research Context

This project explores how event-related spectral dynamics underlying the P300 can be embedded into scalable machine learning architectures for socio-affective neural modeling.

It serves as a methodological bridge between task-specific ERP decoding and broader multimodal biomedical representation learning.

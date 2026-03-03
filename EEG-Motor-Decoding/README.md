# EEG Motor Decoding
This module implements deep learning pipelines for single-trial EEG motor execution and motor imagery decoding, integrating explainability techniques (Grad-CAM) for model interpretation.

## Core Components
- Time–frequency and spatial–spectral representations (2D spectrogram-based inputs and 3D tensor-based volumes)
- Deep learning architectures (CNN3D, Separable Convolutions, Hybrid CNN2D-LSTM, BiLSTM, Transformer Encoder)
- Explainability analysis (Grad-CAM) for spatiotemporal and sensor-level relevance attribution driving model predictions

## Methodological Focus
- High-dimensional neural decoding
- Learning in low-sample-size regimes
- Structured temporal dependency modeling
- Inter-subject variability handling
- Interpretability constraints in biomedical AI

## Research Context
This project serves as a methodological testbed for scalable neural signal modeling architectures, with the objective of generalizing toward multimodal biomedical representation learning systems.

## PhysioNet EDF metadata
The curated .mat export does not always provide channel-name strings in a clean MNE-compatible format. For reproducibility, this project reads the exact metadata (sampling frequency and raw channel strings) from a single EDF file from the original [PhysioNet EEGMMIDB release](https://physionet.org/content/eegmmidb/1.0.0/) (e.g., S001R01.edf). This EDF is used only to retrieve sfreq and channel names; all modeling uses the curated .mat signals.

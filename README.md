# Kepler Exoplanet Detection Using Deep Learning

An independent machine learning project exploring exoplanet transit classification using NASA Kepler light curves and deep learning techniques.

**Status:** Work in progress — initial data exploration; deep learning pipeline under development.

## Project Objective

Investigate whether machine learning models can distinguish planetary transit candidates from false positives using stellar brightness measurements over time. The planned approach combines astronomical time-series preprocessing, a conventional machine learning baseline, and a one-dimensional convolutional neural network (1D CNN).

## Data

The project explores publicly available observations from NASA's Kepler mission. The planned classification pipeline will use Kepler DR24 Threshold Crossing Event (TCE) data and suitable disposition labels.

- [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)
- [MAST Portal](https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html)
- [Lightkurve documentation](https://lightkurve.github.io/lightkurve/)

## Planned Methodology

1. Explore Kepler light curves and TCE metadata.
2. Clean, phase-fold, normalize, and bin light curves.
3. Construct global and local views of transit signals.
4. Establish a gradient boosting classification baseline.
5. Develop and train a two-branch 1D CNN using global and local views.
6. Evaluate model performance using precision, recall, F1-score, confusion matrices, and precision-recall curves, with attention to class imbalance and data leakage.

## Project Progress

- [x] Initial Kepler light-curve exploration notebook
- [ ] TCE dataset exploration and label preparation
- [ ] Light-curve preprocessing pipeline
- [ ] Global and local transit representations
- [ ] Machine learning baseline
- [ ] CNN training and validation
- [ ] Model evaluation and comparison
- [ ] Reproducible training workflow and documentation

## Current Repository Structure

```text
kepler-exoplanet-detection/
├── notebooks/
│   └── 01_kepler_data_exploration.ipynb
├── .gitignore
└── README.md
```

## Technologies

Current exploration: Python, Jupyter Notebook, Lightkurve, NumPy, pandas, and Matplotlib.

Planned modeling: scikit-learn and a deep learning framework for 1D CNN training.

## Usage

```bash
git clone https://github.com/athenayun/kepler-exoplanet-detection.git
cd kepler-exoplanet-detection
```

Open the [initial exploration notebook](notebooks/01_kepler_data_exploration.ipynb) in VS Code or Jupyter. Dependency and training instructions will be expanded as the pipeline develops.

## Notes

This is an exploratory research-inspired project, not a validated astronomical discovery system. Model results and performance metrics will be documented after experiments are completed. Large datasets and model checkpoints are intended to remain outside Git version control.

# 🍇 SEDM-Vineyard

This module automates the classification of vineyards using Sentinel-2 imagery and polygon labels.

## 🔍 Features

- Load vineyard shapefiles (GeoJSON)
- Support for multi-class or binary labels (via `"Classe"` attribute or thresholds)
- Retrieve temporal satellite imagery from Sentinel Hub
- Normalize, mask, and patch data for machine learning
- Export TFRecord training sets

## 🧩 Dependencies

- Requires the base `SpaceEconomyDataManager` library
- Sentinel Hub API access for imagery download
- Optional: Optuna for hyperparameter optimization

## 🚀 Quick Start

```bash
cd SpaceEconomyDataManager
git submodule update --init --recursive
```

Then use the vineyard dashboard or CLI pipeline to build your classification dataset.

## 🧱 Module Structure

```
SEDM-Vineyard/
├── __init__.py                     # Module initializer
├── README.md                       # Module documentation
├── vineyard_dataset_builder.py    # Preprocessing and TFRecord export from vineyard polygons
├── vineyard_dashboard.py          # GUI for visual configuration and dataset generation
├── vineyard_model.py              # Model training and evaluation pipeline for vineyard classification
└── vineyard_optuna.py             # Optuna-based hyperparameter search and optimization
```

## 🍇 **File Descriptions**

| File | Description |
|------|-------------|
| `vineyard_dataset_builder.py` | Constructs ML-ready datasets from labeled vineyard polygons. Includes cropping, normalization, and TFRecord conversion. |
| `vineyard_dashboard.py` | Interactive dashboard to configure class mapping, imagery parameters, and run data pipeline. |
| `vineyard_model.py` | Defines vineyard classification models, metrics, and evaluation routines. |
| `vineyard_optuna.py` | Performs hyperparameter tuning via Optuna for model architecture or training params. |
| `README.md` | Documentation specific to the vineyard classification module. |

---


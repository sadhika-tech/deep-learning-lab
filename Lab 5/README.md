# CS3807 – Deep Learning Laboratory: Experiment 5

Comprehensive study of CNN training, regularization, optimization, hyperparameter
tuning, transfer learning and cross-validation, using **MobileNetV2** on the
**Oxford-IIIT Pet Dataset** (37 breeds, RGB, resized to 224×224×3).

## Files

| File | Description |
|---|---|
| `comprehensive_study_of_cnn_hyperparameters.ipynb` | Full notebook, run top to bottom on Kaggle |
| `README.md` | This file |
| `requirements.txt` | Requirements to install |

## Requirements

Runs on a stock Kaggle notebook. No extra installs needed — `tensorflow`,
`tensorflow_datasets`, `scikit-learn`, `pandas`, `seaborn` are preinstalled.

**Before running:**
- Settings → Accelerator → GPU (T4 x2 or P100)
- Settings → Internet → On (required for `tensorflow_datasets` to download
  Oxford-IIIT Pet on first run)

## Structure

The notebook is organized into sections that mirror the lab handout, each as
its own set of cells: build → train → combined plot → summary table.

1. **Setup** — imports, seeds, output directories
2. **Data loading** — 85/15 train/val split of the TFDS `train` split; `test`
   split
3. **Backbone** — shared frozen MobileNetV2 feature extractor
4. **Weight Initialization** — Zeros, RandomNormal, GlorotUniform, HeNormal
5. **Regularization** — none, dropout, L2, dropout+L2 (with generalization gap)
6. **Batch Normalization** — with vs. without
7. **Optimizers** — SGD, Momentum, RMSProp, Adam
8. **Hyperparameter Tuning** — learning rate, batch size, dropout rate (one factor at a time)
9. **Transfer Learning** — feature extraction vs. fine-tuning (partial unfreeze, low LR)
10. **5-Fold Cross-Validation** — 4 candidate configs, mean ± SD per fold
11. **Final Evaluation** — retrain best CV config on full training pool, evaluate once on the untouched test set (accuracy, precision, recall, F1, confusion matrix, classification report)

## Outputs

Running the notebook writes to:
- `/kaggle/working/plots/` — all figures (`.png`)
- `/kaggle/working/tables/` — all result tables (`.csv`), one per section, ready to paste into the lab report

After committing the notebook, both folders appear under the run's **Output** tab.

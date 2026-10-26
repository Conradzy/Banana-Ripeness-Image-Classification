# Banana Ripeness Image Classification

Classifies banana images into unripe, ripe, overripe, and rotten stages using transfer learning. It compares three convolutional backbones, fine-tunes the best checkpoints, and reports aggregate and per-class behavior.

## Workflow

1. Load class-organized banana ripeness images from Google Drive.
2. Build augmented train, validation, and test generators.
3. Train MobileNetV2, ResNet50, and EfficientNetB0.
4. Fine-tune upper backbone layers with early stopping.
5. Save models, labels, metrics, and evaluation graphics.

## Data Requirements

- `ripeness_dataset/` with `unripe`, `ripe`, `overripe`, and `rotten` class folders.

Datasets and generated artifacts are not included unless they are embedded directly in the notebook.

## Requirements

- TensorFlow/Keras
- scikit-learn
- pandas
- NumPy
- Matplotlib
- Seaborn

Install missing packages in your Jupyter or Google Colab environment before running the notebook.

## Running the Notebook

1. Open [`bananaripeness.ipynb`](bananaripeness.ipynb) in Jupyter Notebook or Google Colab.
2. Place any required data files in the path expected by the notebook.
3. Update local or Google Drive paths where needed.
4. Run the cells from top to bottom.

## Outputs

- `.keras` model checkpoints
- Ripeness label file
- Algorithm comparison and learning curves
- Confusion matrix and per-class metrics
- Training-results JSON

## Repository Contents

```text
.
|-- README.md
`-- bananaripeness.ipynb
```

## Notes

- This repository preserves the analysis as a notebook-first educational project.
- Results may vary with dataset versions, random splits, package versions, and available hardware.
- Review file paths and runtime-specific commands before executing outside Google Colab.

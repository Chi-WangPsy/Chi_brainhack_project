# Chi_brainhack_project
# 🧠 MEG Data in Continuous Speech

This project explores time-aligned word-level features and their relationship to MEG signals during naturalistic language listening.

## 📥 Download Dataset

Before running the notebooks, please download the **SMN4Lang** dataset from OpenNeuro:  
🔗 https://openneuro.org/datasets/ds004078

After downloading, extract the dataset **into the root of this repository**, so the folder structure looks like this:

```
your-project/
├── SMN4Lang/             ← downloaded dataset folder
├── notebooks/
├── README.md
├── environment.yml
└── ...
```

The notebooks assume this folder structure and access the MEG files via `../SMN4Lang/`.

## 🛠️ Environment Setup

To reproduce the analysis, please set up the conda environment using the provided file:

```bash
conda env create -f environment.yml
conda activate meg-analysis-env
```

Alternatively, you may install the main dependencies via pip:

```bash
pip install -r requirements.txt
```

## 🚀 How to Run

1. Launch Jupyter Notebook:

```bash
jupyter notebook
```

2. Navigate to the `notebooks/` folder and run the notebooks in order.

## 📒 Notebooks Overview

All main analyses are in the `notebooks/` folder:

- `01_alignstimuli.ipynb`: Extracts part-of-speech, word frequency, and onset time per word; exports a story-specific CSV file.
- `02_epoch.ipynb`: Reads the CSV and segments MEG signals into epochs.
- `03_POVSVM.ipynb`: Uses verbs and nouns as features for SVM classification.
- `04_TRF.ipynb`: Computes and plots TRF coefficients.

## 📚 References

- Brodbeck, C., Hong, L. E., & Simon, J. Z. (2018). Rapid transformation from auditory to linguistic representations of continuous speech. *Current Biology*, 28(24), 3976–3983.e5. https://doi.org/10.1016/j.cub.2018.10.042

- Wang, S., Zhang, X., Zhang, J., & Zong, C. (2022). A synchronized multimodal neuroimaging dataset for studying brain language processing. *Scientific Data*, 9, Article 590. https://doi.org/10.1038/s41597-022-01708-5

## 🙏 Acknowledgements

This project was developed as part of **Brainhack School 2025**.  
I would like to thank the organizers and instructors for providing comprehensive modules and guidance that made this work possible.

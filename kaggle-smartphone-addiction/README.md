# Kaggle Playground Series S6E8 — Predicting Smartphone Addiction

Hands-on binary classification study with probabilistic output, using the
[Playground Series - Season 6, Episode 8](https://www.kaggle.com/competitions/playground-series-s6e8) Kaggle competition.

## Problem

Predict, for each `id` in the test set, the **probability** of `addicted_label = 1`
(binary smartphone addiction indicator), based on screen time, sleep, notifications,
and demographic/categorical habits.

- **Target (train):** `addicted_label` — binary (`0`/`1`), imbalanced (~71% class 1).
- **Submission:** continuous probability per `id` (not the raw label).
- **Metric:** AUC (area under the ROC curve) between predicted probability and observed target — confirmed on the Kaggle *Evaluation* tab.

## Structure

```
kaggle-smartphone-addiction/
├── data/                 train.csv, test.csv, sample_submission.csv (not versioned)
├── notebooks/            exploration, modeling, and submission notebook(s)
└── README.md
```

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate          # Windows
pip install -r ../requirements.txt
```

Data downloaded via the Kaggle API:

```bash
kaggle competitions download -c playground-series-s6e8 -p data
```

(you need to accept the competition rules on the website before the download works).

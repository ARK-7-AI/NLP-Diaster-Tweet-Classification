# NLP-Diaster-Tweet-Classification

Detecting real disasters from tweets using binary text classification.

## Project Objective
This project aims to classify tweets into two categories:
- **Disaster-related** tweets (real emergency/disaster content)
- **Non-disaster** tweets (unrelated or figurative usage)

The goal is to build a robust NLP pipeline for preprocessing, feature engineering/modeling, and evaluation so predictions can support downstream monitoring and alerting workflows.

## Project Structure
```text
NLP-Diaster-Tweet-Classification/
├── data/          # datasets (kept out of version control by default)
├── src/           # training/evaluation scripts and reusable code
├── notebooks/     # exploratory analysis and experiments
├── models/        # saved model artifacts
├── reports/       # metrics, plots, and summaries
├── tests/         # unit/integration tests
├── requirements.txt
└── README.md
```

## Setup Instructions
1. **Clone repository**
   ```bash
   git clone <your-repo-url>
   cd NLP-Diaster-Tweet-Classification
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

## Training & Evaluation Commands
These are recommended baseline commands once scripts are added under `src/`.

1. **Train model**
   ```bash
   python -m src.train --train-path data/processed/train.csv --model-out models/baseline.pkl
   ```

2. **Evaluate model**
   ```bash
   python -m src.evaluate --test-path data/processed/test.csv --model-path models/baseline.pkl --report-out reports/metrics/eval.json
   ```

3. **Run tests**
   ```bash
   pytest -q
   ```

## Expected Outputs
After training/evaluation, you should expect:
- `models/`:
  - serialized model artifact(s) (e.g., `.pkl`, `.pt`)
- `reports/metrics/`:
  - evaluation metrics JSON/CSV (accuracy, precision, recall, F1)
- `reports/figures/`:
  - confusion matrix, class distribution plots, and optional error analysis visuals

> Note: dataset files, model checkpoints, and notebook checkpoints are excluded via `.gitignore`.

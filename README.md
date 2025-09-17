# NLP Sentiment Analysis with IMDb Reviews

## 📑 Overview
This project explores sentiment analysis using IMDb reviews dataset.
We compare:
- **Logistic Regression + TF-IDF** (baseline)
- **DistilBERT fine-tuning** (transfer learning)

## 📂 Project Structure
nlp-sentiment-analysis/
│
├── data/                 # Raw and processed data (ignored in GitHub)
├── notebooks/            # Jupyter notebooks
│   ├── 01_data_eda.ipynb             # Exploratory data analysis
│   ├── 02_baseline_model.ipynb       # Logistic Regression baseline
│   ├── 03_transformer_model.ipynb    # DistilBERT fine-tuning
│   └── 04_evaluation_and_reporting.ipynb # Comparison & reporting
│
├── reports/
|   ├── final_report.pdf  # Final report
│   └── figures/          # Plots and visualisations
|
│
├── src/                  # Source code (future: inference scripts, utils)
├── requirements.txt      # Project dependencies
├── README.md             # Project overview
└── .gitignore            # Ignore large/unnecessary files

## 📊 Notebooks

**01_data_eda.ipynb**
- Load IMDB dataset
- Explore class balance, review lengths, sample text

**02_baseline_model.ipynb**
- Feature extraction with TF–IDF
- Logistic Regression classifier
- Accuracy ~89%

**03_transformer_model.ipynb**
- Tokenisation with DistilBERT tokenizer
- Fine-tuned DistilBERT for sentiment classification
- Accuracy ~87% (subset, 2 epochs)

**04_evaluation_and_reporting.ipynb**
- Aggregate results
- Compare Logistic Regression vs DistilBERT (Accuracy, Precision, Recall, F1)
- Visualisation + analysis
- Discussion on trade-offs and future improvements

## 📈 Results  

| Model                   | Accuracy | Precision | Recall | F1   |
|-------------------------|----------|-----------|--------|------|
| Logistic Regression     | 0.892    | 0.89      | 0.89   | 0.89 |
| DistilBERT (subset, 2e) | 0.870    | ~0.86     | ~0.87  | ~0.87 |

![Model Comparison](reports/figures/model_comparison.png)

## 🚀 Future Work
- Train DistilBERT on full dataset
- Try BERT-base / RoBERTa
- Advanced evaluation (confusion matrices, ROC-AUC)
- Inference script for new reviews
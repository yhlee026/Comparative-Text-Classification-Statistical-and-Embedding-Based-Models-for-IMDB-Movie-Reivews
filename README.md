# IMDB Sentiment Analysis

A comparison of two sentiment-analysis methods on the IMDB movie-review dataset:

* **Logistic Regression + TF–IDF**
* **Fine-tuned BERT**

## Installation

```bash
git clone https://github.com/YOUR-USERNAME/REPO.git
cd REPO
python -m venv venv && source venv/bin/activate  # Windows: venv\\Scripts\\activate
pip install -r requirements.txt
```

## Usage

```bash
# Preprocess data
python src/preprocess.py --input_dir dataset --output_dir processed_data

# Train baseline model
python src/baseline.py --data_dir processed_data

# Fine-tune BERT
python src/bert_train.py --data_dir processed_data --output_dir models/bert
```

## Project Structure

```
dataset/            # Raw IMDB reviews
processed_data/     # Cleaned data
src/                # Scripts
notebooks/          # Optional analysis notebooks
requirements.txt    # Dependencies
README.md           # Project overview
```

## License

MIT © yhlee026

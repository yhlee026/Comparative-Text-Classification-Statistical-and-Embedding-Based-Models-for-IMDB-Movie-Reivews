# CM3060 NLP Mid-Term: IMDB Sentiment Analysis

This project implements and compares two text-classification approaches on the IMDB movie-review dataset:

* **Logistic Regression + TF–IDF**
* **Word2Vec Embeddings + Neural Network**

## Requirements

* Python 3.7+
* numpy, pandas, scikit-learn, nltk, gensim, tensorflow, matplotlib

Install dependencies with:

```bash
pip install numpy pandas scikit-learn nltk gensim tensorflow matplotlib
```

## Dataset

Download the IMDB dataset from the Stanford AI Lab:
[https://ai.stanford.edu/\~amaas/data/sentiment/](https://ai.stanford.edu/~amaas/data/sentiment/)
and extract into a `dataset/` directory with subfolders:

```
dataset/
  train/pos
  train/neg
  test/pos
  test/neg
```

## Usage

Launch Jupyter and open the notebook:

```bash
jupyter notebook CM3060_NLP_MID_TERM.ipynb
```

Run all cells to preprocess data, train models, and view outputs.

## Project Structure

```
dataset/                       # IMDB raw reviews
CM3060_NLP_MID_TERM.ipynb      # Main analysis notebook (also provided as HTML)
requirements.txt               # Python dependencies
```

## Methodology

1. **Preprocessing**

   * Tokenization, lowercasing, stop-word removal, and lemmatization using NLTK fileciteturn2file10

2. **Baseline Model**

   * TF–IDF vectorizer (max\_features=5000) + Logistic Regression (max\_iter=1000) fileciteturn2file2turn2file4

3. **Embedding Model**

   * Train Word2Vec (vector\_size=100, window=5) on cleaned tokens, then define a Sequential neural network with an Embedding layer and GlobalAveragePooling1D fileciteturn2file12

## Results

* **Logistic Regression** achieved \~54% accuracy with precision 0.55/0.54 and recall 0.48/0.60 on negative/positive classes fileciteturn2file13
* **Embedding-based model** demonstrated stronger true positive and true negative counts, reflecting richer semantic features captured by Word2Vec embeddings.

## License

MIT License © yhlee027

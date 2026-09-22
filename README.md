# AI Engineering Practice Lab

![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white)
![NLP](https://img.shields.io/badge/Focus-NLP-8A2BE2)
![Notebooks](https://img.shields.io/badge/Jupyter-8_notebooks-F37626?logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

My **learning-in-public practice lab** for AI engineering fundamentals — hands-on Jupyter notebooks working through the core NLP stack (NLTK, spaCy, gensim, scikit-learn, Hugging Face) plus supporting numerical computing. These are living study notes: written for revision and muscle memory before applying the techniques in real projects.

## Notebook index

| Notebook | Topics covered | Key libraries |
|---|---|---|
| [`3.01_Numpy_Introduction.ipynb`](3.01_Numpy_Introduction.ipynb) | NumPy fundamentals — ndarray creation (0D–3D), array operations | NumPy |
| [`NLP.ipynb`](NLP.ipynb) | Core text preprocessing — lowercasing, stop words, regex cleaning, tokenization, stemming vs. lemmatization | NLTK, spaCy |
| [`NLP_POS_NER.ipynb`](NLP_POS_NER.ipynb) | Preprocessing pipeline extended with part-of-speech tagging and named-entity recognition | NLTK, spaCy |
| [`NLP_master_notes.ipynb`](NLP_master_notes.ipynb) | Consolidated NLP reference notes covering the full preprocessing toolkit | NLTK, spaCy |
| [`Practice_LSA_VS_DSA.ipynb`](Practice_LSA_VS_DSA.ipynb) | Topic modelling deep dive — TF‑IDF, LDA vs. LSA, `doc2bow`, coherence scores for choosing *k*, plus a logistic-regression text classifier | gensim, scikit-learn, NLTK |
| [`Practice_Text_Classification.ipynb`](Practice_Text_Classification.ipynb) | Practice run: bag-of-words / TF‑IDF features and topic modelling on customer-feedback text | gensim, scikit-learn |
| [`Text_classifier.ipynb`](Text_classifier.ipynb) | Custom text classifiers — TF‑IDF + Logistic Regression and Multinomial Naive Bayes, with train/test evaluation | scikit-learn, gensim |
| [`Sentiment_Analysis_Pratical.ipynb`](Sentiment_Analysis_Pratical.ipynb) | Three approaches to sentiment analysis compared — lexicon-based (VADER), transformer pipeline (Hugging Face), and a trained NLTK Naive Bayes classifier on book reviews | vaderSentiment, transformers, NLTK |

> **Note:** `Sentiment_Analysis_Pratical.ipynb` expects a local `book_reviews_sample.csv` (an Amazon book-reviews sample) that is not committed to the repo — drop your own copy alongside the notebook to re-run it.

## Concepts practiced

- **Text preprocessing:** normalization, stop-word handling, punctuation stripping, tokenization, stemming (Porter) vs. lemmatization (WordNet)
- **Feature engineering for text:** bag-of-words, TF‑IDF, gensim dictionaries and `doc2bow`
- **Topic modelling:** Latent Dirichlet Allocation vs. Latent Semantic Analysis, SVD intuition, picking the number of topics with coherence scores
- **Classification:** logistic regression, Multinomial Naive Bayes, train/test splits, accuracy and classification reports
- **Sentiment analysis:** rule-based (VADER) vs. pretrained transformers vs. classic ML — trade-offs of each
- **Tagging:** POS tagging and NER with spaCy's `en_core_web_sm`

## Environment setup

```bash
git clone https://github.com/adityashroff06-code/AI_ENGG_PRATICE.git
cd AI_ENGG_PRATICE

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# one-time model/corpus downloads
python -m spacy download en_core_web_sm
python -c "import nltk; [nltk.download(p) for p in ('punkt', 'stopwords', 'wordnet')]"

jupyter notebook
```

## License

Released under the [MIT License](LICENSE).

## Author

**Aditya Shroff** — [GitHub](https://github.com/adityashroff06-code) · [LinkedIn](https://www.linkedin.com/in/aditya-shroff-8033a31b0)

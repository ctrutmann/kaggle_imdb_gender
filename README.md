# How movie reviews describe men and women (2016)

An early exploration of gendered language by [Christel Trutmann](https://christeltrutmann.com/), from August 2016.

## The question

What does a language model learn about men and women from how people write about movies? I trained a word2vec model on 75,000 IMDB movie reviews. Word2vec places words close together when they appear in similar contexts. I then asked which words are closest to "man" and to "woman."

## What it found

The 12 nearest words to each, in order of similarity:

| Closest to "man" | Closest to "woman" |
|---|---|
| woman | lady |
| lady | prostitute |
| lad | girl |
| guy | widow |
| millionaire | man |
| monk | heiress |
| sailor | housewife |
| soldier | waitress |
| men | nun |
| person | nurse |
| farmer | maid |
| chap | whore |

Further down the lists the pattern continues. Near "man": businessman, doctor, poet, lawyer, journalist, scientist, politician. Near "woman": slut, stripper, hooker, virgin, spinster, "sexually." Men tend to be described by what they do. Women tend to be described by their relationships, their sexual availability, and service roles.

The full top-50 lists are in the notebook.

## About the code

[`docs/notebooks/Kaggle Part 2 - Word Vectors.ipynb`](docs/notebooks/Kaggle%20Part%202%20-%20Word%20Vectors.ipynb) is kept as it was written in 2016. The data loading, text cleaning and model training follow Part 2 of Kaggle's ["Bag of Words Meets Bags of Popcorn"](https://www.kaggle.com/c/word2vec-nlp-tutorial) tutorial. The gender questions at the end are my own. The 2D plot at the very end was an unfinished experiment.

The notebook is Python 2 and won't run on a current setup without updating. It also doesn't include the review data, which can be downloaded from the Kaggle tutorial page (`labeledTrainData.tsv` and `unlabeledTrainData.tsv`).

This is one model trained on one corpus, not a controlled study. Results like these depend on the data and settings, and IMDB reviewers aren't a representative sample of anyone. Still, the pattern is consistent with later published work on gender bias in word embeddings.

## Where it led

This exploration was a starting point for my later writing on gendered sexual language and for an NLP independent study at the University at Albany (2025). More at [christeltrutmann.com](https://christeltrutmann.com/).

## Acknowledgments

Thanks to Noble Kennamer, who walked me through this project when I was just learning to code.

## License

GPL-3.0. See [LICENSE](LICENSE).

---
layout: post
title: Experiments on Paraphrase Identification using Quora Question Pairs
---

We modeled the Quora question pairs dataset to identify a similar question. 
The dataset that we use is provided by Quora. The task is a binary classification. 
We tried several methods and algorithms and different approach from previous works.
For feature extraction, we used Bag of Words including Count Vectorizer, and Term Frequency-Inverse Document
Frequency with unigram for XGBoost and CatBoost.
Furthermore, we also experimented with WordPiece tokenizer which improves the model performance significantly. 
We achieved up to 97 percent accuracy. 
[Code and Dataset](https://github.com/jakartaresearch/quora-question-pairs)
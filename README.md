# nlp-getting-started

Модель машинного обучения, которая предсказывает, какие твиты посвящены реальным бедствиям, а какие нет.

## Cloud of words

### Keywords

<p align="center">
    <img width="100%" src="images/cloud-keywords.PNG" style="max-width:100%;"></a>
</p>

### Locations

<p align="center">
    <img width="100%" src="images/cloud-locations.PNG" style="max-width:100%;"></a>
</p>

## EDA

### Target and not target records count

<p align="center">
    <img width="100%" src="images/records.PNG" style="max-width:100%;"></a>
</p>

### Keywords statistics

<p align="center">
    <img width="100%" src="images/keywords.PNG" style="max-width:100%;"></a>
</p>

### Locations statistics

<p align="center">
    <img width="100%" src="images/locations.PNG" style="max-width:100%;"></a>
</p>

### Disaster and Non Disaster tweets length

<p align="center">
    <img width="100%" src="images/tweets.PNG" style="max-width:100%;"></a>
</p>

### Disaster and Non Disaster word length

<p align="center">
    <img width="100%" src="images/words.PNG" style="max-width:100%;"></a>
</p>

## Methods description

### CountVectorize

Convert a collection of text documents to a matrix of token counts.

### TF-IDF

Count Vectorizer give number of frequency with respect to index of vocabulary where as tf-idf consider overall documents of weight of words

### GloVe

GloVe stands for global vectors for word representation. It is an unsupervised learning algorithm developed by Stanford for generating word embeddings by aggregating global word-word co-occurrence matrix from a corpus. The resulting embeddings show interesting linear substructures of the word in vector space.

### BERT

Splitting a word into a vector of 32 numbers. Search for suitable words by measuring the distance between the axes of vectors
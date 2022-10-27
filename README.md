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

### Text

<p align="center">
    <img width="100%" src="images/cloud-text.PNG" style="max-width:100%;"></a>
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

В данном подходе входные данные токенизируются и представляются в виде словаря. 
А затем документ представляется, используя этот словарь.

У CountVectorize есть несколько параметров:
- max_features — построенный словарь будет содержать только n самых часто встречающихся в корпусе токенов, отсортированных по частоте.
- min_df — при построении словаря будут игнорироваться слова из текстов, частота которых строго ниже заданного порогового значения.
- max_df — при построении словаря будут игнорироваться слова из текстов, частота которых строго выше заданного порогового значения.

### TF-IDF

Count Vectorizer give number of frequency with respect to index of vocabulary where as tf-idf consider overall documents of weight of words

Подход чем то похож на CountVectorize, только здесь для каждого токена используется метрика
TF-IDF. 

- Частота слова (Term Frequency) — подсчитывает, как часто выбранное слово появляется в документе.

- Обратная частота документа (Inverse Document Frequency) — снижает вес слов, которые часто встречаются в документах.

### GloVe

GloVe stands for global vectors for word representation. It is an unsupervised learning algorithm developed by Stanford for generating word embeddings by aggregating global word-word co-occurrence matrix from a corpus. The resulting embeddings show interesting linear substructures of the word in vector space.

### BERT

Splitting a word into a vector of 32 numbers. Search for suitable words by measuring the distance between the axes of vectors


### Про метрики
Для данной задачи наиболее интересны метрики Recall и Roc Auc Score. Ведь нам важно определить 
как можно больше бедствий из твитов, и не так страшно, если какой то твит будет опознан ложно положительно.
Ведь страшнее не узнать о катастрофе, чем получить ложную тревогу.
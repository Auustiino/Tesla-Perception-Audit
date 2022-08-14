
# Tesla-Perception-Audit
### An audit of the publics perception of Tesla 

## Summary

The goal with this project is to explore to what extenet public sentiment and discourse can be captured surrounding Tesla Inc. What topics surrounding Tesla concern the public the most and how are these topics being discussed. 


# The Data, Preperation and EDA

## Data

The Data was sourced from the Twitter API, ranging from 5.9.2022 - 6.1.2022 
** Example Queries: **
1. tesla
2. tesla -@elonmusk
3. tesla cars

## Preperation

Preprocessing steps were applied to each of the documents, these steps included:

- Removal of stop words
- Lemmatization, utilizing a Part of Speech tagging function to imporove quality of lemmatization 
- Creation of bigrams and trigrams
- Tokenization
- Removal of tweets shorter than 5 tokens
- Removal of tokens appearing in less than 10 documents or in more than 95% of documents

## EDA

Show Tweet lengths (Character word plot)

**Document Lengths**

Initial EDA reveals a potential issue moving forward with the project; the documents are all quite short.

<img src = 'img/TP-doc-lengths.png' alt = 'Document Lengths' height = '600' width = '800'>


Show Sentiment Distribution (Only if Sentiment is to be removed from the final plot, make a new final plot)

**Sentiment Distribution**

Exploring the distribution of document sentiments reveals the vast majority of documents have been given a sentiment of **0.00**
This, along with several other issues wihtin this project can be attributed to the data being made up of very short documents, made even shorter by the preprocessing steps to remove stop words and most / least frequent words. These short documents do not contain substantive information, resulting in perfectly neutral sentiments. 

<img src = 'img/original-sent-distribution.png' alt = 'Sentiemnt Distributions' height = '600' width = '800'>



And here's a cool WordCloud

<img src = 'img/Tesla-wordcloud.png' alt = 'Cool WordCloud of Common Words' height = '600' width = '800'>


## Useful Findings

Show final graph with removed 0 sentiment Values

<img src = 'img/fin-sent-axes.png' alt = 'Final Sentiments' height = '600' width = '800'>

Show topic keywords and then explanations

<img src = 'img/Topic-Keywords.png' alt = 'Final Sentiments' height = '200' width = '600'>


## Improvements

The Data
From the beginning, knowing how LDA works (prove this before posting) I should have known that using tweets with a max character count of 140 and an average word length of XX that LDA for Topic Modeling wpuld not work. Other Topic Modeling algorithims were tried (like GSDMM) but were equally unsuccesful is getting coherent topics



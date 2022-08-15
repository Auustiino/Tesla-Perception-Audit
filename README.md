
# Tesla-Perception-Audit
### An audit of the publics perception of Tesla 

## Summary

The goal with this project is to explore to what extenet public sentiment and discourse can be captured surrounding Tesla Inc. What topics surrounding Tesla concern the public the most and how are these topics being discussed. 


# The Data, Preperation and EDA

## Data

The Data was sourced from the Twitter API, ranging from 5.9.2022 - 6.1.2022 

**Example Queries:**
- tesla
- tesla -@elonmusk
- tesla cars

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

## Topic Interpretations 
- **Topic 0 Sentiment: 0.185**

These Keywords give a sense that the company Tesla Inc. is good for the world and helps people. 
This evaluation correlates to the sentiment value of the topic, being the second most positive of all the categories.  


- **Topics 1/2 Sentiments:  0.038/0.013**

Neither of these topics are particularly coherent, topic 1 has the words ‘get’, ‘open’, and ‘fire’ which could be referring to a Tesla car fire in which the door was stuck closed with the driver inside. If so, the topic is being discussed not only in a non-negative way but in a slightly positive neutral way. Topic 2 mentions SpaceX and Ford, both of which are entirely unrelated, with a very sentiment. 


- **Topic 3 Sentiment: 0.062**

A topic consisting of tweets concerning the relationship of both Tesla and Twitter to the stock market, 
Chatter related to twitter itself inevitably makes it’s way into the queries due to the link between Elon Musk, Tesla Inc. and Twitter.
This topic is slightly above neutral sentiment, notably not negative,  indicating no strong feelings in the aggregate surrounding Tesla’s and Twitters relationship with the stock market. 

- **Topic 4 Sentiment: 0.199**

A topic surrounding specifically Tesla’s electric vehicles
This topic is noticeably more positive than the others, indicating that in general discourse surrounding Tesla’s electric vehicles skews more positively


## Summary 

Tesla inc.’s cars, stocks and positive impact dominated the discussion surrounding the company during the period in which the data was collected. We learned that the company’s positive impact and electric vehicles are discussed most positively although with the sentiment scale being (-1, 1) receiving a 0.2 is still not amazing. We suggest the company focus on emphasizing their positive contributions to society. We also learned that an incident in which a Tesla vehicle caught fire, trapping a passenger inside, made a ripple in online discussion. Although the topic was not evaluated to be being discussed in a negative way, this incident could reduce a potential customer’s confidence in the vehicles, raising questions about safety. This issue should be addressed directly. 



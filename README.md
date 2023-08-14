# Topic-Modeling
[![Follow](https://img.shields.io/twitter/follow/gensim_py.svg?style=social&style=flat&logo=twitter&label=Follow&color=blue)](https://twitter.com/KAfzalnia76689)

Topic Modeling Using LDA algorithm
## Installation
LDA algorithm require gensim 3.8.3 and this version of gensim need to run in python=<3.6
```bash
pip install gensim==3.8.3
```
## Usage
```python
ldamallet = gensim.models.wrappers.LdaMallet(mallet_path, corpus=corpus, num_topics=20, id2word=id2word)
```
## Abstract
Topic Modeling is a technique to extract the hidden topics from large volumes of text.Topic Models are very useful for the purpose for document clustering, organizing large blocks of textual data, information retrieval from unstructured text and feature selection.

Here I use [LDA](https://jonathan-hui.medium.com/machine-learning-latent-dirichlet-allocation-lda-1d9d148f13a4) algorithm to do the topic modeling and use pyLDAvis and other tools to interpret and visualize the results.
## Notebook Outline:
- Environment set-up
- Loading Data and get a brief overview of columns
- Preprocessing and EDA
- Topic Moodeing Using LDA algorithm
## Dataset
I have taken review data from [Trustpilot.com](https://www.trustpilot.com/). It consists of about 2000 reviews of various UK train companies. The data is stored in a JSON file and contains the comment itself, when it was submitted, to which site it was submitted, and the review scores the user gave.
## Concluding Topics
- **TOPIC 0:** It's  about customer experience during the travel(toilet, carriage, passenger, ...) like how staff treat passengers, the timing of travel(whether it has delay or not), hygienic services like toilets, seats and the wifi conncetion, interenet.
- **Topic 1:** It's about the user experience of their webistes and the qulity of servies provided on webiste like getting ticket, choosing seats and cost of travels and services.
- **Topic 2:** It's about the services that passengers recieve before or after the trip regarding to ticket and other after/before sales services. It's also about booking tickets, refund and retuning tickets and how service providers handle canceling tickets and trip due to bad whether or unexpected events

Note that I could increase topic number but after some test/run I observe that we had overlap in topic semantics so by choosing 3 topics we have the most distinct topics(as I illusterated in pyLDAvis graph).
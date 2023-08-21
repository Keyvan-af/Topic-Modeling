# Topic-Modeling
[![Follow](https://img.shields.io/twitter/follow/gensim_py.svg?style=social&style=flat&logo=twitter&label=Follow&color=blue)](https://twitter.com/KAfzalnia76689)

Topic Modeling with the LDA algorithm. ([Notebook](https://drive.google.com/file/d/1L5P8gwKOY_vhvBpp-rZ1yShBQKSs5X6w/view?usp=sharing))
## Installation
The LDA algorithm requires gensim 3.8.3 and this version of gensim must run in python=<3.6
```bash
pip install gensim==3.8.3
```
## Usage
```python
import gensim.corpora as corpora
from gensim.utils import simple_preprocess
from gensim.models import CoherenceModel
```
## Summary
Topic Modeling is a technique for extracting hidden topics from large amounts of text.Topic Models are very useful for clustering documents, organizing large blocks of textual data, extracting information from unstructured text and feature selection.

Here I use the [LDA](https://jonathan-hui.medium.com/machine-learning-latent-dirichlet-allocation-lda-1d9d148f13a4) algorithm for topic modeling and use pyLDAvis and other tools to interpret and visualize the results.
## Dataset
I have taken review data from [Trustpilot.com](https://www.trustpilot.com/). It consists of about 2000 reviews of various UK train companies. The data is stored in a JSON file and includes the comment itself, when it was submitted, to which site it was submitted, and the review scores the user gave.
## Concluding Topics
- ** TOPIC 0:** It's about the customer experience during the trip (toilet, carriage, passenger, ...), how the staff treats the passengers, the timing of the trip (whether there are delays or not), hygienic services such as toilets, seats and the wifi connection, internet.
![](https://github.com/Keyvan-af/Topic-Modeling/blob/main/Top%20keywords%20of%20topic%200.png)
- **Topic 1:** It's about the usability of the websites and the quality of the services offered on the website, such as ticket purchase, seat selection and cost of the trips and services.
![](https://github.com/Keyvan-af/Topic-Modeling/blob/main/Top%20keywords%20of%20topic%201.png)
- **Topic 2:** It's about the services that passengers receive before or after travel in terms of tickets and other after/before sales services. It's also about ticket booking, ticket refunds and returns, and how service providers handle ticket and trip cancelations due to bad weather or unexpected events
![](https://github.com/Keyvan-af/Topic-Modeling/blob/main/Top%20keywords%20of%20topic%202.png)
Note that I could increase the number of topics, but after some testing/running I found that there is overlap in the semantics of the topics, so by choosing 3 topics we have the clearest topics (as I illustrated in the pyLDAvis diagram).
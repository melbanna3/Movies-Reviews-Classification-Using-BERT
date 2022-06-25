# Movies-Reviews-Classification-Using-BERT

IMDB is the most globally famous movie reviews website where you can publish a review for
any film you watched. Classifying the positive reviews and the negative ones can be useful for
several purposes such as giving an overall rating for the film or making statistical analysis about
the preferences of people from different countries, age levels, etc... So IMDB dataset is released
which composed of 50k reviews labeled as positive or negative to enable training movie reviews
classifiers. Moreover, NLP tasks are currently solved based on pretrained language models such
as BERT. These models provide a deep understanding of both semantic and contextual aspects
of language words, sentences or even large paragraphs due to their training on huge corpus for
very long time. In this assignment you will download the IMDB dataset from kaggle using this
Link. Then, you will train BERT based classifier for movie reviews.

Dataset Link: https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

## Text pre-processing

Text pre-processing is essential for NLP tasks. So, you will apply the following steps on
our data before used for classification:

(a) Remove punctuation.

(b) Remove stop words.

(c) Lowercase all characters.

(d) Lemmatization of words.

We used NLP library such as nltk to pre-process the data

## Classification using BERT

We build a classifier model based on BERT. We used transformers library
supplied by hugging face to get a pretrained and ready version of BERT model. It helped us 
to tokenize the input sentence in the BERT required form and to pad the
short sentences or trim the long ones. We used the CLS token embedding outputs of
BERT as input to the hidden dense classification layers we need to add after BERT. This
embedding is of size 768.
We added 4 hidden layers of 512, 256, 128, 64 units respectively before the output
layer. We used binary cross entropy loss and adam optimizer.

This Project worked with pre-processed data and data withoud pre-processing, also e compared between them 

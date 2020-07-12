> capture data.

> cleaning   (web scrapping and remove <html> tag).

> Normalization  Tokenization  (a fancy word of symbol, `nltk `) 

> Stop word removal 

> Sentence Parsing 

> Stemming & LEmmatization


## Text procesing (see text_cleaning.ipynb)
  * capture and cleaning 

### Part-of-Speech Tagging
  * normization 
  * tokenization
  * stop pword removal
    ```words = [w for w in words if w not in stopwords.words("english")]```
  * part-of-Speech Tagging
    ``` python
    from nltk import pos_tag
    sentence = word_tokenize("i always lie down to tell a lie")
    pos_tag(sentence)
    ```


Note: Part-of-speech tagging using a predefined grammar like this is a simple, but limited solution. It can be very tedious and error-prone for a large corpus of text, since you have to account for all possible sentence structures and tags!

There are other more advanced forms of POS tagging that can learn sentence structures and tags from given data, including Hidden Markov Models (HMMs) and Recurrent Neural Networks (RNNs).

### Name Entiy Recongition

``` python
# Named Entity Recongnition
from nltk import pos_tag, ne_chunk
from nltk.tokenize import word_tokenize

ne_chunk(pos_tag(word_tokenize("Antonio joined Udacity Inc. in California")))
```
### Stemming and Lemmatization
caching, cached, caches -> cache

#### Stemming

``` python
from nltk.stem.porter import PorterStemmer
# Reduce words to their stems
stemmed = [PorterStemmer().stem(w) for w in words

```

#### Lemmatization
is, was, were ---> be 
change the word become the root form
``` python
from nltk.stem.wordnet import WordNetLemmatizer
# Reduce words to their stems
lemmed = [WordNetLemmatizer().lennatize(w) for w in words ]
print(lemmed)

```
Stemming change word into simple form
Stemming does not require dictionary but Lemmatization will change to words to root from,


## Summary
# 1. Nomalize -> Tokenize -> Remove Stop Words -> Stem/Lemmatize
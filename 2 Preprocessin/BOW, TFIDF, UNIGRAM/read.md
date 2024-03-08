
# Bag of Words, TF-IDF, and Unigrams in Natural Language Processing (NLP)
## Introduction
In Natural Language Processing (NLP), we often need to convert text data into numerical representations that machine learning algorithms can understand. Bag of Words (BoW) and Term Frequency-Inverse Document Frequency (TF-IDF) are two common techniques used for this purpose. Let's explore these concepts in a simple and easy-to-understand way.

## Bag of Words (BoW)
Bag of Words is a simple technique where we represent text data as a collection of words, ignoring grammar and word order. We create a vocabulary of unique words present in the entire corpus and then count the frequency of each word in each document.

## TF-IDF (Term Frequency-Inverse Document Frequency)
TF-IDF is a more advanced technique that not only considers the frequency of words in a document but also takes into account how important a word is in the entire corpus. It assigns higher weights to words that are more unique to a document and less common in other documents.

## Unigrams
Unigrams are simply individual words or tokens in a piece of text. In the context of BoW and TF-IDF, we consider each word as a unigram.

## Examples
Let's understand Bag of Words, TF-IDF, and unigrams with some examples:

## Bag of Words (BoW) Example:
Consider the following two sentences:

"The cat sat on the mat."
"The dog jumped over the fence."
Using Bag of Words, we create a vocabulary of unique words:

The
cat
sat
on
mat
dog
jumped
over
fence
Now, we represent each sentence based on the frequency of these words:

[1, 1, 1, 1, 1, 0, 0, 0, 0]
[1, 0, 0, 0, 0, 1, 1, 1, 1]

## TF-IDF Example:
Let's use the same sentences as before. We calculate TF-IDF scores for each word in each sentence. TF-IDF values are calculated based on the frequency of a word in a document and the frequency of the word across all documents.

Unigrams Example:
Unigrams are simply individual words. 


## Lets get deeper on the TFIDF part, there is a bit of math involved.
TF measures the frequency of a term (word) within a document. It is calculated using the following formula:
**_TF= n/N_** ,
 where n is the number of times a term(word) of our interest appears in a document and N is the total number of words or term in the document. 
 
 The term frequency TF represents the ratio of the number of occurrences of term _t_ to the total number of terms in document _d_.Essentially, TF measures how often a term appears in a document relative to the total number of terms in that document.


And **_IDF = log( Nd/Dt)_**
 where _Nd_ is the total number of documents and _Dt_ is the number of documents containing the term _t_.
 Obtained by taking the logarithm of the ratio of the total number of documents to the number of documents containing term _t_. This logarithmic transformation helps in giving more weight to terms that are rare across documents.


TFIDF = TF X IDF

**eg: Let's consider a simple example with two documents:**

Document 1: "The quick brown fox"
Document 2: "The lazy dog"
Suppose we want to calculate the TF-IDF score for the term "fox". We would perform the following steps:

TF of fox in first doc = 1/4
Tf of fox in second doc = 0 since there is no fox in the second doc

Now IDF = log(2/1) since there are ttwo documents and fox appears in one doc 

TFIDF for doc 1 = (1/4)x log(2)
TFIDF for doc 2 = 0


Refer to the ipynb file in the same folder for codes


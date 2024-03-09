Before we jump into word2vec we will define what is _neural word embeddings_. part of text preprocessing in natural language processing (NLP). They play a crucial role in representing words as dense vectors in a continuous vector space, capturing semantic relationships between words based on their context.
Neural word embeddings, such as Word2Vec, GloVe (Global Vectors for Word Representation), and fastText, are typically generated using deep learning models trained on large corpora of text data. These embeddings are learned in an unsupervised manner and can be used as feature representations for downstream NLP tasks, such as sentiment analysis, text classification, and machine translation.

# Here's how neural word embeddings fit into the text preprocessing pipeline:

**Tokenization**: The text data is tokenized into individual words or subword units, depending on the specific tokenization strategy used.

**Word Embedding Generation**: Neural word embeddings are generated using deep learning models trained on the tokenized text data. These models learn to represent each word as a dense vector in a continuous vector space.

**Embedding Lookup**: During text preprocessing, the pre-trained word embeddings are looked up for each word in the input text. This step transforms the input text into a sequence of dense vectors, where each vector represents a word in the text.

**Padding and Truncation**: If necessary, padding or truncation may be applied to ensure that all input sequences have the same length, which is often required for training neural networks.

**Normalization**: The word embeddings may be normalized to ensure that they have similar scales, which can improve the stability and convergence of neural network training.

**Data Splitting**: Finally, the preprocessed text data, along with their corresponding labels (if available), are split into training, validation, and test sets for model training and evaluation.

Neural word embeddings are an essential component of text preprocessing in NLP, as they provide a dense and semantically meaningful representation of words, which can capture complex linguistic relationships and improve the performance of downstream NLP tasks.

**Now lets jump to the most commonly used ones:**
Word2Vec is a popular technique used in natural language processing (NLP) to learn distributed representations of words in vector space. It represents each word as a dense vector in a continuous vector space, where the similarity between words is captured based on their context in a given corpus.

# Word2Vec:
Word2Vec is based on the idea that words appearing in similar contexts tend to have similar meanings. It learns distributed representations of words by training a neural network on a large corpus of text. There are two main architectures for Word2Vec:

_Continuous Bag of Words (CBOW)_: This architecture predicts the target word based on its context (surrounding words).

_Skip-gram_: This architecture predicts the surrounding words given a target word.

After training, each word in the vocabulary is represented as a dense vector of fixed dimensionality (e.g., 100, 200, 300 dimensions), where words with similar meanings are closer together in the vector space.

# Average Word2Vec:
Average Word2Vec is a simple approach to represent a piece of text (sentence, paragraph) using Word2Vec word embeddings. Here's how it works:

For each word in the text, obtain its pre-trained Word2Vec vector representation.
Compute the average of all these vectors to get a single vector representation for the entire text.
This average vector represents the "meaning" or "context" of the text in the Word2Vec vector space.

_refer the notebook in the folder for code_


**_A few extra stuff related to neural word embeddings that you might want to learn because this doc is a rrefletion of what i am learning( won't get into too much of  details)_**

**GloVe (Global Vectors for Word Representation)**: GloVe is a word embedding technique used to obtain vectors for words, however it takes a different approach when compared to word2vec in training word embeddings.
GloVe is trained using a global matrix factorization technique. It constructs a co-occurrence matrix X where Xij represents the number of times word j appears in the context of word i . The model then learns to  factorize this matrix into word vectors. 
    
when it comes to _loss function_ GloVe optimizes a loss function that measures how well the dot product of word vectors matches the logarithm of the co-occurrence probabilities. The loss function encourages word vectors to capture the semantic relationships between words based on their co-occurrence statistics. Now this might go a bit over the head so let me simplify it.

Imagine you have a bunch of words like "cat," "dog," "ball," and "run" that you want the computer to understand better. Now, let's play a game with these words!

First, we want to know how often these words hang out together. For example, when someone says "cat," the word "dog" might come up a lot, right? So, we count how many times "cat" and "dog" are mentioned together in some sentences.

Now, let's imagine each word has its own secret code. We want to make sure these secret codes help us understand how words are related to each other. So, we want the computer to find the best codes for each word.

Here's the tricky part: we want the computer to figure out these codes by looking at how often words hang out together. If "cat" and "dog" are mentioned together a lot, their secret codes should be similar somehow.

Now, we need a way to tell the computer how good its codes are. We use a special trick called a loss function. It's like a game score that tells the computer how close its secret codes are to what we want.

In our game, we want the computer to make the dot product of the secret codes for "cat" and "dog" closer to how often they hang out together. If "cat" and "dog" are mentioned together a lot, the dot product should be high. If they're not mentioned together much, the dot product should be low.

So, our loss function checks how well the dot product matches how often words hang out together. If the dot product and the real hanging-out-together numbers match well, the computer gets a good score. If they don't match, the computer tries to adjust its secret codes to do better in the next round of the game.

In simple words, the computer learns to make secret codes (word vectors) that help us understand how words are related by playing this game and trying to make the dot product of the codes match how often words hang out together in sentences.






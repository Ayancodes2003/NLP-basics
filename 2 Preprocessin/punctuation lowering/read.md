Apart from all the text representation discussed, it is very important that we don't miss out on the basic pre processing ie., _removing punctuations, removing stopwords and convertint text to lowercase_. In the next module we would be including more advanced _POS tagging, parsing and coreference resolution_.

# 1. Removing Punctuations:
Punctuations are symbols like periods, commas, and exclamation marks that appear in text but often do not carry significant meaning for many NLP tasks. Removing punctuations helps simplify the text data and reduces noise.

# 2. Removing Stopwords:
Stopwords are common words in a language (e.g., "the," "is," "and") that occur frequently but typically do not contribute much to the overall meaning of a text. Removing stopwords can help reduce the dimensionality of the data and improve the performance of NLP models.

# 3. Converting Text to Lowercase:
Converting text to lowercase ensures that words with the same meaning but different cases (e.g., "Apple" vs. "apple") are treated as the same word. This normalization step helps improve the consistency of the text data and prevents duplication of features in NLP models.

Example:
"Hi, This is Oliver here and we are planning to cook some LLMs. I also like to play valo"

After preprocessing it would be like : hi this is oliver here and we are planning to cook some llms i also like to play valo

go through the punlow.ipynb file for the code
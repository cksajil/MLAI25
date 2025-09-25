- Introduction to Natural Language Processing (NLP)

	- Sentiment Analysis
	- Text Translation
	- Speech to Text (S2T)
	- Text to Speech (T2S)
	- Text Summarization
	- Named Entity Recognition (NER)
	- Chatboats
	- Large Language Models

- NLP Data Preprocessing/Text Cleaning Steps
	- Lowercase conversion
		- Tool/Technique: Regular expression
	- Tokenization
	- Stopwords removal
		- Remove Punctuations
	- Stemming
	- Lemmatization
	- Embedding
		- Corpus
		- Document/review
		- Corpus vocabulary
		- Bag of Words (BoW)
			- Binary Bag of Words
			- Count Vectorirzation
			- Term Frequency-Inverse Document Frequency (TF-IDF)
			- Ngrams
			- Word2Vec (W2V)
			- Average Word2Vec (AvgW2V)
			- TF-IDF weighted Word2Vec

- NLP Libraries
	- Natural Language Tool Kit (NLTK)
	- Spacy

- Activity: Apply a classical machine learning model and deep learning model to NLP Spam/non-spam example. Train and evaluate the models. Select the model with best accuracy. Convert all preprocessing steps to a single function. Demonstrate the model output for a sample test input.

TF-IDF (wj, ri) = TF*IDF

TF = # of times wj occurs in rj/Total #of words in rj
IDF (wj, C) = log(N/# of documents which contain wj)

More rare word -> N/#wj will be high -> IDF high
frequent word  -> N/#wj will be low  -> IDF low

r1 = This is the first document
r2 = This document is the second document
r3 = And this is the third one

	and, the, document, is, this, first, one, second, third
r1                              1/5*log(1/3)

Pros: Compensates for rarity of words
Cons: Dimension grows as corpus grows, doesn't captures sematic meaning

- Bigram

r1 = This, is, the, first, document, This is, is the, the first, first document

Pros: Considers context information
Cons: High dimension

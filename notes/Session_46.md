## Word2Vec, Glove, FastText Embedding Methods

- Pros: Considers Semantic Meaning, fixed dimension
Available as Pretrained Embeddings, vector representations are dense and not sparse like BoW or TFIDF
- Higher dimensions>more info rich

- Cons:
	- Doesn't work well with morphologically rich languages (solved by fasttext)
	-Lacks broad context awareness (solved by BERT)

- Word2Vec
	- Idea is if neighborhood of two words are similar then the words must be also similar in meaning
	- using Singular Value Decomposition (SVD). also called LSA (latent semantic analysis)

	- Continuous Bag-of-Words Model (CBOW)
	- Skip-gram

	- Tutorial: https://jaketae.github.io/study/word2vec/
	- https://www.geeksforgeeks.org/python/python-word-embedding-using-word2vec/
	- Captures semantic similarity but struggles with OOV words.


- Glove (Global Vectors for Word Representation)
	- Its primary objective is to capture semantic relationships between words by analyzing their co-occurrence patterns in a large text corpus.

	- Trained on global co-occurrence stats, good for large-scale corpora.

	- Tutorial: https://www.geeksforgeeks.org/nlp/Glove-Word-Embedding-in-NLP/

- FastText
	- https://www.geeksforgeeks.org/machine-learning/fasttext-working-and-implementation/
	- Uses subword information, handles OOV words better.


- Activity: 
    - (a) use w2v, Glove, Fasttext to compare consine similarity of known words (e.g. joy-sad-happy).
    - (b) find words similary to a given word
    - (c) Check parallel semantic relationships (e.g husband-wife, King-Queen), compute angle between the difference vectors a.b = |a||b|cos(theta)
    - (d) Perform sentiment analysis classifier using Tf-IDF weighted word2vec
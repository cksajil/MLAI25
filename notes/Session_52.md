- Recommendation Systems
    - Introduction
        - What is a Recommendation System?
        - Examples: Netflix, Amazon, Spotify
        - Business impact of recommendations

- Types of Recommendation Systems
	- Content-Based Filtering/Cosine Similarity | requires item details
	- Collaborative Filtering | requires user ratings of items
	- Matrix Factorization | requires user ratings of items

- Content-based filtering
	👉 “You like this item, so you’ll probably like something with similar features.”
	So content-based filtering looks at item features and recommends similar items.Every user gets personalized recommendations based on what they liked in the past.

- Collaborative Filtering
	👉 “People like you also liked these items.”
	- Uses user-item interactions (ratings, clicks)
	- Types:
		- User-User CF: given user find similar user:suggest the similar user's favorites
		- Item-Item CF: given a movie, find the most similar movie

	- Cold start problem
	- Code Demo: User-User Collaborative Filtering
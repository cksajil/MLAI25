- Application of Gen AI
	- LLM for Summarization, Q&A, Co-pilot Scenarios

- LLM usecases
	- Text Summarization
	- Headline Generator
	- Question Answering
	- Build a Simple FAQ Bot
	- Q&A on Uploaded Document (PDF)
	- Text Summarization: Comparing Different Model Outputs
	- Topic-Based Summaries
	- Multi-Document Q&A
	- True/False Questioning
	- Conversational Q&A

- Audio I/O
	- Text to Speech
	- Speech to Text

- Copilot Scenarios
	- Analyze and Describe CSV Data
	- Copilot Combo (Code + Writing + Data)
	- Python Helper
	- Email Assistant

- Activity: Create a conversational (audio) Q&A App that helps students know more about ICT academy of kerala. Information includes the types of courses offered, fees, duration. etc. Use the data available in ICTAK website for building the Q&A Model. Use proper prompt engineering to develop the app and code required. Push your app code as a GitHub project. Screenrecord the working of your app and share the same via discord.

Seq2Seq Training Data Samples

🔹 1. Machine Translation (English → Malayalam)

	Input (source language): "I love machine learning"

	Output (target language): "എനിക്ക് മെഷീൻ ലേണിംഗ് ഇഷ്ടമാണ്"

	Looks like paired bilingual sentences.
	📂 Dataset example: WMT, OPUS

🔹 2. Text Summarization

	Input: "Article: The Transformer architecture was introduced in 2017 by Vaswani et al. It replaced recurrence with attention and became the foundation of BERT, GPT, T5, etc."

	Output: "Transformers revolutionized NLP by replacing recurrence with attention."

	Paired (document, summary).
	📂 Dataset example: CNN/DailyMail

🔹 3. Sentiment Classification

	Input: "Review: The movie was boring and too long."

	Output: "Negative"

	Here, instead of generating long text, the model outputs a label token.
	📂 Dataset example: IMDB, SST-2

🔹 4. Question Answering

	Two common types:

	(a) Extractive QA (like BERT on SQuAD)

	Input:

	Question: "Who founded Microsoft?"

	Context: "Microsoft was founded by Bill Gates and Paul Allen in 1975."

	Output: Start=5, End=8 → "Bill Gates and Paul Allen"

	Here training labels are positions in the context.

	(b) Generative QA (like T5)

	Input: "question: Who founded Microsoft? context: Microsoft was founded by Bill Gates and Paul Allen in 1975."

	Output: "Bill Gates and Paul Allen"

	Here training labels are tokens of the answer text.

	📂 Dataset example: SQuAD, Natural Questions

🔹 5. Text Generation (Language Modeling, GPT)

	Input: "Once upon a time"

	Output: "there was a king who lived in a castle..."

	Training is self-supervised:

	Take a long text: "Once upon a time there was a king"

	Input = "Once upon a time there was a"

	Output = "king"
	and repeat for each position.

	📂 Dataset example: BooksCorpus, WebText

🔹 6. T5’s Unified “Text-to-Text” Format

	T5 makes all tasks look like input text → output text:

	Translation:
	Input: "translate English to German: That is good."
	Output: "Das ist gut."

	Summarization:
	Input: "summarize: The transformer was introduced in 2017 and changed NLP..."
	Output: "Transformers changed NLP."

	QA:
	Input: "question: Who founded Microsoft? context: Microsoft was founded by Bill Gates and Paul Allen."
	Output: "Bill Gates and Paul Allen"

Notebooks
	https://huggingface.co/datasets/bird-of-paradise/transformer-from-scratch-tutorial/blob/main/Transformer_Implementation_Tutorial.ipynb
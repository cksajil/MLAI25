- Common Generative AI Tools
	- Chatgpt-5 (https://chatgpt.com/)
	- Gemini (https://gemini.google.com/)
	- Grok (https://grok.com/)
	- DeepSeek (https://chat.deepseek.com/)
	- Claude (https://claude.ai/)
	- Perplexity (https://www.perplexity.ai/)
	- Copilot (https://copilot.microsoft.com/chats)

- Generative AI
	- For Learning/Upskilling
	- For Developing/Building

- Fundamental rules
	- You should have a clear understanding of what you want and be able instruct to judge the clarity & quality of prompt engineered output

	- Learn to ask right questions

- Tutorials
	- https://www.promptingguide.ai/
	-https://learnprompting.org/docs/basics/prompt_engineering

- Simple Prompt format
	- Question and Answer

- Elements of a prompt
	Instruction - a specific task or instruction you want the model to perform

	Persona - Adopt a Persona

	Context - external information or additional context that can steer the model to better responses

	Input Data - the input or question that we are interested to find a response for

	Specify the format - the type or format of the output.

- Prompting Techniques

	Zero-shot prompting: Ask the model to perform a task without giving any examples. Example: “Translate this sentence into French: ‘I love learning.’”

	Few-shot prompting: Provide a few examples to guide the model’s behavior. Example: “Translate the following sentences into French:

	‘Hello’ → ‘Bonjour’

	‘Good night’ → ‘Bonne nuit’ Now translate: ‘I love learning.’”

	Chain-of-thought prompting: Encourage the model to reason step-by-step before answering. Example: “If a train travels 60 km in 1 hour, how far will it go in 3 hours? Let’s think step by step.”

	Instruction based prompting: Clearly stating what the model should do. Example: Summarize the following article in two sentences. Focus on the main argument and conclusion.

	Contextual Anchoring: Embedding relevant background information in the prompt. Example: You are a financial advisor. Based on current market trends, explain whether investing in tech stocks is a good idea.

	Role-based Prompting: Assigning a role to the model to guide tone and style. Example: Explain the concept of mathematical function in laymans terms

- Activity: Try out various types of prompt engineering techniques.

	Zero shot
		- write function to convert mm/dd/yyyy to dd/mm/yyyy
	One shot
		- write a Python function to convert mm/dd/yyyy to dd/mm/yyyy

	Few shot
		- write a Python function to convert mm/dd/yyyy to dd/mm/yyyy so that it will work for multiple separators like (\,-,/)
		- Add persona: write a Python function to convert mm/dd/yyyy to dd/mm/yyyy so that it will work for multiple separators like (\,-,/) explain the logic for a python beginner

- Activity: Use prompt engineering to learn any concept from MLAI course. Report your prompts, its features and self rated clarity in a table form

	- What is tsne in machine learning? (zero shot)
	- Explain tsne in laymans terms (Persona added)
	- What is the applications of tsne (important prompt)
	- What are the limitations of tsne (important prompt)
	- What does the terms t-distributed, stochastic, neighborhood and embedding in tnse means, explain in laymans terms (Few shot)
	- Why tsne is good for dimentionality reduction but not feature reduction does it have any connection to stochasticity in tsne (chain of thought & follow up prompt)
	- Will the results of tsne consistent across differnt runs, if not why, explain with reasoning (chain of thought)
	- Explain with a minimal Python code for tsne implementation. The code should be at the level of a beginner python programmer


- Activity: Use prompt engineering to create a Python web app. Screen record of your app's working and share the same via discord.

Sample requirement: Create a Python based online quizz app. Each user can login using the local host url provided. Only one question is shown to the user at a time.  The answer options should be shown a lage tiles on to which the user can click. Add CSS to look the appearence like a professional website. The questions are populated from a CSV file. Provide the complete code.



# Evolution of Deep Learning Models (till ChatGPT-5)
1. Early Neural Networks (1950s–1990s)
- Perceptron (1958) – Rosenblatt’s single-layer neural net. Couldn’t model XOR.
- Backpropagation (1986, Rumelhart et al.) – Enabled training of multi-layer neural networks.
- Limitations: compute power + lack of data.

2. Rise of Deep Learning (2006–2012)
- Deep Belief Networks (2006) – Hinton revived neural networks.
- AlexNet (2012, Krizhevsky et al.) – Deep CNN that crushed ImageNet.
- GPU training, ReLU activations, dropout.
- Impact: Sparked the “deep learning revolution.”

3. Specialized Architectures (2013–2017)
- CNNs for vision: VGG, ResNet, Inception.
- RNNs for sequences: LSTM, GRU.
- Seq2Seq (2014, Sutskever) – Encoder–decoder for machine translation.
- Attention (2015, Bahdanau et al.) – Allowed models to focus on important parts of a sequence.

4. Transformers (2017–2018)
- “Attention is All You Need” (Vaswani et al., 2017)
- No recurrence, no convolutions → just attention.
- Scales better, parallelizable.
- Hugely influential → basis of modern NLP.

5. Pretrained Language Models (2018–2020)
- BERT (2018, Google) – Bidirectional transformer pretraining on masked language modeling.
- GPT (2018, OpenAI) – Autoregressive transformer.
- T5 (2019, Google) – Unified text-to-text framework.

6. Scaling Up (2020–2022)
- GPT-2 (2019) – Showed emergent abilities at scale.
- GPT-3 (2020) – 175B parameters, few-shot learning.
- Diffusion models (2021) – For images (DALL·E, Stable Diffusion).

7. Instruction Tuning & Alignment (2022–2023)
- InstructGPT (2022) – Fine-tuning GPT-3 with human feedback (RLHF).
- ChatGPT (2022) – Conversational AI for mass users.
- LLaMA, Falcon, MPT – Open-source alternatives.
- Emergent abilities – reasoning, coding, multilingual chat.

8. Multimodal & Tool-Using Models (2023–2024)
- GPT-4 (2023) – Better reasoning, vision (GPT-4V), improved alignment.
- Gemini, Claude, Mistral – Competing LLMs with different trade-offs.
- Function calling, tool use, retrieval augmentation → models became agents.

9. ChatGPT-5 (2025)
- Successor to GPT-4, with:
- More efficient training (smarter, not just bigger).
- Better reasoning across long contexts.
- Improved alignment with human values.
- Likely more multimodal (text, vision, audio).
- Represents the current state of the art in general-purpose AI assistants.

# LLMs and Transformers
- Transformers
- BERT
- T5
- GPT Fundamentals

## Why Transformers
### Why Transformers?
Before 2017, NLP models were dominated by:
- Recurrent Neural Network (RNN)
- Long Short-Term Memory (LSTM)
- Gated Recurrent Unit (GRU)

❌ Core Problems of RNNs
- Sequential processing → slow
- Vanishing gradients
- Poor long-range dependency capture
- Not parallelizable

### The Breakthrough: Attention Is All You Need (2017)
Everything changed with:
- Attention Is All You Need
- Authors from Google Brain
- Introduced the Transformer architecture

### Transformer Architecture
- Encoder Block
    - Multi-head attention
    - Add & LayerNorm
    - Feedforward network
    - Add & LayerNorm

- Decoder Block
    - Masked self-attention
    - Encoder-decoder attention
    - Feedforward

### BERT
- Introduced by Google in 2018
- Key Idea: Bidirectional Encoding
- Unlike GPT: BERT reads both left and right context.
- Applications
    - Pretraining Tasks: Masked Language Modeling (MLM)
    - Next Sentence Prediction (NSP)

- Architecture
    - Encoder-only Transformer
    - No decoder
    - Deep bidirectional self-attention

- BERT Works Well For:
    - Classification
    - NER
    - Question answering
    - Sentiment analysis

### GPT (Generative Pretrained Transformer)
- Created by OpenAI
- Decoder-only Transformer
- Masked self-attention
- Causal mask
- Left-to-right generation
- Performance improves with:
    - Model size
    - Data size
    - Compute
- GPT Strengths
    - Text generation
    - Few-shot learning
    - Instruction following
    - Creative writing
    
## Architectural Comparison
| Model | Architecture    | Direction     | Good For      |
| ----- | --------------- | ------------- | ------------- |
| BERT  | Encoder-only    | Bidirectional | Understanding |
| GPT   | Decoder-only    | Left-to-right | Generation    |
| T5    | Encoder-Decoder | Seq2Seq       | Both          |

## Tutorials
1. https://www.datacamp.com/tutorial/building-a-transformer-with-py-torch
2. https://jalammar.github.io/illustrated-transformer/
3. https://jalammar.github.io/illustrated-bert/



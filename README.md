# FinanceBot

<div align="justify">

## Context

The application of Artificial Intelligence in finance has been highly effective. If, in the past, this use was focused on predicting new investment trends and detecting fraudulent activities, with the advancement
of Generative Artificial Intelligence, chatbots (Mohamad Suhaili et al., 2021), systems that communicate with the user upon receiving requests in natural language, have been intensively developed to reduce the heavy workload of employees and improve the operational efficiency of organizations (Balaji et al.,2024). Banks, hedge funds, and private equity firms have been eager to use generative AI moving from pockets of experimentation to scaling companywide.

The Current literature for conversational generation focuses largely on improving generation capabilities in specific systems with much of the literature elucidating on pre-trained LLMs, expecially in health
care fields (Yu and McGuinness, 2024). The intent of this project is to develop a chatbot focused on finance as a specific domain , priotizing efficiency and accuracy for financial subjects.By incorporating
a domain-specific knowledge, its possible to enhance the accuracy and relevance of responses.Sequence to Sequence Learning(Seq2Seq) presented an end-to-end approach to sequence learning, making minimal assumptions on the sequence structure. Using a multilayered Long Short-Term Memory(LSTM) mapping the input to a vector of a fixed dimensionality sebsequenced by another deep LSTM to decode the target sequence from the vector. Showing that could learn sensible phases and setences representations.(Sutskever et al., 2014) Luong Attention (Luong et al., 2015) simplifies the computation of alignment scores by using matrix multiplication. Providing a computationally efficient way of dynamically attending to input sequence elements during decoding,faster for short sequences.The baseline Transformers Vaswani et al. (2017) following attention mechanisms, demonstrates a
good generalization when applied to the English constituency parsing observing with large and limited training data. Inside this approach Multi-head Attention is presented as a module for attention mechan-isms extending self-attention by splitting the input into multiple heads, allowing for attending different sequences including longer-term dependencies and shorter-term dependencies.

MHA Talking heads attention(Shazeer et al., 2020) aims to include linear projections across the attention-heads, before and after softmax, generating better quality when transfer-learning to language comprehension and question answering tasks. The variation of MHA named MQA(Multy Query Attention)Shazeer (2019) introduces the key and values shared across all the different attention heads, with a proeminent resulting in a faster process training and with minor quality degradation.


The focus of this project is to investigate effective model implementations that can be case studied by companies when it comes to conversational systems. Using the finance alpaca datadrame, we propose
a benchmark study of various models architcures with emphasis on the baseline generative models such as SeqSeq2 and Transformers, as well as their subsequent evolutions, following the stipulations of the original articles.

## Dataset
The dataset used in this work is the Finance Alpaca dataset (Bharti, 2024). In a JSON format, is a specialized instruction-tuning dataset for large language models (LLMs) in the financial domain.It contains 68,912 examples formatted as instruction-input-output triples, combining Stanford’s Alpaca, FiQA, and around 1,300 GPT-3.5-generated examples.The dataset is in English and commonly used forfine-tuning models such as Llama 3.1 8B.

## Architectures

### Sequence to Sequence
Sequence to Sequence models are built using two main components Encoder and Decoder. The encoder processes the input text and converts it into a fixed size context vector, which captures important information from the input sequence Sutskever et al. (2014)

### Attention Mechanism
Seq2Seq models use the attention mechanism to focus on the most important parts of the input while minimizing the impact of irrelevant information during training. Attention helps the model handle long input sentences by focusing on the certain words that are crucial for predicting the correct output.

### Bahdanau Attention

Bahdanau attention mechanism, also known as additive attention, is the architecture of the encoder block that stays the same. However, in the decoder, a small feedforward neural network called the alignment model is added. The process starts by feeding the input sentence into the encoder, to get hidden states like hi e.g h1, h2, h3, h4 and so on.

### Luong Attention

In contrast, Luong attention, also known as dot product or multiplicative attention, introduces a few improvements over Bahdanau attention. In Luong attention, the attention weights are calculated using the current hidden states of both the encoder and the decoder, unlike Bahdanau attention, which uses the previous hidden state of the decoder. This approach makes Luong attention slightly simpler and more efficient.

### Transformers

With the introduction of attention mechanisms, a technique used to provide weights to different parts of an input sequence so that a better understanding of its underlying context is achieved. The Transformers
model architecture can be defined by a combination of encoder, decoder, attention, feed-forward networks (FFN), normalization layers, and positional coding.


</div>

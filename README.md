# Summarization_dialogue
 The goal of this project is to build a model that will be capable to summarize dialogue.

## Description of the dataset
 The dataset used to train the models was the SAMSum dataset.
 The SAMSum dataset consists of over 16,000 dialogue examples designed for the task of summarizing informal conversations, such as chat messages. 
 This corpus allows models to generate concise, coherent summaries of multi-turn dialogues, helping refine AI’s ability to process and summarize human-like interactions.

## Finetuned models
### 1. BART (Bidirectional and Auto-Regressive Transformers)
- **Architecture**: BART is a transformer-based sequence-to-sequence model that combines a bidirectional encoder (similar to BERT) with an autoregressive decoder (similar to GPT). This design allows BART to capture context in both directions (left-to-right and right-to-left) during encoding, while generating text sequentially during decoding.
### 2. T5 (Text-to-Text Transfer Transformer)
- **Architecture**: T5 is a unified text-to-text framework that treats every NLP task as a text generation task. It is a transformer-based model with both encoder and decoder components. Unlike many models that specialize in specific tasks, T5 uses the same format (text-to-text) across all NLP tasks, allowing for straightforward task adaptation.

## Metrics
### 1. Training Loss
- **Description**: The average loss during model training. Lower values indicate that the model is learning well, minimizing the difference between predicted and actual values. Typically, this is computed over each batch during training and helps measure model convergence.

### 2. Validation Loss
- **Description**: The average loss during validation. This is a key metric to monitor overfitting. If validation loss diverges significantly from training loss, the model may not generalize well to unseen data. Lower values generally indicate better generalization.

### 3. ROUGE-1
- **Description**: Measures the overlap of unigrams (single words) between the generated summary and the reference summary. Useful for evaluating recall of individual words and content selection quality in summarization.

### 4. ROUGE-2
- **Description**: Measures the overlap of bigrams (two consecutive words) between the generated summary and the reference summary. Provides a more stringent measure of similarity and coherence, capturing phrase-level overlap.

### 5. ROUGE-L
- **Description**: Measures the longest common subsequence (LCS) between the generated and reference summaries. This metric captures the longest sequence of matching words while preserving order, making it useful for assessing fluency and coherence in the generated summary.

### 6. ROUGE-LSum
- **Description**: A variation of ROUGE-L tailored specifically for summarization tasks. It considers sentence-level longest common subsequence, measuring similarity between sentences in the generated and reference summaries. Useful for evaluating complex summarization structures.

### 7. Gen Len (Generation Length)
- **Description**: Captures the average length of the generated summaries. This metric helps understand whether the model is generating summaries that are appropriately concise or verbose relative to the desired output length.
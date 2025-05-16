# Transformer-English-to-Hindi (WIP)
In this repo I have tried to implement a transformer-based sequence-to-sequence model from scratch in order to perform translation of an input sentence from English (Latin script) to Hindi (Devanagari script), inspired by the original ["Attention is All You Need"](https://arxiv.org/abs/1706.03762) paper, and ["Umar Jamil"](https://youtu.be/ISNdQcPhsts?feature=shared)

I have trained the model on ["atrisaxena/mini-iitb-english-hindi"](https://huggingface.co/datasets/atrisaxena/mini-iitb-english-hindi) (which is a mini version of the official ["cfilt/iitb-english-hindi"](https://huggingface.co/datasets/cfilt/iitb-english-hindi)), which contains 20000 samples for training out of which I used 19000 samples for training and the rest for validation. The official dataset by IIT Bombay consisted of 1.66 mil samples to train on, which could not be processed by my current memory and compute (Google Colab).

These were some of the hyperparameters I set:
* batch_size - 16,
* num_epochs - 45,
* lr - 5e-4,
* seq_len - 256,
* d_model - 512,

For tokenization I used "Tokenizers" by HuggingFace, in which I currently implemented the "Word-level tokenization". I am also trying to implement tokenization using Byte-Pair Encoding (BPE) and Unigram (This is currently a work in progress). And I used whitespace as a pre-tokenizer.

I will also try to visualize the attention mechanism in future work.

# English–Urdu Neural Machine Translation (LSTM vs Transformer)

This repository implements and compares two Neural Machine Translation (NMT) architectures for English-to-Urdu translation:
- Seq2Seq LSTM with Bahdanau Attention
- Transformer Encoder–Decoder

The project focuses on low-resource machine translation using the UMC005 parallel corpus and is implemented entirely in PyTorch.

---

## 📌 Project Overview

English–Urdu translation is a challenging task due to script differences, word order variation, and limited availability of high-quality parallel data. This project explores how traditional recurrent models and modern attention-based architectures perform under such constraints.

Both models are trained from scratch and evaluated using standard MT metrics. An interactive Gradio interface is also provided for real-time translation and experimentation.

---

## 📂 Dataset

- **Corpus:** UMC005 (Quran subset)
- **Language Pair:** English → Urdu
- **Total Sentence Pairs:** 4,793 (after filtering)
- **Split:**
  - Train: 80%
  - Validation: 10%
  - Test: 10%

---

## 🧠 Models Implemented

### 1. Seq2Seq LSTM with Attention
- Bidirectional LSTM encoder
- Unidirectional LSTM decoder
- Bahdanau attention mechanism
- Teacher forcing during training

### 2. Transformer Model
- Multi-head self-attention
- Encoder–decoder architecture
- Sinusoidal positional encoding
- Causal and padding masks

---

## ⚙️ Training Configuration

- Framework: PyTorch
- Batch Size: 64
- Epochs: 5
- Optimizer: Adam
- Loss Function: Cross-Entropy (ignoring padding tokens)
- Hardware: Google Colab (GPU)

---

## 📊 Evaluation Metrics

- BLEU
- ROUGE-L
- Perplexity

| Model        | BLEU | ROUGE-L | Perplexity |
|-------------|------|----------|------------|
| LSTM        | 0.42 | 4.29     | 99.78      |
| Transformer | 2.16 | 6.76     | 110.80     |

---

## 🌐 Interactive Translation

A **Gradio-based web interface** is included to perform real-time English–Urdu translation using the trained Transformer model. This allows easy testing and qualitative evaluation of translations.

---

## ⚠️ Limitations

- Small dataset and domain-specific text
- Word-level tokenization
- Limited training epochs
- Greedy decoding
- Small model sizes

---

## 🚀 Future Work

- Subword tokenization (BPE / SentencePiece)
- Larger model architectures
- Beam search decoding
- Pretrained multilingual transformers
- Domain adaptation with diverse corpora

---

## 🧑‍💻 Author

**Moiz Sajjad**  
Department of Data Science  
FAST NUCES, Islamabad

---

## 📄 License

This project is intended for academic and research purposes.

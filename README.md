# 🧠 Seq2Seq Model for Machine Translation

This project implements a **Sequence-to-Sequence (Seq2Seq)** model for **neural machine translation (NMT)**, converting sentences from **English to French** using **TensorFlow/Keras**. The architecture leverages **LSTM-based encoder-decoder networks**, a popular deep learning approach for translating variable-length input and output sequences.

---

## 🚀 Demo

- Input (English): `Where are you going?`
- Output (French): `Où allez-vous ?`

> Run `model.ipynb` to see end-to-end training and prediction.


---

## 📊 Dataset

- 📚 **Source**: [ManyThings.org (fra-eng)](http://www.manythings.org/anki/)
- 👥 Contains ~150,000 English ↔ French sentence pairs.
- ✂️ The dataset is trimmed to 10,000–20,000 sentence pairs for faster training.

---

## 🧠 Model Architecture

- **Encoder**:
  - Embedding Layer
  - LSTM Layer → returns hidden & cell state
- **Decoder**:
  - Embedding Layer
  - LSTM Layer → uses encoder states as initial state
  - Dense (Softmax) → Predicts translated word at each timestep
- **Teacher Forcing**: Helps speed up training and improve convergence.

---

## 🛠️ How to Run

1. **Clone the repo**:
   ```bash
   git clone https://github.com/srilasya-s/Seq2Seq-Model-for-Machine-Translation.git
   cd Seq2Seq-Model-for-Machine-Translation
Install dependencies:


pip install -r requirements.txt
Run the notebook:


jupyter notebook model.ipynb
📦 Dependencies
txt

tensorflow
numpy
pandas
matplotlib
re
You can install all dependencies via:


pip install -r requirements.txt
📈 Results
Metric	Value
Training Loss	~0.92
Validation Loss	~1.10
BLEU Score	(Optional) You can compute using nltk.translate.bleu_score

💡 Future Improvements
 Add attention mechanism (Bahdanau or Luong)

 Replace LSTM with GRU or Transformer-based encoder

 BLEU score evaluation

 Create REST API for translation

🙋‍♀️ Author
Sri Lasya

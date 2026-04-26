# 🔍 TrueSight AI — Fair Pricing Guard

> *"AI doesn't just make decisions — it sets prices. And if those prices are biased, millions are affected silently."*

**TrueSight AI** is an open-source bias detection and mitigation pipeline that identifies and fixes algorithmic price discrimination based on demographic attributes like gender, age, and zip code.

Built for the **Google Solution Challenge 2026** under the **Unbiased AI Decision** problem statement.

---

## 🚀 Live Demo

| Resource | Link |
|---|---|
| 🧪 Google Colab Notebook | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jqcdpKdbNIxKpJimjgOcFjqXwFWMTwOT) |
| 🤗 Hugging Face Space |https://huggingface.co/spaces/siddu413/truesight-ai |

---

## 📌 Problem Statement

AI and ML systems are increasingly used to set prices, approve loans, and screen applications. When trained on historically biased data, they silently perpetuate discrimination against protected groups. Existing solutions fail because:

- Manual audits are expensive and infrequent
- Regulatory checks lag behind deployment
- Black-box models provide no explanation
- Users have no way to detect or challenge biased outcomes

---

## ✅ What TrueSight AI Does

1. **Upload** a CSV dataset with demographic + pricing/decision columns
2. **Detect** bias using 5 industry-standard fairness metrics
3. **Explain** the findings in plain English via a Hugging Face LLM (no API key needed)
4. **Mitigate** bias with one-click AIF360 reweighing or Fairlearn threshold optimization
5. **Export** a before/after fairness report and cleaned dataset

---

## 📊 Fairness Metrics Used

| Metric | Threshold | Library |
|---|---|---|
| Demographic Parity Difference | < 0.1 (ideal: 0) | Fairlearn |
| Equalized Odds Difference | < 0.1 (ideal: 0) | Fairlearn |
| Disparate Impact Ratio | > 0.8 (legal standard) | AIF360 |
| Statistical Parity Difference | < 0.05 (ideal: 0) | AIF360 |
| Average Odds Difference | < 0.1 (ideal: 0) | AIF360 |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Platform | Google Colab (free tier) |
| Language | Python 3.10+ |
| Bias Detection | Fairlearn 0.10, AIF360 0.6 |
| AI Explanation | Hugging Face Transformers — FLAN-T5 (no API key) |
| ML Framework | scikit-learn, PyTorch |
| Visualization | matplotlib, seaborn, plotly |
| Data Handling | pandas, numpy |
| UI | Gradio |

> ⚠️ **No Gemini API. No OpenAI API. No proprietary dependencies.** Fully open-source and free.

---

## 📁 Repository Structure

```
truesight-ai/
│
├── notebook/
│   └── truesight_ai.ipynb          # Main Colab notebook (all 9 cells)
│
├── src/
│   ├── data_generator.py           # Synthetic biased dataset generator
│   ├── bias_detector.py            # Fairlearn + AIF360 metrics
│   ├── explainer.py                # Hugging Face FLAN-T5 explanation
│   ├── mitigator.py                # Reweighing + ThresholdOptimizer
│   ├── visualizer.py               # Before/after charts
│   └── app.py                      # Gradio UI
│
├── data/
│   └── sample_pricing_dataset.csv  # Sample dataset with injected bias
│
├── requirements.txt
└── README.md
```

---

## ⚡ Quick Start

### Option 1: Google Colab (Recommended — Zero Setup)
Click the **Open in Colab** badge above and run all cells top to bottom.

### Option 2: Local Setup
```bash
git clone https://github.com/YOUR_USERNAME/truesight-ai.git
cd truesight-ai
pip install -r requirements.txt
python src/app.py
```

---

## 📈 Expected Results

| Metric | Before Mitigation | After Mitigation |
|---|---|---|
| Demographic Parity Difference | 0.18 – 0.25 | < 0.05 |
| Disparate Impact Ratio | 0.60 – 0.75 | > 0.85 |

---

## 🔮 Future Work

- Intersectional fairness analysis (gender + age simultaneously)
- Causal fairness methods
- Real-time API on Google Cloud Run
- NLP bias detection in job descriptions

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🏆 Google Solution Challenge 2026

This project addresses the **Unbiased AI Decision** problem statement.  
Built with ❤️ using Google Colab + Hugging Face.

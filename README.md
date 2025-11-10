# ClarifAI 💡 — Ambiguity Detection and Rectification in Software Requirements

## Overview
ClarifAI is a Python-based tool for detecting **ambiguous terms** in software requirement glossaries and suggesting clear, measurable clarifications.  
The project consists of **two main scripts**:

1. **Rectification Script** – generates a dataset of ambiguous terms with dynamic suggestions.  
2. **Main Model + GUI** – fine-tunes DistilBERT for ambiguity detection and provides an interactive Tkinter GUI.

---

## 1️⃣ Rectification Script
- **Input:** `glossary_full.csv` (124 terms with labels and optional clarifications)  
- **Output:** `ambiguous_rectified.csv` (only ambiguous terms with auto-generated clarifications)  
- **Function:** Automatically produces precise suggestions for ambiguous terms.  
- **Example Output:**

Term: user-friendly
Rectification: 'user-friendly' should be described explicitly. Clarify its meaning, scope, and measurable criteria.

---

## 2️⃣ Main Model + GUI
- **Model:** DistilBERT fine-tuned for **binary ambiguity classification** (Ambiguous/Clear)  
- **Dataset:** Uses both `glossary_full.csv` and `ambiguous_rectified.csv`  
- **Features:**
  - Detects if a term is ambiguous  
  - Shows **confidence**, **Precision**, **Recall**, **F1-Score**  
  - Provides **suggestions / rectifications** for ambiguous terms  
  - Dynamic **bar graph visualization** of probabilities  
- **GUI:** Users enter a term and optional clarification, then receive real-time analysis.

---

## Workflow
1. Run **rectification script** to generate `ambiguous_rectified.csv`.  
2. Run **ClarifAI GUI** to analyze terms using fine-tuned DistilBERT.  
3. View predictions, suggestions, and metrics interactively.

---

## Tools & Technologies
- Python, PyTorch, Hugging Face Transformers, Tkinter  
- pandas, numpy, scikit-learn, matplotlib, Pillow, scipy  

## Deliverables
- `pytorch_model.bin` (fine-tuned model)  
- Interactive GUI for term analysis  
- Ambiguity rectifications and evaluation metrics




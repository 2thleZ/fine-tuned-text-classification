# fine-tuned-text-classification
### SST-2 Fine-tuning (BERT / DistilBERT)

Fine-tuned pretrained transformers for **binary sentiment** (GLUE/SST-2) using a **custom training loop**
(AdamW, dynamic padding, gradient clipping, linear LR schedule). Includes learning curves and an error
analysis CSV of misclassified validation samples.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/2thleZ/<fine-tuned-text-classification>/blob/main/Finetuning.ipynb)

## Results
- **BERT-base-uncased:** val accuracy **0.919** (best epoch ~1)  
- **DistilBERT-base-uncased:** val accuracy **0.905** (best epoch ~3)  
- Mild overfitting after epochs 3–4; error modes: **negation/contrast, sarcasm, spurious lexical cues**.

## How to run (local)
```bash
python -m venv .venv && .\.venv\Scripts\activate    # Windows; or source .venv/bin/activate on macOS/Linux
pip install -r requirements.txt
# open Finetuning.ipynb and run all cells

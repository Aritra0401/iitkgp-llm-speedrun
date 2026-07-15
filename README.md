# IIT KGP LLM Speedrun 2026

## Overview

This repository contains my solution for the IIT Kharagpur LLM Speedrun assignment.

The objective was to improve the baseline GPT implementation while staying within the parameter budget and training constraints.

---

## Model

Architecture:
- Decoder-only GPT
- Byte-level tokenizer (256 vocabulary)
- 4 Transformer layers
- 4 Attention heads
- Embedding dimension: 192
- Context length: 128

---

## Training

Dataset:
- train_corpus.txt

Training command:

```bash
python train.py --data ../data/train_corpus.txt
```

Evaluation:

```bash
python evaluate.py --checkpoint ckpt_v4.pt --text_file ../data/dev_eval.txt
```

---

## Experiments

| Run | Change | BPB |
|-----|--------|------|
| Baseline | Starter model | 2.3718 |
| Run 2 | Weight tying + AdamW + Scheduler + Gradient Clipping | 2.6956 |
| Run 3 | Increased embedding dimension | **2.3472** |

Best checkpoint:
- ckpt_v4.pt

---

## Files

- model.py
- train.py
- evaluate.py
- tokenizer.py
- RUNLOG.md
- NOTES.md
- SUMMARY.html
- ckpt_v4.pt

---

## Final Result

Best BPB:

**2.3472**

This checkpoint is included in the repository.
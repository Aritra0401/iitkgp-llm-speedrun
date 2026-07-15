# RUNLOG

## Run 1 (Baseline)

Command:

python train.py --data ../data/train_corpus.txt

Changes:

- None (starter baseline)

Training:

- 2000 steps
- Default learning rate (3e-4)

Result:

- Training completed successfully.
- Checkpoint saved as ckpt.pt.

Notes:

- Baseline before optimization.

## Run 2

Changes:
- Enabled weight tying.
- Switched Adam → AdamW (weight_decay=0.01).
- Added gradient clipping (max_norm=1.0).
- Added cosine learning-rate schedule.

Reason:
Simple optimization improvements with minimal code changes.
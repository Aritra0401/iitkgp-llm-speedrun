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
- Enabled weight tying
- AdamW
- Cosine LR scheduler
- Gradient clipping

Result:
- BPB increased from 2.3718 to 2.6956.

Conclusion:
- Rejected these changes and reverted to the baseline training configuration.

## Run 3

Changes:
- Increased embedding dimension from 160 to 192.

Result:
- BPB: 2.3472

Conclusion:
- Best performing model.
- Final submission uses this checkpoint.
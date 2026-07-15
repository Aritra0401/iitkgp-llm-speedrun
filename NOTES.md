# NOTES

## Experiments

### Failed
- Weight tying
- AdamW
- Cosine scheduler
- Gradient clipping

These significantly worsened BPB.

### Successful

Increasing embedding dimension from 160 to 192 improved BPB.

## Final Model

- n_embd = 192
- Adam optimizer
- No scheduler
- No dropout
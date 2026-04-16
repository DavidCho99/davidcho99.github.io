# Plan (NN-Pytorch -> Math for ML + Project Page)

Goal: extract the core concepts from `NN-Pytorch.pdf`, rewrite them as a clean "Math for ML" reference page on the site, and create a related project writeup page.

## Deliverables

- A new site page: `math-for-ml.md` (`/math-for-ml/`)
- A new project post: `_posts/project/2026-04-16-nn-pytorch-study-project.md` (category: `Project`)
- Navigation links so the pages are easy to find

## Work Items

1. Extract book outline (Ch. 1-15) and decide what becomes "math" vs "tools".
2. Write `math-for-ml.md`:
   - Linear regression (normal equation, gradient descent, bias/variance intuition)
   - Neural nets (matrix notation, activations, backprop via chain rule)
   - Validation (train/val/test, leakage, metrics)
   - CNN math (convolution, padding/stride, pooling)
   - Classification + cross entropy (softmax, log-loss), info theory basics
   - Regularization (dropout, weight decay)
3. Write the project post:
   - Scope, milestones, datasets (MNIST, housing), and experiment checklist
   - Link to the Math-for-ML page
4. Wire navigation:
   - Add `/math-for-ml/` link to sidebar and home
5. Sanity check:
   - Ensure pages render (front matter, permalinks, internal links)


# Neural Superposition - Manim Explainer

Manim animation source code for the video [Superposition in neural networks](https://youtu.be/JHUymseNbUg).

This repo visualizes a central mechanistic-interpretability idea: neural networks can represent more features than they have obvious independent dimensions by packing features into shared directions. The scenes use vectors, projections, straw-packing metaphors, ReLU behavior, and small network diagrams to make that geometry easier to reason about.

## What This Teaches

- What a "feature" means in a neural network representation.
- Why orthogonal vectors are easy to separate but limited in number.
- How superposition lets features share representational dimensions.
- Why sparsity and nonlinear activations make feature packing more plausible.
- How projection, reconstruction, and compression create tradeoffs.

## Repo Map

- `code/what_is_a_feature.py` - feature-vector intuition.
- `code/vctr_ortho_3d.py`, `code/VectorOrthogonality.py` - orthogonal vector scenes.
- `code/three_vectors_120_degrees.py`, `code/pentagonal_angles.py` - packed vector-angle examples.
- `code/straw_box.py`, `code/big_straw_box.py`, `code/NeuralStrawPacking.py` - straw-packing metaphor scenes.
- `code/vector_reconstruction_2d_to_3d.py`, `code/projection3d2d.py`, `code/3dVctr.py` - projection and reconstruction scenes.
- `code/relu.py`, `code/after_relu.py` - ReLU and sparsity intuition.
- `code/mlp.py`, `code/mlp_zoom.py`, `code/hidden_layers.py`, `code/last_layer.py` - neural network structure scenes.
- `angles.py`, `straw_scatter.py` - additional vector and 3D scatter scenes.

## Setup

Install Manim in a Python environment:

```bash
python -m venv .venv
source .venv/bin/activate
pip install manim
```

## Running A Scene

Render a feature-intuition scene:

```bash
manim -pql code/what_is_a_feature.py WhatIsAFeature
```

Render a straw-packing scene:

```bash
manim -pql code/NeuralStrawPacking.py NeuralStrawPacking
```

Render a 3D scatter scene:

```bash
manim -pql straw_scatter.py StrawScatter
```

Use `-pqh` instead of `-pql` for a higher-quality render.

## Why This Exists

Superposition is easier to discuss abstractly than to picture. This repo makes the geometric argument visible: how features can be arranged, compressed, projected, activated, and recovered under representational pressure.

## Related Explainers

- [LLM Arithmetic](https://github.com/leannchen86/llm-arithmetic-manim)
- [Hybrid Search + BM25](https://github.com/leannchen86/hybrid-search-bm25-manim)
- [CLIP Encoding](https://github.com/leannchen86/clip-encoding-manim)

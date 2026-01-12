## SparseSearchEverything

This repository explores **Sparse Autoencoders (SAEs) applied to Large Language Models (LLMs)** with the goal of extracting **interpretable, sparse, and potentially monosemantic features** from model activations.

The project is inspired primarily by Anthropic’s work on mechanistic interpretability and sparse representations, including:
- *Scaling Monosemanticity*
- *Toy Models of Superposition*

(see references below)

---

### Goal

The original goal of this repository was to:
- Build sparse autoencoders on top of LLM internal activations
- Train and evaluate SAEs on intermediate representations (MLP and attention outputs)
- Run experiments to identify relationships between neurons and model behavior, and probe these representations to **mechanistically alter model behavior** by modifying activations

---

### Approach

The code focuses on:
- Extracting intermediate activations from a GPT-style transformer
- Running inference over large text datasets (e.g. Wikipedia-style corpora)
- Collecting and saving MLP hidden states and outputs for downstream SAE training
- Training SAEs on the collected activations
- Identifying neuron and feature contributions
- Altering model behavior through targeted, mechanistic intervention

---

### Status

⚠️ **This repository is incomplete / paused**

**Current state:**  
Development progressed up to **collecting and saving internal activations from the model** (e.g. MLP hidden states and outputs).  
Work on large-scale SAE training, feature analysis, and behavioral intervention was not completed in this codebase.

During development, I discovered **TransformerLens** and **SAELens**, two libraries created by Neel Nanda and maintained by a fantastic group of people.
Given their quality and maturity, further work in this repository was paused in favor of using these tools instead.

---

### References

- Anthropic — *Scaling Monosemanticity*  
  https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html

- Anthropic — *Toy Models of Superposition*  
  https://transformer-circuits.pub/2022/toy_model/index.html

- TransformerLens & SAELens
  https://github.com/TransformerLensOrg/TransformerLens
  https://github.com/decoderesearch/SAELens

## GitHub Repository Description

---

> **Learning a Similarity Metric Discriminatively — Chopra et al. (2005)**
>
> PyTorch implementation of the Siamese network and contrastive loss introduced in *"Learning a Similarity Metric Discriminatively, with Application to Face Verification"* (Chopra, Hadsell & LeCun, CVPR 2005) — one of the foundational papers in metric learning and representation learning.
>
> The model learns an embedding function $G_W$ that maps inputs into a feature space where semantically similar pairs are geometrically close and dissimilar pairs are pushed apart. Unlike standard classifiers that learn to assign labels, the model learns **relationships between examples** — a distinction that turns out to matter enormously for tasks like face verification, image retrieval, and one-shot recognition.
>
> Training uses the original contrastive objective:
>
> $$\mathcal{L}(W, Y, X_1, X_2) = (1-Y)\cdot\frac{1}{2Q}E_W^2 + Y\cdot\frac{1}{2}Q^2\exp\!\left(-\frac{2.77}{Q}E_W\right)$$
>
> where $Y=0$ denotes a genuine pair, $Y=1$ an impostor pair, $E_W = \|G_W(X_1) - G_W(X_2)\|$ is the energy, and $Q$ controls the dynamic range of the network output.
>
> **For a deeper discussion of the paper's ideas, its mathematical foundations, and its lasting influence on modern representation learning and contrastive self-supervised methods, read the accompanying article:**
> 📖 [Representation Learning Through the Lens of Similarity](https://medium.com/p/5e2e752748bc/edit)

---

### Features

- Siamese network architecture with shared weights
- Original exponential contrastive loss (Chopra 2005)
- Configurable embedding dimension and network backbone
- Training and evaluation on paired datasets
- Embedding visualization utilities

---

### References

- Chopra, S., Hadsell, R., & LeCun, Y. (2005). *Learning a Similarity Metric Discriminatively, with Application to Face Verification.* CVPR 2005.

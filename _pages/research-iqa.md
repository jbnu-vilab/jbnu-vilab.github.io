---
title: "Image Quality Assessment"
permalink: /research/iqa/
author_profile: false
---

<a href="/research/">&larr; Back to Research</a>

---

## Image Quality Assessment

<figure style="margin: 1.5em 0; text-align: center;">
  <img src="/files/figure4.png" alt="Dual-branch vision transformer for BIQA" style="width: 100%; max-width: 860px;">
  <figcaption style="margin-top: 0.5em; font-size: 0.9em; color: #555;">The proposed dual-branch vision transformer for blind image quality assessment (BIQA).</figcaption>
</figure>

Blind image quality assessment (BIQA) aims to predict the perceptual quality of an image without access to a reference. We propose a dual-branch vision transformer that simultaneously considers both local distortions and global semantic information. Dual-scale features are extracted from a backbone network and fed into separate transformer encoder branches — the S-Branch and L-Branch — each capturing scale-variant local distortions through local feature embeddings. Content-aware IQA (CA-IQA) embeddings enable each branch to also capture the global distortion context. The outputs of both branches are combined via feed-forward blocks to produce the final quality score.

**Publications**

- **Se-Ho Lee** and Seung-Wook Kim, "Dual-branch vision transformer for blind image quality assessment," *Journal of Visual Communication and Image Representation*, vol. 94, pp. 103850, Jun. 2023. \[[DOI](https://doi.org/10.1016/j.jvcir.2023.103850)\]

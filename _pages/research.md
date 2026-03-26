---
title: "Research"
permalink: /research/
author_profile: false
---

---

## 3D Gaussian Splatting

<video width="100%" controls style="margin: 1em 0;">
  <source src="/files/ECCV_video_supp.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

We present a novel geometry-aware style transfer framework for 3D Gaussian Splatting (3DGS) that simultaneously transfers both appearance attributes and geometric structures from a style image. Unlike previous works that focus solely on color-based stylization, our method explicitly incorporates geometry adaptation through a decoupled optimization scheme that alternately updates color and geometry parameters. The decoupled optimization is enabled by the proposed geometry-aware contrastive feature matching (GCFM), which integrates RGB, depth, and edge cues into a contrastive objective for effective and structurally consistent style transfer.

**Publications**
- Min Hyeok Bang\*, Jun Hyeong Kim\*, Seung-Wook Kim, and **Se-Ho Lee**, "Geometry-aware style transfer in 3D Gaussian splatting," *ECCV*, 2026 (Submitted).

---

## Image Enhancement

We develop deep learning-based image enhancement methods that adaptively improve visual quality across diverse conditions. Our approaches span global color transformation and local refinement, enabling high-quality photo retouching, tone mapping, and content-adaptive enhancement. We model complex color mappings through pigment-based representations and deformable control points that go beyond conventional pre-defined color spaces.

**Publications**
- **Se-Ho Lee**, Keunsoo Koh, and Seung-Wook Kim, "Image enhancement based on pigment representation," *IEEE Transactions on Multimedia*, 2026. [[DOI](https://doi.org/10.1109/TMM.2026.3654419)] [[Project](https://github.com/jbnu-vilab/pigment_enhancement)]
- **Se-Ho Lee** and Seung-Wook Kim, "DCPNet: Deformable control point network for image enhancement," *Journal of Visual Communication and Image Representation*, vol. 104, pp. 104308, Oct. 2024. [[DOI](https://doi.org/10.1016/j.jvcir.2024.104308)]

---

## Image Quality Assessment

Blind image quality assessment (BIQA) aims to predict perceptual image quality without a reference image. We propose a dual-branch vision transformer for BIQA that simultaneously considers both local distortions and global semantic information. Dual-scale features extracted from a backbone network are fed into separate transformer encoder branches, each capturing scale-variant local distortions alongside global distortion context through content-aware embeddings.

**Publications**
- **Se-Ho Lee** and Seung-Wook Kim, "Dual-branch vision transformer for blind image quality assessment," *Journal of Visual Communication and Image Representation*, vol. 94, pp. 103850, Jun. 2023. [[DOI](https://doi.org/10.1016/j.jvcir.2023.103850)]

---

## Demoiréing

Moiré artifacts arise from frequency interference between display grids and camera sensors, causing visually disturbing patterns in photos and videos. We address both image and video demoiréing by exploiting spectral and temporal characteristics of moiré patterns. Our video demoiréing network adaptively suppresses moiré in the frequency domain and uses inter-frame subtraction to guide alignment and prevent temporal propagation of artifacts.

**Publications**
- Seung-Hun Ok, Young-Min Choi, Seung-Wook Kim, and **Se-Ho Lee**, "Adaptive video demoiréing network with subtraction-guided alignment," *IEEE Signal Processing Letters*, vol. 32, Jul. 2025. [[DOI](https://doi.org/10.1109/LSP.2025.3585820)] [[Code](https://github.com/Oksta1002/AVDNet)]
- Duong Hai Nguyen, **Se-Ho Lee**, and Chul Lee, "Multiscale coarse-to-fine guided screenshot demoiréing," *IEEE Signal Processing Letters*, vol. 30, pp. 898–902, Jul. 2023. [[DOI](https://doi.org/10.1109/LSP.2023.3296039)]

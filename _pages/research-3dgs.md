---
title: "3D Gaussian Splatting"
permalink: /research/3dgs/
author_profile: false
---

<a href="/research/">&larr; Back to Research</a>

---

## Geometry-Aware Style Transfer in 3D Gaussian Splatting

<p style="margin: 0.5em 0 1.2em 0; font-size: 0.95em; color: #555;">
  <strong>ECCV 2026 (Accepted)</strong> &nbsp;|&nbsp;
  Min Hyeok Bang*, Jun Hyeong Kim*, Seung-Wook Kim, and Se-Ho Lee
</p>

<p style="margin: 0.5em 0 1.5em 0; font-size: 0.95em;">
  [<a href="/files/ECCV_2026_manuscript.pdf">Paper</a>]
  [<a href="/files/ECCV_2026_supp.pdf">Supplementary</a>]
  [<a href="/files/ECCV_video_supp.mp4">Video</a>]
  [<a href="https://github.com/oweixx/gast">Code</a>]
</p>

<video width="100%" controls style="margin: 1.5em 0; border-radius: 6px;">
  <source src="/files/ECCV_video_supp.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

We present a geometry-aware style transfer framework for 3D Gaussian Splatting (3DGS) that transfers both appearance attributes and geometric structures. Unlike previous 3DGS stylization methods that mainly focus on color-based changes, our method explicitly adapts scene geometry through a decoupled optimization scheme that alternately updates color and geometry parameters.

The core component is geometry-aware contrastive feature matching (GCFM), which combines RGB, depth, and edge cues into a contrastive objective. This multi-modal guidance helps align rendered 3DGS features with a target style image while preserving stable scene-level optimization. Experiments show that the proposed method achieves superior qualitative fidelity and quantitative performance over existing 3DGS-based stylization methods.

**Publications**

- Min Hyeok Bang*, Jun Hyeong Kim*, Seung-Wook Kim, and Se-Ho Lee, "Geometry-aware style transfer in 3D Gaussian splatting," *in Proc. European Conference on Computer Vision (ECCV)*, Sep. 2026 (Accepted). [[Paper](/files/ECCV_2026_manuscript.pdf)] [[Supplementary](/files/ECCV_2026_supp.pdf)] [[Code](https://github.com/oweixx/gast)]

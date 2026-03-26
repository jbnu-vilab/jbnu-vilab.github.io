---
title: "Demoiréing"
permalink: /research/demoireing/
author_profile: false
---

<a href="/research/">&larr; Back to Research</a>

---

## Demoiréing

<figure style="margin: 1.5em 0; text-align: center;">
  <img src="/files/figure2.png" alt="AVDNet architecture" style="width: 100%; max-width: 900px;">
  <figcaption style="margin-top: 0.5em; font-size: 0.9em; color: #555;">(a) Overview of AVDNet. (b) Architecture of the Adaptive Bandpass Block (ABB). (c) Architecture of the Subtraction-Guided Alignment Block (SGAB).</figcaption>
</figure>

<figure style="margin: 1.5em 0; text-align: center;">
  <img src="/files/figure3.png" alt="Visual comparison results" style="width: 100%; max-width: 900px;">
  <figcaption style="margin-top: 0.5em; font-size: 0.9em; color: #555;">Visual comparison of video demoiréing results against state-of-the-art methods.</figcaption>
</figure>

Moiré artifacts arise from frequency interference between display grids and camera sensors, causing visually disturbing patterns in captured photos and videos. We address both image and video demoiréing by exploiting spectral and temporal characteristics of moiré patterns. Our adaptive video demoiréing network (AVDNet) suppresses moiré adaptively in the implicit frequency domain using an adaptive bandpass filter, and uses inter-frame subtraction maps to guide temporal alignment and prevent propagation of moiré artifacts across frames. For image demoiréing, we propose a multiscale coarse-to-fine strategy that exploits correlations between moiré frequencies at multiple scales.

**Publications**

- Seung-Hun Ok, Young-Min Choi, Seung-Wook Kim, and **Se-Ho Lee**, "Adaptive video demoiréing network with subtraction-guided alignment," *IEEE Signal Processing Letters*, vol. 32, Jul. 2025. \[[DOI](https://doi.org/10.1109/LSP.2025.3585820)\] \[[Code](https://github.com/Oksta1002/AVDNet)\]
- Duong Hai Nguyen, **Se-Ho Lee**, and Chul Lee, "Multiscale coarse-to-fine guided screenshot demoiréing," *IEEE Signal Processing Letters*, vol. 30, pp. 898–902, Jul. 2023. \[[DOI](https://doi.org/10.1109/LSP.2023.3296039)\]

---
title: "Image Enhancement"
permalink: /research/image-enhancement/
author_profile: false
---

<a href="/research/">&larr; Back to Research</a>

---

## Image Enhancement Based on Pigment Representation

<figure style="margin: 2em 0; text-align: center;">
  <img src="/files/figure6.png" alt="Qualitative comparison for tone mapping" style="width: 100%;">
  <figcaption style="margin-top: 0.5em; font-size: 0.88em; color: #555;">Fig. 1. Comparisons of the (a) 1D LUT-based method, (b) 3D LUT-based method, and (c) the proposed pigment representation-based method. In (c), the input image is first converted into a set of pigments, which are then transformed using pigment reprojection functions. The reprojected pigments are subsequently combined to reconstruct the enhanced image.</figcaption>
</figure>

<figure style="margin: 1.5em 0; text-align: center;">
  <img src="/files/figure1.png" alt="Pigment representation framework" style="width: 100%;">
  <figcaption style="margin-top: 0.5em; font-size: 0.88em; color: #555;">Fig. 2. Overall framework of the proposed pigment representation-based image enhancement method.</figcaption>
</figure>

We develop deep learning-based image enhancement methods that adaptively improve visual quality across diverse conditions. Our core approach transforms input RGB colors into a high-dimensional *pigment* representation customized for each image, enabling complex color mappings that go beyond conventional pre-defined color spaces such as RGB or CIE LAB. The pigment-based method consists of five stages: visual encoder, pigment expansion, pigment reprojection, pigment blending, and RGB reconstruction.



<figure style="margin: 2em 0; text-align: center;">
  <img src="/files/figure5.png" alt="Qualitative comparison for photo retouching" style="width: 100%;">
  <figcaption style="margin-top: 0.5em; font-size: 0.88em; color: #555;">Fig. 3. Qualitative comparisons on the MIT-Adobe FiveK dataset for photo retouching: (a) shows GT (retouched by expert C) with its corresponding input image. (b), (c), and (d) show the resultant images and their corresponding error maps obtained by 4D LUT, CoTF, and the proposed method, respectively.</figcaption>
</figure>

<div style="overflow-x: auto; margin: 2em 0;">
<table style="border-collapse: collapse; font-size: 0.83em; text-align: center; width: 100%; min-width: 480px;">
<caption style="caption-side: top; text-align: left; font-weight: bold; padding-bottom: 6px;">
TABLE I. Quantitative comparisons on MIT-Adobe FiveK (480p) for photo retouching. Best result is <strong>bold</strong>.
</caption>
<thead style="background: #f2f2f2;">
<tr>
<th style="border: 1px solid #ccc; padding: 5px 10px; text-align: left;">Method</th>
<th style="border: 1px solid #ccc; padding: 5px 10px;">PSNR ↑</th>
<th style="border: 1px solid #ccc; padding: 5px 10px;">SSIM ↑</th>
<th style="border: 1px solid #ccc; padding: 5px 10px;">&#916;E<sub>ab</sub> ↓</th>
<th style="border: 1px solid #ccc; padding: 5px 10px;"># Params.</th>
<th style="border: 1px solid #ccc; padding: 5px 10px;">Runtime</th>
</tr>
</thead>
<tbody>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">UPE</td><td style="border:1px solid #ccc;padding:4px 8px;">21.88</td><td style="border:1px solid #ccc;padding:4px 8px;">0.853</td><td style="border:1px solid #ccc;padding:4px 8px;">10.80</td><td style="border:1px solid #ccc;padding:4px 8px;">927.1K</td><td style="border:1px solid #ccc;padding:4px 8px;">—</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">DPE</td><td style="border:1px solid #ccc;padding:4px 8px;">23.75</td><td style="border:1px solid #ccc;padding:4px 8px;">0.908</td><td style="border:1px solid #ccc;padding:4px 8px;">9.34</td><td style="border:1px solid #ccc;padding:4px 8px;">3.4M</td><td style="border:1px solid #ccc;padding:4px 8px;">—</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">HDRNet</td><td style="border:1px solid #ccc;padding:4px 8px;">24.66</td><td style="border:1px solid #ccc;padding:4px 8px;">0.915</td><td style="border:1px solid #ccc;padding:4px 8px;">8.06</td><td style="border:1px solid #ccc;padding:4px 8px;">483.1K</td><td style="border:1px solid #ccc;padding:4px 8px;">—</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">CSRNet</td><td style="border:1px solid #ccc;padding:4px 8px;">25.17</td><td style="border:1px solid #ccc;padding:4px 8px;">0.921</td><td style="border:1px solid #ccc;padding:4px 8px;">7.75</td><td style="border:1px solid #ccc;padding:4px 8px;">36.4K</td><td style="border:1px solid #ccc;padding:4px 8px;">0.71ms</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">DeepLPF</td><td style="border:1px solid #ccc;padding:4px 8px;">24.73</td><td style="border:1px solid #ccc;padding:4px 8px;">0.916</td><td style="border:1px solid #ccc;padding:4px 8px;">7.99</td><td style="border:1px solid #ccc;padding:4px 8px;">1.7M</td><td style="border:1px solid #ccc;padding:4px 8px;">36.69ms</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">3D LUT</td><td style="border:1px solid #ccc;padding:4px 8px;">25.29</td><td style="border:1px solid #ccc;padding:4px 8px;">0.920</td><td style="border:1px solid #ccc;padding:4px 8px;">7.55</td><td style="border:1px solid #ccc;padding:4px 8px;">593.5K</td><td style="border:1px solid #ccc;padding:4px 8px;">0.80ms</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">SepLUT</td><td style="border:1px solid #ccc;padding:4px 8px;">25.47</td><td style="border:1px solid #ccc;padding:4px 8px;">0.921</td><td style="border:1px solid #ccc;padding:4px 8px;">7.54</td><td style="border:1px solid #ccc;padding:4px 8px;">119.8K</td><td style="border:1px solid #ccc;padding:4px 8px;">6.20ms</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">AdaInt</td><td style="border:1px solid #ccc;padding:4px 8px;">25.49</td><td style="border:1px solid #ccc;padding:4px 8px;">0.926</td><td style="border:1px solid #ccc;padding:4px 8px;">7.47</td><td style="border:1px solid #ccc;padding:4px 8px;">619.7K</td><td style="border:1px solid #ccc;padding:4px 8px;">1.89ms</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">RSFNet</td><td style="border:1px solid #ccc;padding:4px 8px;">25.49</td><td style="border:1px solid #ccc;padding:4px 8px;">0.924</td><td style="border:1px solid #ccc;padding:4px 8px;">7.23</td><td style="border:1px solid #ccc;padding:4px 8px;">16.1M</td><td style="border:1px solid #ccc;padding:4px 8px;">7.28ms</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">4D LUT</td><td style="border:1px solid #ccc;padding:4px 8px;">25.50</td><td style="border:1px solid #ccc;padding:4px 8px;">0.931</td><td style="border:1px solid #ccc;padding:4px 8px;">7.27</td><td style="border:1px solid #ccc;padding:4px 8px;">924.4K</td><td style="border:1px solid #ccc;padding:4px 8px;">1.25ms</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">HashLUT</td><td style="border:1px solid #ccc;padding:4px 8px;">25.50</td><td style="border:1px solid #ccc;padding:4px 8px;">0.926</td><td style="border:1px solid #ccc;padding:4px 8px;">7.46</td><td style="border:1px solid #ccc;padding:4px 8px;">114.0K</td><td style="border:1px solid #ccc;padding:4px 8px;">—</td></tr>
<tr><td style="border:1px solid #ccc;padding:4px 10px;text-align:left;">CoTF</td><td style="border:1px solid #ccc;padding:4px 8px;">25.54</td><td style="border:1px solid #ccc;padding:4px 8px;">0.938</td><td style="border:1px solid #ccc;padding:4px 8px;">7.46</td><td style="border:1px solid #ccc;padding:4px 8px;">310.0K</td><td style="border:1px solid #ccc;padding:4px 8px;">4.28ms</td></tr>
<tr style="background:#fffde7;">
<td style="border:1px solid #ccc;padding:4px 10px;text-align:left;"><strong>Proposed</strong></td>
<td style="border:1px solid #ccc;padding:4px 8px;"><strong>25.82</strong></td>
<td style="border:1px solid #ccc;padding:4px 8px;"><strong>0.939</strong></td>
<td style="border:1px solid #ccc;padding:4px 8px;"><strong>7.15</strong></td>
<td style="border:1px solid #ccc;padding:4px 8px;">765.0K</td>
<td style="border:1px solid #ccc;padding:4px 8px;">1.43ms</td>
</tr>
</tbody>
</table>
</div>

**Publications**

- Se-Ho Lee, Keunsoo Koh, and Seung-Wook Kim, "Image enhancement based on pigment representation," *IEEE Transactions on Multimedia*, 2026. \[[DOI](https://doi.org/10.1109/TMM.2026.3654419)\] \[[Project](https://github.com/jbnu-vilab/pigment_enhancement)\]
- Se-Ho Lee and Seung-Wook Kim, "DCPNet: Deformable control point network for image enhancement," *Journal of Visual Communication and Image Representation*, vol. 104, pp. 104308, Oct. 2024. \[[DOI](https://doi.org/10.1016/j.jvcir.2024.104308)\]

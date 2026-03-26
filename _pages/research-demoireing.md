---
title: "Image/Video Demoiréing"
permalink: /research/demoireing/
author_profile: false
---

<a href="/research/">&larr; Back to Research</a>

---

## Adaptive Video Demoiréing Network with Subtraction-Guided Alignment

<figure style="margin: 1.5em auto; text-align: center; max-width: 65%;">
  <img src="/files/fig2a.png" alt="Overview of AVDNet" style="width:100%;">
</figure>

<figure style="margin: 1.5em auto; text-align: center; max-width: 65%;">
  <img src="/files/fig2b.png" alt="Architecture of ABB" style="width:100%;">
</figure>

<figure style="margin: 1.5em auto; text-align: center; max-width: 65%;">
  <img src="/files/fig2c.png" alt="Architecture of SGAB" style="width:100%;">
</figure>

<p style="text-align:center; font-size:0.88em; color:#555; margin-top:0;">Fig. 1. AVDNet architecture.</p>

Moiré artifacts arise from frequency interference between display grids and camera sensors, causing visually disturbing patterns in captured photos and videos. We address both image and video demoiréing by exploiting spectral and temporal characteristics of moiré patterns. Our adaptive video demoiréing network (AVDNet) suppresses moiré adaptively in the implicit frequency domain via a learnable bandpass filter (ABB), and uses inter-frame subtraction maps to guide temporal alignment and prevent moiré propagation across frames (SGAB). For image demoiréing, we propose a multiscale coarse-to-fine strategy that exploits correlations between moiré frequencies at multiple scales.

<figure style="margin: 2em 0; text-align: center;">
  <img src="/files/figure3.png" alt="Visual comparison of demoiréing results" style="width: 100%;">
  <figcaption style="margin-top: 0.5em; font-size: 0.88em; color: #555;">Fig. 2. Qualitative comparison on VDmoire dataset: (a) Input, (b) VDmoire, (c) DTNet, (d) Ours, (e) GT.</figcaption>
</figure>

<div style="overflow-x: auto; margin: 2em 0;">
<table style="border-collapse: collapse; font-size: 0.78em; text-align: center; width: 100%; min-width: 700px;">
<caption style="caption-side: top; text-align: left; font-weight: bold; padding-bottom: 6px;">
TABLE I. Quantitative comparison on VDmoire dataset. <strong>Bold</strong>: best, <u>underline</u>: 2nd best.
</caption>
<thead style="background: #f2f2f2;">
<tr>
<th style="border:1px solid #ccc;padding:4px 6px;" rowspan="2">Method</th>
<th style="border:1px solid #ccc;padding:4px 6px;" colspan="3">TCL-V1</th>
<th style="border:1px solid #ccc;padding:4px 6px;" colspan="3">TCL-V2</th>
<th style="border:1px solid #ccc;padding:4px 6px;" colspan="3">iPhone-V1</th>
<th style="border:1px solid #ccc;padding:4px 6px;" colspan="3">iPhone-V2</th>
<th style="border:1px solid #ccc;padding:4px 6px;" colspan="3">Complexity</th>
</tr>
<tr>
<th style="border:1px solid #ccc;padding:3px 5px;">PSNR↑</th><th style="border:1px solid #ccc;padding:3px 5px;">SSIM↑</th><th style="border:1px solid #ccc;padding:3px 5px;">LPIPS↓</th>
<th style="border:1px solid #ccc;padding:3px 5px;">PSNR↑</th><th style="border:1px solid #ccc;padding:3px 5px;">SSIM↑</th><th style="border:1px solid #ccc;padding:3px 5px;">LPIPS↓</th>
<th style="border:1px solid #ccc;padding:3px 5px;">PSNR↑</th><th style="border:1px solid #ccc;padding:3px 5px;">SSIM↑</th><th style="border:1px solid #ccc;padding:3px 5px;">LPIPS↓</th>
<th style="border:1px solid #ccc;padding:3px 5px;">PSNR↑</th><th style="border:1px solid #ccc;padding:3px 5px;">SSIM↑</th><th style="border:1px solid #ccc;padding:3px 5px;">LPIPS↓</th>
<th style="border:1px solid #ccc;padding:3px 5px;">Params(M)</th><th style="border:1px solid #ccc;padding:3px 5px;">TFLOPs</th><th style="border:1px solid #ccc;padding:3px 5px;">Runtime(ms)</th>
</tr>
</thead>
<tbody>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">DMCNN</td><td style="border:1px solid #ccc;padding:3px 5px;">20.321</td><td style="border:1px solid #ccc;padding:3px 5px;">0.703</td><td style="border:1px solid #ccc;padding:3px 5px;">0.321</td><td style="border:1px solid #ccc;padding:3px 5px;">20.707</td><td style="border:1px solid #ccc;padding:3px 5px;">0.793</td><td style="border:1px solid #ccc;padding:3px 5px;">0.385</td><td style="border:1px solid #ccc;padding:3px 5px;">21.967</td><td style="border:1px solid #ccc;padding:3px 5px;">0.712</td><td style="border:1px solid #ccc;padding:3px 5px;">0.280</td><td style="border:1px solid #ccc;padding:3px 5px;">21.416</td><td style="border:1px solid #ccc;padding:3px 5px;">0.749</td><td style="border:1px solid #ccc;padding:3px 5px;">0.496</td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>1.43</strong></td><td style="border:1px solid #ccc;padding:3px 5px;">0.736</td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>32.0</strong></td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">WDNet</td><td style="border:1px solid #ccc;padding:3px 5px;">19.650</td><td style="border:1px solid #ccc;padding:3px 5px;">0.726</td><td style="border:1px solid #ccc;padding:3px 5px;">0.289</td><td style="border:1px solid #ccc;padding:3px 5px;">20.334</td><td style="border:1px solid #ccc;padding:3px 5px;">0.847</td><td style="border:1px solid #ccc;padding:3px 5px;">0.288</td><td style="border:1px solid #ccc;padding:3px 5px;">19.818</td><td style="border:1px solid #ccc;padding:3px 5px;">0.722</td><td style="border:1px solid #ccc;padding:3px 5px;">0.300</td><td style="border:1px solid #ccc;padding:3px 5px;">20.613</td><td style="border:1px solid #ccc;padding:3px 5px;">0.832</td><td style="border:1px solid #ccc;padding:3px 5px;">0.297</td><td style="border:1px solid #ccc;padding:3px 5px;">3.92</td><td style="border:1px solid #ccc;padding:3px 5px;">3.100</td><td style="border:1px solid #ccc;padding:3px 5px;">63.1</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">ESDNet</td><td style="border:1px solid #ccc;padding:3px 5px;">22.026</td><td style="border:1px solid #ccc;padding:3px 5px;">0.734</td><td style="border:1px solid #ccc;padding:3px 5px;">0.199</td><td style="border:1px solid #ccc;padding:3px 5px;">24.898</td><td style="border:1px solid #ccc;padding:3px 5px;">0.874</td><td style="border:1px solid #ccc;padding:3px 5px;">0.163</td><td style="border:1px solid #ccc;padding:3px 5px;">22.537</td><td style="border:1px solid #ccc;padding:3px 5px;">0.751</td><td style="border:1px solid #ccc;padding:3px 5px;">0.218</td><td style="border:1px solid #ccc;padding:3px 5px;">25.064</td><td style="border:1px solid #ccc;padding:3px 5px;">0.853</td><td style="border:1px solid #ccc;padding:3px 5px;">0.165</td><td style="border:1px solid #ccc;padding:3px 5px;">5.93</td><td style="border:1px solid #ccc;padding:3px 5px;">4.484</td><td style="border:1px solid #ccc;padding:3px 5px;"><u>43.6</u></td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">VDmoire</td><td style="border:1px solid #ccc;padding:3px 5px;">21.725</td><td style="border:1px solid #ccc;padding:3px 5px;">0.733</td><td style="border:1px solid #ccc;padding:3px 5px;">0.202</td><td style="border:1px solid #ccc;padding:3px 5px;">23.460</td><td style="border:1px solid #ccc;padding:3px 5px;">0.857</td><td style="border:1px solid #ccc;padding:3px 5px;">0.163</td><td style="border:1px solid #ccc;padding:3px 5px;">21.990</td><td style="border:1px solid #ccc;padding:3px 5px;">0.707</td><td style="border:1px solid #ccc;padding:3px 5px;">0.221</td><td style="border:1px solid #ccc;padding:3px 5px;">25.230</td><td style="border:1px solid #ccc;padding:3px 5px;"><u>0.860</u></td><td style="border:1px solid #ccc;padding:3px 5px;">0.157</td><td style="border:1px solid #ccc;padding:3px 5px;">5.98</td><td style="border:1px solid #ccc;padding:3px 5px;"><u>1.216</u></td><td style="border:1px solid #ccc;padding:3px 5px;">650.2</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">DTNet</td><td style="border:1px solid #ccc;padding:3px 5px;"><u>24.119</u></td><td style="border:1px solid #ccc;padding:3px 5px;"><u>0.801</u></td><td style="border:1px solid #ccc;padding:3px 5px;"><u>0.163</u></td><td style="border:1px solid #ccc;padding:3px 5px;"><u>26.153</u></td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.877</strong></td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.128</strong></td><td style="border:1px solid #ccc;padding:3px 5px;">24.821</td><td style="border:1px solid #ccc;padding:3px 5px;">0.794</td><td style="border:1px solid #ccc;padding:3px 5px;"><u>0.172</u></td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>26.593</strong></td><td style="border:1px solid #ccc;padding:3px 5px;">0.854</td><td style="border:1px solid #ccc;padding:3px 5px;">0.149</td><td style="border:1px solid #ccc;padding:3px 5px;">7.36</td><td style="border:1px solid #ccc;padding:3px 5px;">1.174</td><td style="border:1px solid #ccc;padding:3px 5px;">620.3</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">DTCINet</td><td style="border:1px solid #ccc;padding:3px 5px;">21.881</td><td style="border:1px solid #ccc;padding:3px 5px;">0.744</td><td style="border:1px solid #ccc;padding:3px 5px;">0.181</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;"><u>25.381</u></td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.876</strong></td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.148</strong></td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">5.17</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">STD-Net</td><td style="border:1px solid #ccc;padding:3px 5px;">22.075</td><td style="border:1px solid #ccc;padding:3px 5px;">0.740</td><td style="border:1px solid #ccc;padding:3px 5px;">0.196</td><td style="border:1px solid #ccc;padding:3px 5px;">20.705</td><td style="border:1px solid #ccc;padding:3px 5px;">0.834</td><td style="border:1px solid #ccc;padding:3px 5px;">0.197</td><td style="border:1px solid #ccc;padding:3px 5px;">21.889</td><td style="border:1px solid #ccc;padding:3px 5px;">0.717</td><td style="border:1px solid #ccc;padding:3px 5px;">0.208</td><td style="border:1px solid #ccc;padding:3px 5px;">24.216</td><td style="border:1px solid #ccc;padding:3px 5px;">0.842</td><td style="border:1px solid #ccc;padding:3px 5px;">0.180</td><td style="border:1px solid #ccc;padding:3px 5px;">21.77</td><td style="border:1px solid #ccc;padding:3px 5px;">1.056</td><td style="border:1px solid #ccc;padding:3px 5px;">151.7</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 6px;text-align:left;">FPANet</td><td style="border:1px solid #ccc;padding:3px 5px;">21.953</td><td style="border:1px solid #ccc;padding:3px 5px;">0.784</td><td style="border:1px solid #ccc;padding:3px 5px;">0.173</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;"><u>25.446</u></td><td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.883</strong></td><td style="border:1px solid #ccc;padding:3px 5px;"><u>0.146</u></td><td style="border:1px solid #ccc;padding:3px 5px;">68.89</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td><td style="border:1px solid #ccc;padding:3px 5px;">—</td></tr>
<tr style="background:#fffde7;">
<td style="border:1px solid #ccc;padding:3px 6px;text-align:left;"><strong>Ours</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>24.730</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.819</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.140</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>26.478</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.877</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.128</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>25.492</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><u>0.810</u></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.148</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>26.593</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;">0.855</td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.131</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><u>4.16</u></td>
<td style="border:1px solid #ccc;padding:3px 5px;"><strong>0.540</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;">52.3</td>
</tr>
</tbody>
</table>
</div>

**Publications**

- Seung-Hun Ok, Young-Min Choi, Seung-Wook Kim, and Se-Ho Lee, "Adaptive video demoiréing network with subtraction-guided alignment," *IEEE Signal Processing Letters*, vol. 32, Jul. 2025. \[[DOI](https://doi.org/10.1109/LSP.2025.3585820)\] \[[Code](https://github.com/Oksta1002/AVDNet)\]
- Duong Hai Nguyen, Se-Ho Lee, and Chul Lee, "Multiscale coarse-to-fine guided screenshot demoiréing," *IEEE Signal Processing Letters*, vol. 30, pp. 898–902, Jul. 2023. \[[DOI](https://doi.org/10.1109/LSP.2023.3296039)\]

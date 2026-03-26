---
title: "Image Quality Assessment"
permalink: /research/iqa/
author_profile: false
---

<a href="/research/">&larr; Back to Research</a>

---

## Dual-Branch Vision Transformer for Blind Image Quality Assessment

<figure style="margin: 1.5em 0; text-align: center;">
  <img src="/files/figure4.png" alt="Dual-branch vision transformer for BIQA" style="width: 100%;">
  <figcaption style="margin-top: 0.5em; font-size: 0.88em; color: #555;">Fig. 1. The proposed dual-branch vision transformer for blind image quality assessment (BIQA).</figcaption>
</figure>

Blind image quality assessment (BIQA) aims to predict the perceptual quality of an image without access to a reference. We propose a dual-branch vision transformer that simultaneously considers both local distortions and global semantic information. Dual-scale features (S-Feature and L-Feature) are extracted from a ResNet-50 backbone and fed into separate transformer encoder branches. Each branch captures scale-variant local distortions through local feature embeddings, and jointly models global distortion context via content-aware IQA (CA-IQA) embeddings. The outputs of both branches are combined through feed-forward blocks to predict the final image quality score.

<div style="overflow-x: auto; margin: 2em 0;">
<table style="border-collapse: collapse; font-size: 0.82em; text-align: center; width: 100%; min-width: 560px;">
<caption style="caption-side: top; text-align: left; font-weight: bold; padding-bottom: 6px;">
TABLE 1. Average SRCC results on six IQA databases. Best and second-best results are <strong>bold</strong> and <u>underlined</u>, respectively.
</caption>
<thead style="background: #f2f2f2;">
<tr>
<th style="border:1px solid #ccc;padding:4px 6px;" rowspan="2">Method</th>
<th style="border:1px solid #ccc;padding:4px 6px;" colspan="6">SRCC</th>
</tr>
<tr>
<th style="border:1px solid #ccc;padding:3px 5px;">LIVEC</th>
<th style="border:1px solid #ccc;padding:3px 5px;">TID2013</th>
<th style="border:1px solid #ccc;padding:3px 5px;">LIVE</th>
<th style="border:1px solid #ccc;padding:3px 5px;">CSIQ</th>
<th style="border:1px solid #ccc;padding:3px 5px;">LIVE MD</th>
<th style="border:1px solid #ccc;padding:3px 5px;">KADID-10k</th>
</tr>
</thead>
<tbody>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">BRISQUE</td><td style="border:1px solid #ccc;padding:3px 5px;">0.608</td><td style="border:1px solid #ccc;padding:3px 5px;">0.604</td><td style="border:1px solid #ccc;padding:3px 5px;">0.939</td><td style="border:1px solid #ccc;padding:3px 5px;">0.746</td><td style="border:1px solid #ccc;padding:3px 5px;">0.886</td><td style="border:1px solid #ccc;padding:3px 5px;">0.528</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">M3</td><td style="border:1px solid #ccc;padding:3px 5px;">0.607</td><td style="border:1px solid #ccc;padding:3px 5px;">0.689</td><td style="border:1px solid #ccc;padding:3px 5px;">0.951</td><td style="border:1px solid #ccc;padding:3px 5px;">0.795</td><td style="border:1px solid #ccc;padding:3px 5px;">0.892</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">FRIQUEE</td><td style="border:1px solid #ccc;padding:3px 5px;">0.682</td><td style="border:1px solid #ccc;padding:3px 5px;">0.680</td><td style="border:1px solid #ccc;padding:3px 5px;">0.940</td><td style="border:1px solid #ccc;padding:3px 5px;">0.835</td><td style="border:1px solid #ccc;padding:3px 5px;">0.923</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">CORNIA</td><td style="border:1px solid #ccc;padding:3px 5px;">0.629</td><td style="border:1px solid #ccc;padding:3px 5px;">0.678</td><td style="border:1px solid #ccc;padding:3px 5px;">0.947</td><td style="border:1px solid #ccc;padding:3px 5px;">0.678</td><td style="border:1px solid #ccc;padding:3px 5px;">0.899</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">HOSA</td><td style="border:1px solid #ccc;padding:3px 5px;">0.640</td><td style="border:1px solid #ccc;padding:3px 5px;">0.735</td><td style="border:1px solid #ccc;padding:3px 5px;">0.946</td><td style="border:1px solid #ccc;padding:3px 5px;">0.741</td><td style="border:1px solid #ccc;padding:3px 5px;">0.913</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">Le-CNN</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">0.956</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">BIECON</td><td style="border:1px solid #ccc;padding:3px 5px;">0.595</td><td style="border:1px solid #ccc;padding:3px 5px;">0.717</td><td style="border:1px solid #ccc;padding:3px 5px;">0.961</td><td style="border:1px solid #ccc;padding:3px 5px;">0.815</td><td style="border:1px solid #ccc;padding:3px 5px;">0.909</td><td style="border:1px solid #ccc;padding:3px 5px;">0.623</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">DIQaM-NR</td><td style="border:1px solid #ccc;padding:3px 5px;">0.606</td><td style="border:1px solid #ccc;padding:3px 5px;">0.835</td><td style="border:1px solid #ccc;padding:3px 5px;">0.960</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">WaDIQaM-NR</td><td style="border:1px solid #ccc;padding:3px 5px;">0.671</td><td style="border:1px solid #ccc;padding:3px 5px;">0.761</td><td style="border:1px solid #ccc;padding:3px 5px;">0.954</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">0.739</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">ResNet-ft</td><td style="border:1px solid #ccc;padding:3px 5px;">0.819</td><td style="border:1px solid #ccc;padding:3px 5px;">0.712</td><td style="border:1px solid #ccc;padding:3px 5px;">0.950</td><td style="border:1px solid #ccc;padding:3px 5px;">0.876</td><td style="border:1px solid #ccc;padding:3px 5px;">0.909</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">IW-CNN</td><td style="border:1px solid #ccc;padding:3px 5px;">0.663</td><td style="border:1px solid #ccc;padding:3px 5px;">0.800</td><td style="border:1px solid #ccc;padding:3px 5px;">0.963</td><td style="border:1px solid #ccc;padding:3px 5px;">0.812</td><td style="border:1px solid #ccc;padding:3px 5px;">0.914</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">DBCNN</td><td style="border:1px solid #ccc;padding:3px 5px;">0.851</td><td style="border:1px solid #ccc;padding:3px 5px;">0.816</td><td style="border:1px solid #ccc;padding:3px 5px;">0.968</td><td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.946</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.927</td><td style="border:1px solid #ccc;padding:3px 5px;">0.851</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">HyperIQA</td><td style="border:1px solid #ccc;padding:3px 5px;">0.859</td><td style="border:1px solid #ccc;padding:3px 5px;">0.797</td><td style="border:1px solid #ccc;padding:3px 5px;">0.962</td><td style="border:1px solid #ccc;padding:3px 5px;">0.923</td><td style="border:1px solid #ccc;padding:3px 5px;">0.898</td><td style="border:1px solid #ccc;padding:3px 5px;">0.852</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">TReS</td><td style="border:1px solid #ccc;padding:3px 5px;">0.846</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.863</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.969</td><td style="border:1px solid #ccc;padding:3px 5px;">0.922</td><td style="border:1px solid #ccc;padding:3px 5px;">0.916</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.859</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">BIQA, M.D.</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">0.835</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.969</td><td style="border:1px solid #ccc;padding:3px 5px;">0.903</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">RNSA</td><td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.871</td><td style="border:1px solid #ccc;padding:3px 5px;">0.849</td><td style="border:1px solid #ccc;padding:3px 5px;">0.969</td><td style="border:1px solid #ccc;padding:3px 5px;">0.931</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">0.855</td></tr>
<tr style="background:#fffde7;">
<td style="border:1px solid #ccc;padding:3px 8px;text-align:left;"><strong>Proposed</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.862</td>
<td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.877</td>
<td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.976</td>
<td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.942</td>
<td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.935</td>
<td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.970</td>
</tr>
</tbody>
</table>
</div>

<div style="overflow-x: auto; margin: 1em 0 2em 0;">
<table style="border-collapse: collapse; font-size: 0.82em; text-align: center; width: 100%; min-width: 560px;">
<caption style="caption-side: top; text-align: left; font-weight: bold; padding-bottom: 6px;">
TABLE 2. Average PLCC results on six IQA databases. Best and second-best results are <strong>bold</strong> and <u>underlined</u>, respectively.
</caption>
<thead style="background: #f2f2f2;">
<tr>
<th style="border:1px solid #ccc;padding:4px 6px;" rowspan="2">Method</th>
<th style="border:1px solid #ccc;padding:4px 6px;" colspan="6">PLCC</th>
</tr>
<tr>
<th style="border:1px solid #ccc;padding:3px 5px;">LIVEC</th>
<th style="border:1px solid #ccc;padding:3px 5px;">TID2013</th>
<th style="border:1px solid #ccc;padding:3px 5px;">LIVE</th>
<th style="border:1px solid #ccc;padding:3px 5px;">CSIQ</th>
<th style="border:1px solid #ccc;padding:3px 5px;">LIVE MD</th>
<th style="border:1px solid #ccc;padding:3px 5px;">KADID-10k</th>
</tr>
</thead>
<tbody>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">BRISQUE</td><td style="border:1px solid #ccc;padding:3px 5px;">0.629</td><td style="border:1px solid #ccc;padding:3px 5px;">0.694</td><td style="border:1px solid #ccc;padding:3px 5px;">0.935</td><td style="border:1px solid #ccc;padding:3px 5px;">0.829</td><td style="border:1px solid #ccc;padding:3px 5px;">0.917</td><td style="border:1px solid #ccc;padding:3px 5px;">0.567</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">M3</td><td style="border:1px solid #ccc;padding:3px 5px;">0.630</td><td style="border:1px solid #ccc;padding:3px 5px;">0.771</td><td style="border:1px solid #ccc;padding:3px 5px;">0.950</td><td style="border:1px solid #ccc;padding:3px 5px;">0.839</td><td style="border:1px solid #ccc;padding:3px 5px;">0.919</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">FRIQUEE</td><td style="border:1px solid #ccc;padding:3px 5px;">0.705</td><td style="border:1px solid #ccc;padding:3px 5px;">0.753</td><td style="border:1px solid #ccc;padding:3px 5px;">0.944</td><td style="border:1px solid #ccc;padding:3px 5px;">0.874</td><td style="border:1px solid #ccc;padding:3px 5px;">0.934</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">CORNIA</td><td style="border:1px solid #ccc;padding:3px 5px;">0.671</td><td style="border:1px solid #ccc;padding:3px 5px;">0.768</td><td style="border:1px solid #ccc;padding:3px 5px;">0.950</td><td style="border:1px solid #ccc;padding:3px 5px;">0.776</td><td style="border:1px solid #ccc;padding:3px 5px;">0.921</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">HOSA</td><td style="border:1px solid #ccc;padding:3px 5px;">0.678</td><td style="border:1px solid #ccc;padding:3px 5px;">0.815</td><td style="border:1px solid #ccc;padding:3px 5px;">0.947</td><td style="border:1px solid #ccc;padding:3px 5px;">0.823</td><td style="border:1px solid #ccc;padding:3px 5px;">0.926</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">Le-CNN</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">0.953</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">BIECON</td><td style="border:1px solid #ccc;padding:3px 5px;">0.613</td><td style="border:1px solid #ccc;padding:3px 5px;">0.762</td><td style="border:1px solid #ccc;padding:3px 5px;">0.962</td><td style="border:1px solid #ccc;padding:3px 5px;">0.823</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.933</td><td style="border:1px solid #ccc;padding:3px 5px;">0.648</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">DIQaM-NR</td><td style="border:1px solid #ccc;padding:3px 5px;">0.601</td><td style="border:1px solid #ccc;padding:3px 5px;">0.855</td><td style="border:1px solid #ccc;padding:3px 5px;">0.972</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">WaDIQaM-NR</td><td style="border:1px solid #ccc;padding:3px 5px;">0.680</td><td style="border:1px solid #ccc;padding:3px 5px;">0.787</td><td style="border:1px solid #ccc;padding:3px 5px;">0.963</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">0.752</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">ResNet-ft</td><td style="border:1px solid #ccc;padding:3px 5px;">0.849</td><td style="border:1px solid #ccc;padding:3px 5px;">0.756</td><td style="border:1px solid #ccc;padding:3px 5px;">0.954</td><td style="border:1px solid #ccc;padding:3px 5px;">0.905</td><td style="border:1px solid #ccc;padding:3px 5px;">0.920</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">IW-CNN</td><td style="border:1px solid #ccc;padding:3px 5px;">0.705</td><td style="border:1px solid #ccc;padding:3px 5px;">0.802</td><td style="border:1px solid #ccc;padding:3px 5px;">0.964</td><td style="border:1px solid #ccc;padding:3px 5px;">0.791</td><td style="border:1px solid #ccc;padding:3px 5px;">0.929</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">DBCNN</td><td style="border:1px solid #ccc;padding:3px 5px;">0.869</td><td style="border:1px solid #ccc;padding:3px 5px;">0.865</td><td style="border:1px solid #ccc;padding:3px 5px;">0.971</td><td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.959</td><td style="border:1px solid #ccc;padding:3px 5px;">0.869</td><td style="border:1px solid #ccc;padding:3px 5px;">0.856</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">HyperIQA</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.882</td><td style="border:1px solid #ccc;padding:3px 5px;">0.823</td><td style="border:1px solid #ccc;padding:3px 5px;">0.966</td><td style="border:1px solid #ccc;padding:3px 5px;">0.942</td><td style="border:1px solid #ccc;padding:3px 5px;">0.924</td><td style="border:1px solid #ccc;padding:3px 5px;">0.845</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">TReS</td><td style="border:1px solid #ccc;padding:3px 5px;">0.877</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.883</td><td style="border:1px solid #ccc;padding:3px 5px;">0.968</td><td style="border:1px solid #ccc;padding:3px 5px;">0.942</td><td style="border:1px solid #ccc;padding:3px 5px;">0.921</td><td style="border:1px solid #ccc;padding:3px 5px;">0.858</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">BIQA, M.D.</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">0.859</td><td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.978</td><td style="border:1px solid #ccc;padding:3px 5px;">0.925</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td></tr>
<tr><td style="border:1px solid #ccc;padding:3px 8px;text-align:left;">RNSA</td><td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.883</td><td style="border:1px solid #ccc;padding:3px 5px;">0.861</td><td style="border:1px solid #ccc;padding:3px 5px;">0.972</td><td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.959</td><td style="border:1px solid #ccc;padding:3px 5px;">-</td><td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.859</td></tr>
<tr style="background:#fffde7;">
<td style="border:1px solid #ccc;padding:3px 8px;text-align:left;"><strong>Proposed</strong></td>
<td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.882</td>
<td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.894</td>
<td style="border:1px solid #ccc;padding:3px 5px;text-decoration:underline;">0.976</td>
<td style="border:1px solid #ccc;padding:3px 5px;">0.952</td>
<td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.935</td>
<td style="border:1px solid #ccc;padding:3px 5px;font-weight:bold;">0.971</td>
</tr>
</tbody>
</table>
</div>

**Publications**

- Se-Ho Lee and Seung-Wook Kim, "Dual-branch vision transformer for blind image quality assessment," *Journal of Visual Communication and Image Representation*, vol. 94, pp. 103850, Jun. 2023. \[[DOI](https://doi.org/10.1016/j.jvcir.2023.103850)\]

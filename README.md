# CommercePilot models

ONNX re-exports of a third-party background-removal model, hosted so the CommercePilot desktop app can download
them on the user's request. The app pins every file by SHA-256 and refuses anything else.

## BiRefNet (general, Swin-v1-tiny) — release `birefnet-swin-tiny-onnx-v1`

| File | Input | SHA-256 | Bytes |
|---|---|---|---|
| `birefnet-swin-tiny-768.onnx` | 768 × 768 | `d797c03c62444efeac80801a674aa121953984f0896dc1cab6474da15a89b4bf` | 205,143,264 |
| `birefnet-swin-tiny-512.onnx` | 512 × 512 | `95bb6ff512597b2691eae3633bba57f33bfcaa87db9fa0bbe41d2c994ea1b249` | 191,933,648 |

- **Source weights:** `BiRefNet-general-bb_swin_v1_tiny-epoch_232.pth` from
  [ZhengPeng7/BiRefNet release v1](https://github.com/ZhengPeng7/BiRefNet/releases/tag/v1)
  (SHA-256 `6a1e050c6ec2697e5ed268455df544782b023acf8643ab771250979094875ab1`).
- **What changed:** the weights are unchanged. They were exported to ONNX at fixed input sizes of 768 px and 512 px
  (the upstream ONNX is 1024 px and needs 6–7 GB of memory). Input is RGB normalised with ImageNet mean/std; output is
  the mask logits.
- **Licence:** MIT, © 2024 ZhengPeng — see [LICENSE](LICENSE). The licence and copyright notice apply to these
  derived files.
- **Paper:** Zheng et al., *Bilateral Reference for High-Resolution Dichotomous Image Segmentation*, CAAI AIR 2024.

These files are provided as is, without warranty. They are not an official upstream release.

# 🖼️ Stable Diffusion — Custom Implementation

This repository contains a minimal, modular, and fully Python-based implementation of **Stable Diffusion v1.5**, including CLIP text encoding, the UNet + DDPM denoising process, and VAE encoding/decoding.  
It uses the official **v1-5-pruned-emaonly.ckpt** model weights and supports prompt-based image generation.

---

## 🚀 Features

- ✔️ End-to-end Stable Diffusion v1.5 inference  
- ✔️ CLIP tokenizer + text encoder (using `vocab.json` and `merges.txt`)  
- ✔️ VAE encoder/decoder fully implemented from scratch  
- ✔️ UNet with 2D attention and cross-attention  
- ✔️ DDPM scheduler with classifier-free guidance  
- ✔️ Modular and easy-to-read architecture  

---

## 🔗 Google Colab Notebook

You can try the full working implementation directly in Google Colab:

👉 **[Open the Colab Notebook](https://colab.research.google.com/github/VasuVerma990/Stable-Diffusion/blob/_Main_.ipynb)**


---

## 🔄 Pipeline Overview

The Stable Diffusion inference pipeline follows the official v1.5 process:

1. **Tokenize prompt** (BPE using `vocab.json` + `merges.txt`)  
2. **Encode text** using the CLIP text transformer  
3. **Sample initial Gaussian noise** in latent space  
4. **Iteratively denoise** using UNet + DDPM scheduler  
5. **Decode final latents** into an RGB image with the VAE decoder  

---

## 📝 Notes

- This repository emphasizes **clarity and modularity** in implementation.  
- Includes full support for **classifier-free guidance**.  
- Requires **`vocab.json`** and **`merges.txt`** for CLIP tokenizer functionality.  

---


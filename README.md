
This repository contains code for our paper:

**“The Deployment Gap in AI Media Detection: Platform-Aware and Visually Constrained Adversarial Evaluation”**

---

## Overview

AI-generated image detectors achieve near-perfect performance under standard evaluation settings.  
However, these evaluations do not reflect real-world deployment conditions.

We show that:

- Detection performance degrades significantly under **deployment-aware transformations**
- **Localized (meme-style) perturbations** can flip predictions from *fake → real*
- Attacks remain effective even under **stochastic platform pipelines (EOT)**

---

##  Key Contributions

- **Deployment-aware attack formulation** using differentiable transformations (resize, JPEG, blur)
- **Masked adversarial attacks** constrained to meme-style top/bottom bands
- **EOT-based optimization** to ensure robustness under stochastic transforms
- Comprehensive evaluation:
  - Per-image attacks
  - Universal attacks
  - Ensemble robustness
  - Calibration and confidence analysis

---

##  Repository Structure

```bash
.
├── baseline.ipynb      # Train + evaluate clean detection models
├── attacks.ipynb       # Deployment-aware masked EOT attacks
├── evaluation.ipynb    # Metrics, plots, calibration, analysis
├── fake_images.zip     # (Optional) Synthetic dataset

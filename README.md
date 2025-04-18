# Comparing different GANS on ChestMNIST Dataset

This project focuses on generating synthetic medical images using Generative Adversarial Networks (GANs) trained on the ChestMNIST dataset. Performance is evaluated using metrics like the Inception Score (IS), Fréchet Inception Distance (FID), and visual assessments.

## Project Overview
The primary objective is to explore and compare various GAN architectures in the context of medical image generation. The implemented models include:

Least Squares GAN (LS-GAN)

Wasserstein GAN (WGAN)

Wasserstein GAN with Gradient Penalty (WGAN-GP)

## 📌 Objective

The aim is to experiment with different GAN models for medical image generation and evaluate them using:

- **Inception Score (IS)**
- **Fréchet Inception Distance (FID)**
- **Visual Analysis**

## 📌 Implemented GAN Architectures

### 1. Least Squares GAN (LS-GAN)
- Replaces binary cross-entropy with a **least-squares loss function**.
- Minimizes the **Pearson χ² divergence** for improved image quality and stable training.

### 2. Wasserstein GAN (WGAN)
- Introduces the **Wasserstein (Earth Mover's) Distance**.
- Replaces the discriminator with a **critic** to prevent mode collapse and vanishing gradients.

### 3. Wasserstein GAN with Gradient Penalty (WGAN-GP)
- Enhances WGAN by adding a **gradient penalty**.
- Enforces the **Lipschitz constraint** without weight clipping for better convergence.

## 📌 Architecture Comparison

| Model    | Key Technique                 | Advantage                                      |
|----------|-------------------------------|------------------------------------------------|
| LS-GAN   | Least-squares loss            | Stabilized training, better gradients          |
| WGAN     | Wasserstein distance          | Reduced mode collapse, better convergence      |
| WGAN-GP  | Gradient penalty               | Smooth training, avoids weight clipping        |

## 📊 Evaluation Metrics

- **Inception Score (IS):** Measures diversity and clarity of generated images.
- **Fréchet Inception Distance (FID):** Assesses similarity between real and synthetic data.
- **Visual Inspection:** Manual review to ensure medical plausibility.

## 📁 Project Structure
- GAN Models: Different architectures for image generation.
- Evaluation Methods: Implementation of IS and FID scores for quantitative assessment.
- TensorBoard Logging: Visualization of training progress and image generation.

## 🛠️ Prerequisites

Make sure the following libraries are installed: 
PyTorch, Torchvision, MedMNIST, and TensorBoard

## 🛠️ Getting Started
- Train each GAN model individually.
- Compute IS and FID for evaluation.
- Visually review the output images.

## Contributions
Contributions are encouraged! You’re welcome to enhance evaluation techniques or introduce new GAN models.

## License
This project is distributed under the MIT License and is open for public use and modification.

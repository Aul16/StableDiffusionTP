# Stable Diffusion Lab

## Overview

This repository contains materials for a practical lab on Stable Diffusion models, focusing on implementing a simplified version that works with the MNIST dataset. Stable Diffusion is a powerful generative AI technique used for creating high-quality images from text prompts or transforming existing images.

## Prerequisites

- Understanding of U-Net architecture
- Access to GPU computing resources (Google Colab or local GPU)
- Knowledge of Transformers (optional but recommended)
- Basic understanding of PyTorch

## Repository Contents

- `TP_Stable_Diffusion_MNIST.ipynb`: Main lab notebook with implementation instructions
- `TP_Stable_Diffusion_MNIST Correction.ipynb`: Solution notebook for self-correction
- `model.ckpt`: Pre-trained model checkpoint
- Various PNG files: Example images and architectural diagrams

## Lab Objectives

In this lab, you will:

1. Understand the fundamental principles of diffusion models
2. Implement a simplified Stable Diffusion model
3. Train the model on the MNIST dataset
4. Generate new digit images using the trained model
5. Explore the diffusion process step by step

## Theoretical Background

Stable Diffusion works by gradually adding noise to an image and then training a neural network to reverse this process. The model consists of two main components:

- A noise generator that adds Gaussian noise to images
- A U-Net that predicts and removes noise from images

The training process involves:

1. Taking an image at noise step t_i
2. Denoising it to obtain the image at step t\_(i-1)
3. Comparing with the actual image at t\_(i-1) to calculate error
4. Repeating this process at different noise levels and with different images

## Implementation Details

The lab guides you through implementing:

- The U-Net architecture with residual and attention layers
- The diffusion process (forward and reverse)
- Training procedures
- Sampling methods for generating new images

## Getting Started

1. Open the `TP_Stable_Diffusion_MNIST.ipynb` notebook in Google Colab or a Jupyter environment with GPU access
2. Follow the step-by-step instructions to implement and train the model
3. If you encounter difficulties, refer to the correction notebook

## Notes

- This is a simplified implementation focused on MNIST for educational purposes
- For more complex image generation (like the examples shown in the notebook), more computational resources would be required
- The lab is designed to be accessible while still covering the core concepts of diffusion models

## References

- [DDPM Paper](https://arxiv.org/pdf/2006.11239) - Original Denoising Diffusion Probabilistic Models paper
- Additional resources are referenced throughout the notebook

# Generative Pathways

A study of probability paths in modern generative modeling, focusing on Neural ODEs, diffusion models, and flow matching.

## Overview

This project explores how modern generative models transform a simple prior distribution into a complex data distribution. The main focus is on comparing Diffusion Models and Flow Matching from the perspective of probability paths, sample trajectories, and sampling efficiency.

## Main Research Question

How do Diffusion Models and Flow Matching differ in their probability paths from a prior distribution to a data distribution, and how does this difference affect sampling efficiency and sample trajectories?

## Scope

This project covers:

- Generative modeling as distribution transformation
- Neural ODEs and Continuous Normalizing Flows
- Diffusion Models as iterative denoising processes
- Flow Matching as velocity field learning
- 2D toy experiments with probability path visualization
- NFE-based sampling efficiency analysis

## Project Structure

```text
Generative-Pathways/
├── README.md
├── requirements.txt
├── notes/
├── src/
├── notebooks/
├── results/
│   ├── figures/
│   └── tables/
├── blog/
└── report/
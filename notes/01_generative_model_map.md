# Generative Model Map

## Core Perspective

Generative modeling can be viewed as the problem of transforming a simple prior distribution into a complex data distribution.

\[
z \sim p_0(z) \quad \longrightarrow \quad x \sim p_{\text{data}}(x)
\]

Different generative models define this transformation in different ways.

## Model Comparison

| Model | Main Idea | Density / Likelihood | Sampling | Role in This Project |
|---|---|---|---|---|
| VAE | Latent variable modeling with ELBO | Approximate likelihood via ELBO | Decoder sampling | Background |
| GAN | Adversarial implicit generation | Not explicit | Generator mapping | Background |
| Normalizing Flow | Invertible transformation | Exact likelihood via change of variables | Invertible mapping | Bridge to CNF |
| CNF | ODE-based continuous transformation | Likelihood via instantaneous change of variables | ODE integration | Bridge to Flow Matching |
| Diffusion Model | Iterative denoising from noise | Variational / score-based view | Many reverse steps | Main comparison target |
| Flow Matching | Velocity field along probability path | CNF-compatible view | ODE integration | Main focus |

## Key Insight

VAE and GAN are important historical and conceptual baselines, but this project focuses on the continuous-time perspective. In this view, Diffusion Models and Flow Matching can both be interpreted as methods for moving samples from a simple prior distribution toward the data distribution.

The central comparison is therefore not only sample quality, but also the probability path, sample trajectory, and sampling cost.

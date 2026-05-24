# Classical Generative Models: VAE and GAN

## Purpose of This Note

This note briefly summarizes VAE and GAN as background paradigms in deep generative modeling. They are not the main focus of this project, but they provide context for understanding the transition toward diffusion models and flow-based generative models.

## VAE

VAE is a latent variable generative model. It assumes that observed data \(x\) is generated from a latent variable \(z\).

The marginal likelihood is generally difficult to compute directly:

\[
p_\theta(x) = \int p_\theta(x|z)p(z)dz
\]

Therefore, VAE maximizes the Evidence Lower Bound, ELBO, instead of directly maximizing the exact log-likelihood.

Key points:

- Latent variable model
- Optimizes ELBO
- Provides probabilistic interpretation
- Uses approximate posterior inference
- Limitation: posterior approximation and reconstruction quality trade-off

## GAN

GAN is an implicit generative model. It learns a generator \(G_\theta(z)\) that maps a latent sample \(z\) to a generated sample.

\[
z \sim p(z), \quad x = G_\theta(z)
\]

Instead of explicitly modeling likelihood, GAN trains the generator through adversarial learning with a discriminator.

Key points:

- Implicit generative model
- Uses adversarial training
- Does not provide explicit likelihood
- Often produces high-quality samples
- Limitation: training instability and mode collapse

## Role in This Project

VAE and GAN are treated as background models in this project. The main focus is not to implement or deeply analyze VAE and GAN, but to understand how generative modeling evolved toward diffusion models and continuous-time flow-based models.

The core direction of this project is:

\[
\text{Normalizing Flow} \rightarrow \text{Neural ODE} \rightarrow \text{CNF} \rightarrow \text{Flow Matching}
\]

with Diffusion Models as the main comparison target for probability-path-based generation.
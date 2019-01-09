# Regularization-based methods
## Reweighting the ELBO: β-VAE
L β-VAE (θ, φ) = L VAE (θ, φ) + λ1 E p̂(x) [D KL (q φ (z|x) || p(z))].

## Mutual information of x and z: FactorVAE, β-TCVAE, InfoVAE

E p̂(x) [D KL (q φ (z|x) || p(z)] = I q φ (x; z) + D KL (q φ (z) || p(z))

## Independence between groups of latents: HSIC-VAE, HFVAE

# Preventing the latent code from being ignored: PixelGAN-AE and VIB

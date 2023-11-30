# Images processing

The aim of this repository is to get to know how images are being processed. It covers several topics, including:
- generating artificial images (using GAN and DDPM),
- and more...

## [Generative Adversarial Network (GAN)](generative-adversarial-network/ddpm-denoising.ipynb)
By employing a dataset consisting of pumpkin cakes, we train both a generator and a discriminator model. The primary objective of the generator is to generate high-quality pumpkin cakes, while the discriminator aims to distinguish between real and fake ones. In order to expedite the training process, the images are downscaled to a resolution of 32x32 pixels.

**Results (upscaled)**

![GAN](generative-adversarial-network/generated.png)


**GAN model structure**
![GAN](generative-adversarial-network/gan_diagram.svg)

## Denoising Diffusion Probabilistic Models (DDPM)
The objective of this laboratory is to educate the PyTorch model on the task of denoising images. For this purpose, we emulate an image as a vector with a shape of `(2,)`. Initially, the model undergoes training using the `bicycle.txt` dataset. Subsequently, we employ the trained model to generate a denoised bicycle image by removing the noise introduced through a normal distribution.

**Bike generated from noise**
![Denoising visualisation](denoising-diffusion-probabilistic-model/denoising.gif)

### Other
```
jupyter nbconvert --to webpdf --allow-chromium-download lab.ipynb
```
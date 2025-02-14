
# **Generate CT Images with CycleGAN**

<p align="center">
    <img src="https://static.vecteezy.com/system/resources/thumbnails/004/640/933/small_2x/cycle-arrow-illustration-on-white-background-creative-icon-vector.jpg" height=400 width=1000 alt="CycleGAN">
</p>

<small>Picture Source: <a href="https://static.vecteezy.com/">vecteezy</a></small>

## **Introduction**

CycleGAN, or Cycle-Consistent Generative Adversarial Network, is a sophisticated generative model specifically designed for unpaired image-to-image translation tasks. Unlike traditional approaches that require matched image pairs from two different domains—such as images of CT scans—CycleGAN is capable of generating high-quality images even when paired data is not available. This feature is especially useful in fields such as medical imaging, where obtaining paired data (e.g., intact images and their corresponding CT scans) is often difficult or impractical.

This repository implements **CycleGAN** for generating CT images from intact images, enabling unpaired image translation in domains like medical imaging where paired data is scarce. The model uses dual generators and discriminators to perform image transformations while preserving content and style integrity.

### **Keywords**:

-   CycleGAN
-   CT Image Generation
-   Image-to-Image Translation
-   Unpaired Data
-   Medical Imaging
-   Generative Adversarial Networks

<br>

## **Motivation**

The primary motivation behind CycleGAN is to address challenges related to unpaired data. In medical applications like CT imaging, finding paired datasets that correlate specific features between the source and target images (like an intact image and its corresponding CT scan) can be time-consuming, expensive, and sometimes unfeasible. CycleGAN allows for flexible image transformation even in the absence of such paired datasets, thus enabling a wide range of applications across different domains.

<br>

## **Methodology**

CycleGAN employs a dual-generative architecture consisting of two generators and two discriminators:

1. **Two Generators**:
   - **$G$**: Transforms images from domain X (e.g., intact images) to domain $Y$ (e.g., CT images).
   - **$F$**: Transforms images from domain $Y$ back to domain $X$.

2. **Two Discriminators**:
   - **$D_Y$**: Distinguishes between real images from domain Y and generated images from $G$.
   - **$D_X$**: Distinguishes between real images from domain X and generated images from $F$.

3. **Cycle Consistency Loss**:
   - Ensures that if you translate an image from $X$ to $Y$ and then back to $X$ (or vice versa), you should end up with the original image. This helps maintain content and style integrity during translation.

4. **Adversarial Loss**:
   - CycleGAN uses adversarial loss to encourage the generators to produce realistic images that can fool the discriminators.

## **Features**

- Transforms images between different domains without requiring paired data.
- Maintains content and style integrity through cycle consistency.
- Can be applied to various fields such as medical imaging, art, style transfer, and domain adaptation.
- Flexible and powerful framework for image manipulation tasks.

## **Results**


CycleGAN has been successfully applied to numerous tasks. For example, in **style transfer**, it can transform the style of an image while preserving its underlying content. In **image synthesis**, it generates images in a different domain, such as creating CT images from intact images. Additionally, CycleGAN is highly effective for **domain adaptation**, enabling models trained in one domain to work in another without the need for paired data.

<p align="center">
    <img src="https://media.tenor.com/JhHYrYgP_qgAAAAM/abdominal-ct-scan.gif" width=500  alt="tenor.com">
</p>

## **Usage**

To use CycleGAN for generating CT images, please download IPython Notebook to your device:

1. Clone this repository:
   ```bash
   !git clone https://github.com/x
   ```
   or
      ```bash
   git clone https://github.com/x
   ```



## **Reference**

CycleGAN was introduced by **[Sharon Zhou](https://scholar.google.co.uk/citations?user=Kn35TAQAAAAJ&hl=en)**. You can find the original research paper and more details in her Google Scholar page.

- Zhu, J.-Y., Park, T., Isola, P., & Efros, A. A. (2017). "Unpaired Image-to-Image Translation Using Cycle-Consistent Adversarial Networks". *IEEE International Conference on Computer Vision (ICCV)*.

For further reading, you can also check the official [CycleGAN GitHub repository](https://github.com/junyanz/CycleGAN).

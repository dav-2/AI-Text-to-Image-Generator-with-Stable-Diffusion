# Text-to-Image-Generator-Flask-App-Created-Using-the-Stable-Diffusion-Model


<h2>Diffusion Models</h2>

Diffusion models are a type of machine learning model that has gained significant attention in the field of generative modelling. These models are particularly notable for their ability to generate high-quality images.

<h4>Overview of Diffusion Models</h4>

Diffusion models, also known as score-based generative models or denoising diffusion probabilistic models (DDPMs), generate data by reversing a diffusion process. The key idea is to start with a simple distribution (like Gaussian noise) and progressively refine it into a complex data distribution (like images) through a series of denoising steps.

<h4>Forward Diffusion Process</h4>

The forward process involves gradually adding noise to the data in a sequence of steps. This process transforms the data into a noise distribution. Over many steps, this process ensures that the data becomes indistinguishable from Gaussian noise.

<h4>Reverse Diffusion Process</h4>

The reverse process aims to gradually remove the noise, reconstructing the data from the noisy version. This involves learning a denoising function that can predict the clean data from the noisy data at each step. 

<h4>Training the Model</h4>

Training a diffusion model involves optimising the parameters to minimise the difference between the predicted clean data and the actual clean data at each step.

<h4>Generation Process</h4>

Once trained, generating new data involves starting with a sample from the Gaussian noise distribution and iteratively applying the learned denoising steps. This gradually transforms the noise into a coherent sample from the data distribution.

<h4>Applications and Advantages</h4>

Diffusion models have been shown to generate high-quality images and are competitive with other generative models like GANs (Generative Adversarial Networks) and VAEs (Variational Autoencoders). They have several advantages:
- Stable Training: Unlike GANs, diffusion models do not suffer from mode collapse or instability during training.
- High-Quality Outputs: They can produce high-resolution and detailed images.


<h2>Latent Diffusion Models</h2>

Latent Diffusion Models (LDMs) are an extension of the basic diffusion models that operate in a latent space instead of directly in the pixel space. This can lead to more efficient and scalable generative modelling, particularly for high-dimensional data like images. Here's a detailed explanation of how Latent Diffusion Models work:

<h4>Overview of Latent Diffusion Models</h4>

Latent Diffusion Models leverage the idea of performing the diffusion process in a lower-dimensional latent space rather than in the original high-dimensional data space. This is achieved by using an autoencoder to encode the data into a latent representation and then applying the diffusion process within this latent space.

<h4>Components of Latent Diffusion Models</h4>

LDMs consist of three main components:
- Autoencoder (Encoder-Decoder Network): This network compresses the high-dimensional data (e.g., images) into a lower-dimensional latent space and then reconstructs the data from this latent representation. The autoencoder has two parts: 
    - Encoder: Compresses the high-dimensional data  into a latent representation.
    - Decoder: Reconstructs the data from the latent representation.
- Diffusion Process in Latent Space: The diffusion model operates on the latent representations, adding noise and learning to denoise these representations.
- Latent Variable Model: This model captures the distribution of the latent representations.


<h4>Forward Diffusion Process in Latent Space</h4>

Similar to standard diffusion models, the forward diffusion process involves adding noise to the latent representations over a sequence of steps.

<h4>Reverse Diffusion Process in Latent Space</h4>

The reverse diffusion process aims to denoise the latent representations.

<h4>Training the Latent Diffusion Model</h4>

Training involves optimising the parameters to minimise the difference between the true and predicted distributions in the latent space.

<h4>Generation Process</h4>

To generate new data, the process involves:
1. Sampling from the Gaussian noise distribution in the latent space.
2. Applying the learned denoising steps to obtain a latent representation.
3. Using the decoder to reconstruct the high-dimensional data from the latent representation.

<h4>Advantages of Latent Diffusion Models</h4>

- Efficiency: Operating in a lower-dimensional latent space reduces the computational complexity and memory requirements compared to working in the high-dimensional pixel space.
- Scalability: LDMs can handle higher resolutions and larger datasets more efficiently.
- Quality: By focusing the diffusion process on essential features in the latent space, LDMs can achieve high-quality generation with fewer steps.


<h2>Stable Diffusion Models</h2>

Stable Diffusion models are a type of Latent DIffusion models tuned to produce art. They are trained on LAION-5B; a large-scale dataset containing billions of image-text pairs.



<h1>Project</h1>

Created in Google Colab.

text_to_image_generator.ipynb is just the model working inside Colab.

text_to_image_generator_app.ipynb opens a small web app where the user interacts with the image generator.

Stable Diffusion Model version used: stable-diffusion-2-1. Even though the stable-diffusion-2-1 version was released in December 2022, it still offers a good balance beween precision, speed and resources counsumption. The main reason behind the decision to use this version was to optimise Google Colab resources. However, if a better image quality and/or prompt interpretation is needed, newer versions of the model can be used by changing the version in the code.

Google Colab runs in a cloud-based environment where each notebook is executed on a virtual machine. This VM is isolated from the internet for security and privacy reasons. Ngrok is a tool that creates secure tunnels to your localhost, allowing you to expose a local development server to the internet. When working in Google Colab, ngrok can be particularly useful for creating web applications or APIs that you want to test or share with others, as it creates tunnels that securely expose the services running inside these VMs to the internet. To use ngrok it is needed to create an account and use the authtoken provided in the account.

To open the app, click on the ngrok-free.app link in the output at the end of the program run in text_to_image_generator_app.ipynb.

<h2>Examples of images generated:</h2>

Prompt: white elephant in the water

![Screenshot 2024-07-23 at 17-32-07 (PNG Image 768 × 768 pixels)](https://github.com/user-attachments/assets/572e0baf-6bc4-48bc-a000-4dbf1d83ace0)


Prompt: stormy sea with an island

![Screenshot 2024-07-23 at 20-27-48 (PNG Image 768 × 768 pixels)](https://github.com/user-attachments/assets/4b823948-03b8-4ef7-908b-5cca301924a7)


Prompt: Edinburgh castle

![Screenshot 2024-07-23 at 20-29-11 (PNG Image 768 × 768 pixels)](https://github.com/user-attachments/assets/acfade24-ba58-4645-8122-de1b7d045adb)


Prompt: New York city

![Screenshot 2024-07-23 at 20-30-35 (PNG Image 768 × 768 pixels)](https://github.com/user-attachments/assets/ccfb679b-4f13-42f0-810a-8fe81c78bfd0)


Prompt: realistic image of New York

![Screenshot 2024-07-23 at 20-31-31 (PNG Image 768 × 768 pixels)](https://github.com/user-attachments/assets/a54cc6fa-6ec6-4617-b4b3-184fa05f1ebd)




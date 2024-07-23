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

<h2>Project</h2>

Created in Google Colab.

text_to_image_generator.ipynb is just the model working inside Colab.

text_to_image_generator_app.ipynb opens a small web app where the user interacts with the image generator.

Stable Diffusion Model version used: stable-diffusion-2-1. Even though the stable-diffusion-2-1 version was released in December 2022, it still offers a good balance beween precision, speed and resources counsumption. The main reason behind the decision to use this version was to optimise Google Colab resources. However, if a better image quality and/or prompt interpretation is needed, newer versions of the model can be used by changing the version in the code.

Google Colab runs in a cloud-based environment where each notebook is executed on a virtual machine. This VM is isolated from the internet for security and privacy reasons. Ngrok is a tool that creates secure tunnels to your localhost, allowing you to expose a local development server to the internet. When working in Google Colab, ngrok can be particularly useful for creating web applications or APIs that you want to test or share with others, as it creates tunnels that securely expose the services running inside these VMs to the internet. To use ngrok it is needed to create an account and use the authtoken provided in the account.

To open the app, click on the ngrok-free.app link in the output at the end of the program run in text_to_image_generator_app.ipynb.

Examples of images generated: 
  
![Screenshot 2024-07-23 at 17-32-07 (PNG Image 768 × 768 pixels)](https://github.com/user-attachments/assets/572e0baf-6bc4-48bc-a000-4dbf1d83ace0)

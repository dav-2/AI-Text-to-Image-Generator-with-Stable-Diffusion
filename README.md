# Text-to-Image-Generator-Flask-App-Created-Using-the-Stable-Diffusion-Model


Created in Google Colab.

text_to_image_generator.ipynb is just the model working inside Colab.

text_to_image_generator_app.ipynb opens a small web app where the user interacts with the image generator.

Stable Diffusion Model version used: stable-diffusion-2-1. Even though the stable-diffusion-2-1 version was released in December 2022, it still offers a good balance beween precision, speed and resources counsumption. The main reason behind the decision to use this version was to optimise Google Colab resources. However, if a better image quality and/or prompt interpretation is needed, newer versions of the model can be used by changing the version in the code.

Google Colab runs in a cloud-based environment where each notebook is executed on a virtual machine. This VM is isolated from the internet for security and privacy reasons. Ngrok is a tool that creates secure tunnels to your localhost, allowing you to expose a local development server to the internet. When working in Google Colab, ngrok can be particularly useful for creating web applications or APIs that you want to test or share with others, as it creates tunnels that securely expose the services running inside these VMs to the internet. To use ngrok it is needed to create an account and use the authtoken provided in the account.

To open the app, click on the ngrok-free.app link in the output at the end of the program run in text_to_image_generator_app.ipynb.

Examples of images generated: 
  
![Screenshot 2024-07-23 at 17-32-07 (PNG Image 768 × 768 pixels)](https://github.com/user-attachments/assets/572e0baf-6bc4-48bc-a000-4dbf1d83ace0)

# GAN Image and Video Generation

This repository contains code to generate images and videos using a pre-trained Generative Adversarial Network (GAN) model. The code allows you to generate a single image from random latent vectors and create a video by interpolating the latent space.

## Requirements

- TensorFlow 1.x
- NumPy
- OpenCV

## Setup

First, clone the repository and navigate to the project directory:

```bash
git clone https://github.com/yourusername/gan-image-video-generation.git
cd gan-image-video-generation
Install Dependencies
Make sure you have the required libraries installed:

bash
Copy code
pip install tensorflow==1.15.0
pip install numpy
pip install opencv-python

## See Releases for datasets or use "links to datasets.txt" to access them via google drive

Model Checkpoint
Ensure you have the pre-trained GAN model checkpoint files saved in the ./models/ directory:

model.ckpt.meta
model.ckpt.index
model.ckpt.data-00000-of-00001
Generating a Single Image
To generate a single image from the latent space, use the main_generate_image function. Update the parameters as needed and run the script.

Parameters
input_image_path: Path to the input image (not used for image generation but required for the function).
output_image_path: Path to save the generated image.
checkpoint_path: Path to the model checkpoint.
image_size: Size of the generated image.
latent_dim: Dimension of the latent space.

generate_image.py
The script will generate a single image and save it to the specified output path.

Generating a Video
To generate a video using the GAN model, use the main_generate_video function. Update the parameters as needed and run the script.

Parameters
input_image_path: Path to the input image to preprocess.
checkpoint_path: Path to the model checkpoint.
video_output_path: Path to save the generated video.
image_size: Size of the generated images.
latent_dim: Dimension of the latent space.
num_frames: Number of frames to generate for the video.
fps: Frames per second for the generated video.

python generate_video.py

The script will preprocess the input image, generate frames from the latent space, and save the video to the specified output path.


Notes
Ensure the tensor names like 'generator_499/out:0' and 'input_z:0' match your actual model's tensor names.
Verify that your model checkpoint path is correct.
Adjust parameters like image_size and latent_dim according to your model's requirements.
License
This project is licensed under the MIT License.

# Image Generator Project

This project explores how to generate high-quality images from text prompts using **Stable Diffusion 2** and the **Hugging Face Diffusers** library in Google Colab.  
It was developed as a project to understand how large text-to-image models work and how parameters such as guidance scale, seed, and inference steps influence the final output.

## Project Overview
The notebook loads the *stabilityai/stable-diffusion-2* model through the `diffusers` pipeline and generates images entirely on Google Colab using GPU acceleration.  
Each prompt is processed in several diffusion steps to progressively refine noise into a coherent image.

Example prompts used in this project:
- “Coffee with pen and laptop at side”  
- “Painting exhibition background”  
- “Children playing football in the ground in colorful background”  
- “Realistic astronaut floating in space, detailed suit, Earth in the background”


## Model Configuration
| Parameter | Value | Description |
|------------|--------|-------------|
| `image_gen_model_id` | `stabilityai/stable-diffusion-2` | Pre-trained diffusion model |
| `image_gen_steps` | 35 | Number of inference steps per image |
| `image_gen_guidance_scale` | 9 | Controls prompt adherence vs. creativity |
| `image_gen_size` | (700, 600) | Output image resolution |
| `seed` | 42 | Ensures reproducible results |
| `device` | `"cuda"` | Enables GPU execution in Colab |

---

## How to Run

1. **Open in Google Colab**  
   👉 [Run the Notebook](https://colab.research.google.com/github/Purva2405/Image-Generator/blob/main/Clean_Image_Generator_Project.ipynb)

2. **Enable GPU**  
   Go to `Runtime → Change runtime type → Hardware accelerator → GPU`.

3. **Install dependencies**
   ```python
   !pip install --upgrade diffusers transformers

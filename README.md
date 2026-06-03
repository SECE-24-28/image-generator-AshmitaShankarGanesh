[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/qT3Kmf07)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24069072&assignment_repo_type=AssignmentRepo)
**# AI Image Generator using Stable Diffusion

## Overview

This project is a simple AI-powered image generator built using the Stable Diffusion model from the Diffusers library. Users can enter a text prompt, and the application generates a corresponding image using a pre-trained diffusion model.

The generated images are automatically saved in a dedicated `result` folder with unique timestamps.

---

## Features

* Generate images from text prompts
* Uses Stable Diffusion v1.5
* Automatic CPU/GPU detection
* Saves generated images with unique filenames
* Organized output storage
* Simple command-line interface

---

## Technologies Used

* Python
* PyTorch
* Diffusers
* Transformers
* Stable Diffusion v1.5
* Hugging Face Hub

---

## Project Structure

```
image-generator/
│
├── main.py
├── result/
│   ├── generated_20260603_101530.png
│   ├── generated_20260603_102145.png
│   └── ...
│
├── README.md
└── pyproject.toml
```

---

## Installation

### 1. Clone the Repository

```bash
git clone <repository-url>
cd image-generator
```

### 2. Create Virtual Environment

```bash
python -m venv .venv
```

Activate the environment:

Windows:

```bash
.venv\Scripts\activate
```

Linux/Mac:

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

Using uv:

```bash
uv add diffusers transformers torch accelerate safetensors pillow
```

or using pip:

```bash
pip install diffusers transformers torch accelerate safetensors pillow
```

---

## How to Run

Execute the application:

```bash
uv run main.py
```

or

```bash
python main.py
```

Enter a text prompt when requested:

```text
Enter image description: A futuristic city at sunset with flying cars
```

The model will generate an image and save it inside the `result` folder.

---

## Example

Input Prompt:

```text
A majestic tiger sitting on a mountain during sunrise
```

Output:

```text
Using device: cuda
Generating image... Please wait...
Image saved successfully!
Location: result/generated_20260603_104512.png
```

---

## Working Principle

The project uses a pre-trained Stable Diffusion model.

### Steps:

1. Load the Stable Diffusion v1.5 model.
2. Detect available hardware (GPU or CPU).
3. Accept a text prompt from the user.
4. Convert the prompt into latent representations.
5. Generate an image through the diffusion process.
6. Save the generated image with a timestamp.

---

## Requirements

* Python 3.10+
* Internet connection (first run only)
* Minimum 8 GB RAM recommended
* NVIDIA GPU recommended for faster generation

---

## Future Enhancements

* Streamlit Web Interface
* Gradio Interface
* Multiple image generation
* Image size customization
* Negative prompts
* Prompt history
* Download and share options
* Fine-tuned custom models

---

## Author

Ashmita S

Computer Science and Business Systems (CSBS)

AI & Machine Learning Enthusiast

---

## License

This project is intended for educational and learning purposes.
**

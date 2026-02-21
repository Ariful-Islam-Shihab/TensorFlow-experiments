# TensorFlow + Keras Bootcamp Notebooks (OpenCV University)

This repository contains my hands-on Jupyter notebooks from the **free TensorFlow/Keras course (bootcamp)** by OpenCV University:

- Course page: https://opencv.org/university/free-tensorflow-keras-course/

The notebooks are organized by topic (classification, transfer learning, fine-tuning, segmentation, and object detection). They’re meant for learning and experimentation.

## What’s inside

| Notebook | Topic | What you’ll do |
|---|---|---|
| `MNIST.ipynb` | Image classification | Train a simple neural network/CNN on the MNIST digits dataset. |
| `CIFAR-10.ipynb` | Image classification | Build and train a CNN on CIFAR-10 (harder, color images). |
| `Pre_trained_model.ipynb` | Transfer learning | Use a pretrained backbone and train a new classification head. |
| `Fine_tuning_a_model.ipynb` | Fine-tuning | Unfreeze layers and fine-tune a pretrained model end-to-end. |
| `Image_segmentation.ipynb` | Segmentation | Train/evaluate a segmentation model and visualize masks. |
| `Object_detection.ipynb` | Detection | Run/experiment with an object detection pipeline/model. |

## Requirements

- **Recommended**: Google Colab (runs in the browser, no local install required)
- **Optional (local)**: Python 3.10–3.12 + Jupyter/JupyterLab
- **Compute**: CPU is fine for learning; a GPU can speed things up.

## Run in Google Colab (recommended)

1. Upload/open this repo in GitHub (or download the `.ipynb` files).
2. Open Colab: https://colab.research.google.com/
3. In Colab:
  - **File → Open notebook**
  - Choose **GitHub** (if the repo is on GitHub) or **Upload** (if you downloaded the notebook)
4. (Optional) Enable GPU: **Runtime → Change runtime type → Hardware accelerator → GPU**
5. Run cells top-to-bottom.

Notes:
- Some notebooks may install extra packages in the first cells (common in Colab). If you see `pip install ...`, run that cell and then re-run imports.
- If you’re using a GitHub repo link, Colab will open notebooks read-only by default; use **File → Save a copy in Drive** to edit.

## Local setup (Windows, optional)

From the repo folder:

```powershell
# Create and activate a virtual environment
py -m venv .venv
.\.venv\Scripts\Activate.ps1

# Upgrade pip
python -m pip install -U pip
```

Install common dependencies:

```powershell
python -m pip install jupyter numpy matplotlib

# TensorFlow (CPU)
python -m pip install tensorflow

# Optional (often useful in vision notebooks)
python -m pip install opencv-python pillow
```

Notes:
- If you specifically want GPU acceleration on Windows, your easiest path is often **WSL2 + NVIDIA CUDA**. TensorFlow’s native Windows GPU support has changed over time—use the official TensorFlow install guide for your setup.

## Run the notebooks

If you’re using Colab, follow the steps in **Run in Google Colab (recommended)**.

For local execution:

```powershell
jupyter lab
```

Then open any of the `.ipynb` files and run cells top-to-bottom.

## Data & downloads

Many tutorial-style notebooks download datasets automatically (e.g., MNIST, CIFAR-10). If a notebook asks you to download something manually, follow the instructions inside that notebook.

If you’re behind a proxy or have restricted network access, you may need to:
- pre-download datasets,
- set environment variables for proxies, or
- run once on an unrestricted network to populate the local cache.

## Troubleshooting

- **Kernel can’t import TensorFlow**: verify you launched Jupyter from the same environment where you installed packages.
  - Quick check inside a notebook:
    ```python
    import sys
    print(sys.executable)
    ```
- **Slow training**: reduce epochs, use a smaller model, or switch to GPU.
- **Out of memory**: reduce batch size or image resolution.

## Attribution

- Course reference: OpenCV University — Free TensorFlow/Keras course
  - https://opencv.org/university/free-tensorflow-keras-course/

This repo is a learner project and is **not affiliated with or endorsed by OpenCV**.

## License

No license is provided by default. If you plan to share or reuse this code publicly, consider adding a license file (e.g., MIT) and ensure you have rights to any included datasets or assets.

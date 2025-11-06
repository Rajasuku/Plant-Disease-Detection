# Plant Disease Detection

**Repository:** `Rajasuku/Plant-Disease-Detection`

> A compact project for detecting plant leaf diseases using deep learning. This repository contains Jupyter notebooks for training and testing, a `main.py` script for quick inference/utility, a `requirements.txt` listing dependencies, and example images.

---

## Table of Contents

* [About](#about)
* [Features](#features)
* [Repository structure](#repository-structure)
* [Dataset](#dataset)
* [Requirements](#requirements)
* [Installation](#installation)
* [Usage](#usage)

  * [Running the notebooks](#running-the-notebooks)
  * [Using `main.py` for inference](#using-mainpy-for-inference)
* [Training](#training)
* [Evaluation & Results](#evaluation--results)
* [Model & Implementation Notes](#model--implementation-notes)
* [How to contribute](#how-to-contribute)
* [License](#license)
* [Contact](#contact)

---

## About

This project demonstrates an end-to-end workflow to build a plant leaf disease classifier. It includes data preparation, model training and evaluation, and simple inference. The notebooks show exploratory steps and training experiments.

## Features

* Jupyter notebooks for training and testing models
* `main.py` for quick inference or demo usage
* `requirements.txt` with Python package dependencies
* Example image `Diseases.png` (visual aid)

## Repository structure

```
Plant-Disease-Detection/
├─ Train_plant_disease.ipynb
├─ Train_plant_disease-checkpoint.ipynb
├─ Test_plant_disease.ipynb
├─ Test_plant_disease-checkpoint.ipynb
├─ main.py
├─ requirements.txt
├─ settings.json
├─ Diseases.png
└─ README.md    # <- you are reading this
```

> *Note:* The exact structure in your fork/clone may add folders like `data/`, `models/` or `notebooks/` as you expand the project.

## Dataset

This repository does not include a large dataset. For experiments you can use one of the commonly used public datasets such as:

* **PlantVillage** (public dataset of healthy and diseased plant leaf images) — recommended for prototyping.

Place your images in a folder structure like:

```
data/
  ├─ train/
  │   ├─ Tomato___Late_blight/
  │   ├─ Tomato___Early_blight/
  │   └─ ...
  └─ test/
      ├─ Tomato___Late_blight/
      └─ ...
```

Or update the dataset paths used in the notebooks or `settings.json` accordingly.

## Requirements

A `requirements.txt` is provided. Typical packages used in this kind of project include:

* Python 3.8+
* numpy
* pandas
* matplotlib
* scikit-learn
* pillow
* tensorflow or torch (depending on model used in notebooks)
* jupyter

Install the exact dependencies with:

```bash
pip install -r requirements.txt
```

If you plan to use GPU acceleration, install the appropriate TensorFlow/PyTorch builds compatible with your CUDA version.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/Rajasuku/Plant-Disease-Detection.git
cd Plant-Disease-Detection
```

2. (Optional) Create a virtual environment:

```bash
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate     # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Running the notebooks

Open the notebooks in JupyterLab / Jupyter Notebook:

```bash
jupyter notebook
# or
jupyter lab
```

Open `Train_plant_disease.ipynb` to inspect preprocessing, model architecture and training steps. Use `Test_plant_disease.ipynb` for running inference on test images and visualizing predictions.

### Using `main.py` for inference

`main.py` is included for quick demo/inference or utility tasks. Typical usage (adjust command-line options if the script supports them):

```bash
python main.py --image path/to/leaf.jpg
```

> If `main.py` parses arguments or expects a settings file (`settings.json` exists), update those files with correct paths and model checkpoint names before running.

## Training

1. Prepare the dataset directory as described above.
2. Open `Train_plant_disease.ipynb` (or the checkpoint notebook) and follow the cells: data loading → augmentation → model construction → compile → fit.
3. Save model weights/checkpoints to a `models/` directory.

Tips:

* Start with a smaller subset to iterate quickly.
* Use transfer learning (MobileNet, EfficientNet, ResNet) for faster convergence.
* Monitor training/validation loss and accuracy to avoid overfitting.

## Evaluation & Results

The notebooks include code to compute accuracy, recall, precision, F1-score, and confusion matrix. Add your final numbers and, if available, sample output images and the model checkpoint details here.

**Example (fill with your results):**

* Model: `EfficientNetB0` (transfer learning)
* Test accuracy: `XX.XX%`
* Macro F1-score: `XX.XX`

## Model & Implementation Notes

* Check the notebooks for the model architecture used (likely in the training notebooks).
* If you prefer PyTorch or TensorFlow, convert/modify the model cells accordingly.
* Save preprocessing pipelines (image resizing, normalization) and reuse the same for inference.

## How to contribute

1. Fork the repository
2. Create a branch: `git checkout -b feature/my-feature`
3. Make changes, add tests or a short description of experiments
4. Commit and push: `git push origin feature/my-feature`
5. Open a pull request describing your changes

Please follow standard best practices for commits and documentation.

## License

Add a license file if you want to open-source this project. If you prefer a permissive license, consider `MIT`.

```
MIT License
```

(Replace or add a `LICENSE` file at the repository root.)

## Contact

If you have questions or want to collaborate, open an issue or contact the repository owner.

---

### Next steps / To-do (suggested)

* Add an explicit `README.md` to the repository root (this file).
* Add example `models/` and `data/` with a tiny sample so newcomers can run the project end-to-end quickly.
* Add CLI usage examples in `main.py` and a `scripts/` folder for common tasks (train/eval/infer).
* Add unit tests for data loaders and the inference pipeline.

---

*Generated README — please review and tell me if you'd like specific wording, added badges (build/coverage), or to include your exact training results and model checkpoints.*

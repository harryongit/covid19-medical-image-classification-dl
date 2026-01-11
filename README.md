# COVID-19 Medical Image Classification ✅

**A lightweight project for classifying chest X-Ray / CT images to detect COVID-19**.

---

## 🔎 Overview
This repository contains code and model artifacts used for training and evaluating a COVID-19 medical image classification model (a Hybrid CNN + Transformer architecture). The dataset used is the COVID-19 Radiography Database on Kaggle.

Dataset: https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database

---

## 📁 Project structure

- `deeplearning.py` — Main script to train / evaluate the model
- `notebooks/deeplearning.ipynb` — Notebook with experiments and visualization
- `models/Hybrid_CNN_Transformer_COVID19.h5` — Example trained model
- `results/` — Evaluation outputs and plots
- `requirements.txt` — Python dependencies to install

---

## ⚙️ Requirements
Create a virtual environment and install dependencies:

```bash
python -m venv venv
venv\Scripts\activate    # Windows
pip install -r requirements.txt
```

> Note: GPU support requires a tensorflow build compatible with your CUDA/cuDNN versions. Install `tensorflow` or `tensorflow-gpu` accordingly.

---

## 📥 Downloading the dataset
You can download the dataset manually from the Kaggle link above, or use the Kaggle CLI:

1. Install the Kaggle package (already included in `requirements.txt`):
```bash
pip install kaggle
```
2. Place your `kaggle.json` in `%USERPROFILE%\.kaggle\kaggle.json` (Windows) or `~/.kaggle/kaggle.json` (Linux/Mac).
3. Download and unzip the dataset:

```bash
kaggle datasets download -d tawsifurrahman/covid19-radiography-database -p data --unzip
```

Make sure the extracted folder structure matches the paths expected by `deeplearning.py` or update the script accordingly.

---

## 🚀 Usage

- To run training or evaluation from the script:

```bash
python deeplearning.py --train --data_dir data/COVID-19_Radiography_Dataset
```

- Or, open and run cells in `notebooks/deeplearning.ipynb` to reproduce experiments and visualize results.

(Adjust command-line arguments and paths according to how `deeplearning.py` is implemented.)

---

## 🧪 Reproducing results
- Ensure dataset is in place and `requirements.txt` is installed.
- Use the notebook for step-by-step experiments or the script for full runs.
- Trained models are saved to `models/` by default.

---

## 📝 Notes & Tips
- Preprocessing and augmentation are crucial for medical image tasks; check the notebook to see what transforms were used.
- If you run into memory/GPU issues, reduce batch size or use mixed-precision training (TensorFlow recommended settings).

---

## 📄 License
Add your preferred license here (e.g., MIT) or state any restrictions.

---

## ❤️ Contributing
Contributions, bug reports, and improvements are welcome — please open issues or pull requests.

---

If you'd like, I can also add a simple example command for evaluation or implement a sample `--help` in `deeplearning.py` to document available options. 🔧

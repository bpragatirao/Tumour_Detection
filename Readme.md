# Brain Tumour Detection: Classification vs Segmentation

A beginner-friendly deep learning project to understand the fundamental difference between **Image Classification** and **Image Segmentation** using Brain MRI images.

This project was intentionally designed with a **very small dataset** so the concepts can be easily visualized, understood, and experimented with using Jupyter Notebook.

---

# Project Objective

The main goal of this project is to compare:

| Task | Goal |
|---|---|
| Classification | Predict whether a tumour exists or not |
| Segmentation | Identify the exact tumour region pixel-by-pixel |

Using the same medical imaging domain helps clearly understand:
- how outputs differ,
- how models differ,
- and how computer vision tasks evolve from simple to advanced.

---

# Understanding the Difference

## 1. Classification

### Input:
Brain MRI Image

### Output:
```text
Tumour / No Tumour
```

The model predicts:
> “Does this MRI contain a tumour?”

### Model Used:
Simple CNN (Convolutional Neural Network)

### Output Example:
```text
MRI Image → Tumour Present
```

---

## 2. Segmentation

### Input:
Brain MRI Image

### Output:
```text
Tumour Mask
```

The model predicts:
> “Where exactly is the tumour located?”

### Model Used:
U-Net Architecture

### Output Example:
```text
MRI Image → Highlighted Tumour Region
```

---

# Why This Project?

Medical imaging is one of the most important real-world applications of AI.

This project helps understand:
- Computer Vision basics
- CNNs
- U-Net
- Image preprocessing
- Pixel-level prediction
- Medical image analysis
- Visualization of AI outputs

without needing:
- huge datasets,
- GPUs,
- or complex pipelines.

---

# Dataset Used

## Classification Dataset
Brain MRI Images for Brain Tumor Detection

Source:
https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection

Used Classes:
- Yes (Tumour)
- No (No Tumour)

Only a very small subset (~40 images) was used for learning purposes.

---

## Segmentation Dataset
LGG MRI Segmentation Dataset

Source:
https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation

Used Data:
- MRI images
- Corresponding tumour masks

Only ~20 image-mask pairs were used to simplify visualization and training.

---

# Project Structure

```text
tumour_project/
│
├── data/
│   ├── classification/
│   │   ├── yes/
│   │   └── no/
│   │
│   └── segmentation/
│       ├── images/
│       └── masks/
│
├── notebooks/
│   ├── 01_classification.ipynb
│   └── 02_segmentation.ipynb
│
├── src/
│   ├── classification_model.py
│   ├── segmentation_model.py
│   ├── utils.py
│   └── visualize.py
│
├── models/
│
├── requirements.txt
└── README.md
```

---

# Workflow Overview

## Classification Workflow

```text
MRI Image
   ↓
Preprocessing
   ↓
CNN Model
   ↓
Tumour / No Tumour
```

---

## Segmentation Workflow

```text
MRI Image
   ↓
Preprocessing
   ↓
U-Net Model
   ↓
Tumour Mask Prediction
```

---

# Key Learning Outcomes

After completing this project, the following concepts become clear:

| Concept | Classification | Segmentation |
|---|---|---|
| Output Type | Single Label | Pixel Mask |
| Prediction Level | Image Level | Pixel Level |
| Architecture | CNN | U-Net |
| Goal | Detect Tumour | Locate Tumour |
| Complexity | Easier | More Advanced |
| Visualization | Class Label | Predicted Mask |

---

# Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

# Model Architectures

## Classification Model
A simple CNN with:
- Convolution layers
- MaxPooling
- Dense layers
- Sigmoid output

Used for binary classification.

---

## Segmentation Model
A simplified U-Net architecture with:
- Encoder
- Bottleneck
- Decoder
- Pixel-wise sigmoid output

Used for tumour mask prediction.

---

# Visualizations Included

## Classification
- Sample MRI images
- Predicted labels
- Accuracy graphs

## Segmentation
- MRI image
- Ground truth mask
- Predicted tumour mask

These visualizations help understand:
- how the model learns,
- what the model predicts,
- and the practical difference between both tasks.

---

# Running the Project

## 1. Create Virtual Environment

```bash
python -m venv venv
```

Activate environment:

### Mac/Linux
```bash
source venv/bin/activate
```

### Windows
```bash
venv\Scripts\activate
```

---

## 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:
- `01_classification.ipynb`
- `02_segmentation.ipynb`

---

# Future Improvements

Possible extensions:
- Transfer Learning
- Attention U-Net
- Dice Loss
- IoU Metric
- Data Augmentation
- Multi-class tumour segmentation
- 3D MRI segmentation

---

# Final Takeaway

This project demonstrates the evolution from:

```text
“Does a tumour exist?”
```

to

```text
“Where exactly is the tumour?”
```

which represents the core difference between:
- Image Classification
- Image Segmentation

in Deep Learning and Medical AI.

# 🪙 Coin Classifier using OpenCV & Deep Learning

An end-to-end computer vision project that detects Indian coins from an image and classifies each coin into its denomination using a Convolutional Neural Network (CNN).

## Features

- Detects multiple coins in a single image
- Crops each detected coin automatically
- Removes the background using a circular mask
- Classifies each coin using a trained CNN
- Displays prediction confidence for every detected coin
- Supports visualization of detected coins and predictions

---

## Demo

### Input Image

(Add an image here)

### Coin Detection

(Add screenshot)

### Predictions

(Add screenshot showing confidence graphs)

---

## Project Pipeline

1. Read input image
2. Detect coins using Hough Circle Transform
3. Crop each detected coin
4. Apply black circular background
5. Resize image for the CNN
6. Predict denomination
7. Display confidence scores

```

```
Input Image
      │
      ▼
Detect Coins (OpenCV)
      │
      ▼
Crop Coins
      │
      ▼
Black Background
      │
      ▼
Resize (256×256)
      │
      ▼
CNN Model
      │
      ▼
Predicted Coin + Confidence
```

```markdown
---

## Tech Stack

- Python
- OpenCV
- TensorFlow / Keras
- NumPy
- Matplotlib
- Google Colab

---

## Dataset

The dataset consists of Indian coin images belonging to multiple denominations.

Classes:
- ₹1
- ₹2
- ₹5
- ₹10

Images were preprocessed before training by:
- Detecting the coin
- Cropping
- Applying a black background
- Resizing to 256×256 pixels

---

## Model

Architecture:
- Convolutional Neural Network (CNN)

Loss Function:
- Categorical Crossentropy

Optimizer:
- Adam

Evaluation Metric:
- Accuracy

---

## Results

| Metric | Value |
|---------|--------|
| Training Accuracy | XX% |
| Validation Accuracy | XX% |
| Test Accuracy | XX% |

---

## Folder Structure

```

Coin-Classifier/
│
├── Dataset/
├── Model/
├── Notebooks/
├── Results/
├── README.md
└── requirements.txt

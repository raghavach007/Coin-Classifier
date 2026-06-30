# Indian Coin Classifier using OpenCV + EfficientNetB0

An AI-powered Indian coin recognition system that detects multiple scattered coins from an image and classifies them into their respective denominations using **Computer Vision** and **Deep Learning**.

---

## Features

- Detects multiple coins from a single image
- Works on scattered coins placed on a plain background
- Classifies coins into:
  - ₹1
  - ₹2
  - ₹5
  - ₹10
- Displays prediction confidence for every detected coin
- Calculates the total monetary value automatically
- Uses OpenCV for coin detection
- Uses EfficientNetB0 Transfer Learning for classification

---

## Technologies Used

- Python
- OpenCV
- TensorFlow / Keras
- EfficientNetB0
- NumPy
- Matplotlib
- Google Colab

---

## Project Structure

```
Coin-Classifier/
│
├── dataset/
│   ├── 1_rupee/
│   ├── 2_rupee/
│   ├── 5_rupee/
│   └── 10_rupee/
│
├── model/
│   └── best_coin_model.keras
│
├── notebooks/
│   └── Coin_Classifier.ipynb
│
├── images/
│   ├── sample1.jpg
│   ├── sample2.jpg
│   └── sample3.jpg
│
├── README.md
└── requirements.txt
```

---

# Dataset

The model was trained using a custom dataset consisting of cropped Indian coin images.

| Coin | Images |
|------|--------|
| ₹1 | 500+ |
| ₹2 | 500+ |
| ₹5 | 500+ |
| ₹10 | 300+ |

Dataset includes:

- Different lighting conditions
- Different orientations
- Multiple years of minting
- Various coin designs
- White background images

---

# Model Architecture

Transfer Learning using **EfficientNetB0**

```
Input Image
      │
EfficientNetB0
      │
Global Average Pooling
      │
Dense Layer (4 Classes)
      │
Softmax
```

Only the classification head is trained while EfficientNetB0 is used as a pretrained feature extractor.

---

# Coin Detection Pipeline

1. Read Image
2. Convert to Grayscale
3. Gaussian Blur
4. Hough Circle Transform
5. Detect Coin Centers
6. Crop Individual Coins
7. Remove Background
8. Add White/Black Background
9. Resize to 256×256
10. Pass to EfficientNet Model
11. Display Prediction
12. Calculate Total Value

---

# Sample Output

```
Detected Coins: 3

Coin 1
Prediction: ₹5
Confidence: 98.4%

Coin 2
Prediction: ₹1
Confidence: 95.7%

Coin 3
Prediction: ₹2
Confidence: 97.8%

--------------------
Total Value = ₹8
```

---

# Training

The classifier was trained using:

- EfficientNetB0 (ImageNet Weights)
- Adam Optimizer
- Sparse Categorical Crossentropy
- EarlyStopping
- ReduceLROnPlateau
- ModelCheckpoint

Image Size:

```
256 × 256
```

Epochs:

```
15 + Fine Tuning
```

---

# Results

Training Accuracy

```
≈96%
```

Validation Accuracy

```
≈95%
```

The model performs well on unseen images with different orientations and lighting conditions.

---

# Installation

Clone the repository

```bash
git clone https://github.com/raghavach007/Coin-Classifier.git
```

Move into the project

```bash
cd Coin-Classifier
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# Usage

Run the notebook or Python script.

Upload an image containing scattered coins on a plain background.

The program will:

- Detect all coins
- Classify each coin
- Display confidence scores
- Calculate the total value

---

# Future Improvements

- Real-time webcam detection
- Mobile application
- Faster object detection using YOLO
- Support for overlapping coins
- Automatic background removal
- Currency note recognition

---

# Screenshots

## Coin Detection

<img width="378" height="494" alt="Screenshot 2026-06-30 at 10 21 23 AM" src="https://github.com/user-attachments/assets/258f3b6d-174c-4ed5-b967-57aea43fa3d3" />


---

## Coin Classification

<img width="868" height="270" alt="Screenshot 2026-06-30 at 10 23 38 AM" src="https://github.com/user-attachments/assets/00547172-4a86-4747-8e9a-b09b125eccf7" />


---

## Final Output
<img width="1190" height="1180" alt="Prediction" src="https://github.com/user-attachments/assets/5177eba3-8b77-4253-b3f0-ed616bc2afda" />


---

# Author

**Raghava Chakravarthula**

GitHub:
https://github.com/raghavach007

---

# License

This project is developed for educational and academic purposes.

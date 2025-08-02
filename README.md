# Tree Species Classification

## Introduction

This project develops and evaluates deep learning models for multi-class classification of tree species from images. The primary objective is to accurately identify different tree types using computer vision, aiding applications in environmental monitoring, forestry, and botanical research.

## Dataset

* **Source:** [Kaggle](https://www.kaggle.com/)
* **Total Images:** 1,454
* **Classes:** 30 distinct tree species

## Methodology

### 1. Data Preprocessing & Augmentation

* **Data Loading:** Dataset loaded from Google Drive into Google Colab.
* **Initial Analysis:** Checked for duplicates, corrupted files, and size anomalies. None were found.
* **Augmentation Techniques:**

  * Rotation
  * Zooming
  * Shearing
  * Horizontal flipping
  * Rescaling

### 2. Model Development & Training

Three deep learning models were trained:

* **EfficientNetB0 (Transfer Learning):**

  * Used as a feature extractor with frozen layers.
  * Added GlobalAveragePooling2D and Dense layers for classification.
  * Trained for 10 epochs.

* **Basic CNN:**

  * Built from scratch using Conv2D, MaxPooling2D, Flatten, Dense, and Dropout layers.
  * Trained for 10 epochs.

* **Improved CNN:**

  * Similar to Basic CNN with BatchNormalization layers after each convolutional layer.
  * Trained for 25 epochs.

## Results

| Model          | Validation Accuracy |
| -------------- | ------------------- |
| EfficientNetB0 | 9.03%               |
| Basic CNN      | 27.44%              |
| Improved CNN   | 27.08%              |

**Best Performing Model:** Basic CNN

## Technologies Used

* **Language:** Python
* **Libraries:** TensorFlow/Keras, Pandas, Matplotlib, Pillow (PIL)
* **Development Tools:** VS Code, Google Colab
* **Version Control:** Git
* **Dataset Platform:** Kaggle
* **Techniques:** Data Augmentation, Batch Normalization

## How to Run the Code

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Tree-Species-Classification.git
cd Tree-Species-Classification
```

### 2. Setup Google Colab

* Open the Jupyter notebook in Google Colab.
* Mount your Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

* Ensure your dataset is located at:

```
/content/drive/MyDrive/Tree_Species_Dataset
```

### 3. Install Dependencies

```bash
!pip install tensorflow
```

### 4. Run the Notebook

* Execute all cells in the notebook sequentially.
* Models will be saved in `.h5` format.

## Conclusion & Future Work

The project successfully implemented baseline deep learning models for classifying tree species from images.

### Future Improvements

* Increase dataset size and diversity.
* Explore advanced augmentation methods.
* Perform deeper hyperparameter tuning.
* Try other state-of-the-art CNN architectures.

---

**Author:** VIJAYARAGAVAN K
**License:** MIT
**Repository:** [Tree-Species-Classification](https://github.com/your-username/Tree-Species-Classification)

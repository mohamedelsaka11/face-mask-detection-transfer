# 😷 Face Mask Detection using Transfer Learning (MobileNetV2)

This project uses **Transfer Learning** with **MobileNetV2** to detect whether a person is wearing a face mask or not. The dataset consists of labeled images of people with and without face masks. The model was trained on Kaggle using TensorFlow/Keras.

---

## 📁 Dataset

The dataset was sourced from Kaggle:

- `/with_mask`: Contains images of people wearing masks.
- `/without_mask`: Contains images of people not wearing masks.

---

## 🧠 Model Architecture

- **Base Model**: MobileNetV2 (pretrained on ImageNet)
- **Top Layers**:
  - GlobalAveragePooling2D
  - Dense(128, relu)
  - Dropout layers
  - Output layer: Dense(2, softmax)

---

## 📊 Training

- Optimizer: Adam (learning rate = 0.0001)
- Loss Function: Sparse Categorical Crossentropy
- Epochs: 5
- Batch Size: 32
- Accuracy Achieved: ~99% on test set

---

## 📈 Results

The training and validation accuracy/loss curves:

![Accuracy and Loss Curves](images/Acc.png.png)

---

## 📷 Prediction Example

The model can predict on a new image:

```python
# Input an image path
input_image_path = input('Path of the image to be predicted: ')
# Output: Wearing Mask or Not
```

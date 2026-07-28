# 🧠 Multi-Class Liver Couinaud Segmentation using EfficientNetB3 U-Net

A deep learning-based medical image segmentation project that performs **multi-class liver Couinaud segment segmentation** from CT scans using a customized **U-Net architecture** with an **EfficientNetB3 encoder**. The model processes **5-channel CT images** and predicts **9 anatomical liver classes** using TensorFlow and Keras.

---

## 📌 Overview

This project implements a semantic segmentation pipeline for liver Couinaud segmentation with:

- Custom 5-channel EfficientNetB3 encoder
- U-Net decoder architecture
- Dice Loss + Categorical Cross-Entropy loss
- F1-Score evaluation metric
- Advanced data augmentation
- TFRecord-based data pipeline
- Cosine Decay Learning Rate Scheduler

The model is trained on preprocessed CT scan slices stored as TFRecords and predicts pixel-wise liver segment labels.

---

## ✨ Features

- ✅ Multi-class semantic segmentation
- ✅ EfficientNetB3 pretrained encoder
- ✅ U-Net decoder architecture
- ✅ 5-channel CT image support
- ✅ Dice + Cross-Entropy combined loss
- ✅ F1 Score evaluation
- ✅ TensorFlow Data Pipeline
- ✅ TFRecord dataset support
- ✅ Data augmentation
- ✅ Cosine learning rate decay
- ✅ GPU memory optimization

---

## 🏗️ Model Architecture

```
Input (256×256×5)
        │
        ▼
EfficientNetB3 Encoder
        │
 Skip Connections
        │
        ▼
     U-Net Decoder
        │
        ▼
 Softmax Output (9 Classes)
```

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- EfficientNetB3
- NumPy
- Matplotlib
- Segmentation Models
- TFRecord
- Google Colab / Kaggle

---

## 📂 Project Structure

```
├── data/
│   ├── train_set/
│   ├── dev_set/
│   ├── test_set/
│   └── size.json
│
├── models/
│
├── notebooks/
│
├── train.py
├── utils.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Dataset

The dataset consists of preprocessed CT scan slices stored as TFRecord files.

**Input**

- Image Size: **256 × 256**
- Channels: **5**
- Format: TFRecord

**Output**

- Pixel-wise segmentation mask
- **9 segmentation classes**

---

## 📊 Data Augmentation

The training pipeline includes:

- Random Rotation
- Random Scaling
- Random Shearing
- Horizontal Flip
- Vertical Flip
- Random Shift
- CutOut Augmentation

These augmentations improve model robustness and reduce overfitting.

---

## 🎯 Loss Function

The model is optimized using a combination of:

- Categorical Cross-Entropy Loss
- Dice Loss

**Combined Loss**

```
Loss = Categorical Cross Entropy + Dice Loss
```

---

## 📈 Evaluation Metric

The primary evaluation metric is:

- **F1 Score (Dice Score)**

This metric measures the overlap between predicted and ground truth segmentation masks.

---

## ⚡ Training Configuration

| Parameter | Value |
|-----------|-------|
| Image Size | 256 × 256 |
| Channels | 5 |
| Batch Size | 10 |
| Epochs | 250 |
| Learning Rate | 1e-4 |
| Optimizer | Adam |
| LR Scheduler | Cosine Decay |
| Classes | 9 |

---

## 🚀 Installation

Clone the repository

```bash
git clone https://github.com/your-username/liver-couinaud-segmentation.git
```

Move into the project

```bash
cd liver-couinaud-segmentation
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Training

Run the training script

```bash
python train.py
```

---

## 📊 Results

The model predicts pixel-wise liver Couinaud segments with a multi-class semantic segmentation approach using EfficientNetB3 as the encoder and U-Net as the decoder.

Performance can be evaluated using:

- Dice Score
- F1 Score
- Validation Loss

---

## 🔮 Future Improvements

- Attention U-Net
- Deep Supervision
- Mixed Precision Training
- Test Time Augmentation
- Transformer-based Encoder
- 3D Medical Image Segmentation
- MONAI Integration

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Push the branch
5. Open a Pull Request

---

## 📜 License

This project is intended for educational and research purposes.

---

## 👨‍💻 Author

**Vedant Maladkar**

B.Tech Data Science Student  
NMIMS MPSTME

GitHub: https://github.com/your-username

---

## ⭐ Support

If you found this project helpful, consider giving it a **⭐ Star** on GitHub.

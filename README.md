# 🧠 Cancer-jordan-Project

This project is a collaborative AI/ML research project by **Tanish Chavan** and **Jordan** aimed at building robust classification models to detect various types of cancers using image-based datasets.

We focused on **four different cancer types**, using four distinct datasets. Each dataset was trained using a deep learning model based on **MobileNetV2**, which gives great accuracy with minimal computational power—perfect for mid-tier machines.

---

## 🩻 Datasets Used

| Cancer Type       | Dataset Description                  | Size     |
|-------------------|--------------------------------------|----------|
| 🧠 Brain Tumor     | Not included                         | N/A      |
| 👄 Cervical Cancer | Pap smear cell images                | ~5000    |
| 🧴 Skin Cancer     | ISIC-like dermatoscopic images       | ~3000    |
| 💉 Leukemia        | Blood smear images (ALL, AML types)  | ~1500    |
| 🎀 Breast Cancer   | Histopathologic scan images          | ~2000    |

> 📁 Note: All datasets were preprocessed and augmented before training. Image normalization, resizing, and augmentation techniques (flip, rotate, zoom) were applied for better model generalization.

---

## 🧠 Model Architecture

- ✅ **Base Model**: MobileNetV2 (Pretrained on ImageNet)
- 🔄 Fine-tuned last few layers for feature extraction
- 🧪 Trained using:
  - **Adam optimizer**
  - **Categorical cross-entropy**
  - **Accuracy, Precision, Recall, F1-score** as evaluation metrics

Each model was trained individually on respective datasets.

---

## 📊 Performance

| Cancer Type       | Accuracy | Precision | Recall | F1-Score |
|-------------------|----------|-----------|--------|----------|
| Cervical Cancer   | 92%      | 91%       | 93%    | 92%      |
| Skin Cancer       | 89%      | 88%       | 90%    | 89%      |
| Leukemia          | 95%      | 94%       | 96%    | 95%      |
| Breast Cancer     | 91%      | 90%       | 92%    | 91%      |

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/tanishchavaan/Cancer-jordan-Project.git
cd Cancer-jordan-Project

# Install requirements
pip install -r requirements.txt

# Run training (example)
python train_cervical.py
python train_skin.py
python train_leukemia.py
python train_breast.py

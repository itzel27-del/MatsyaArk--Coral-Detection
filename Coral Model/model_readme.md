```markdown
# 🌊 Coral Bleaching Detection – Model Training

This repository contains code for training a **lightweight deep learning model** to detect **coral bleaching** using transfer learning with **MobileNetV2**. The model is trained on a coral reef dataset and achieves high validation accuracy, making it suitable for deployment in lightweight applications.

---

## 📌 Features
- 📂 Dataset loading with **PyTorch `ImageFolder`**
- 🔄 Train-validation split for robust evaluation
- 🖼️ Image preprocessing with resizing and normalization (ImageNet stats)
- 🤖 Transfer learning using **MobileNetV2**
- 🎯 Binary classification:  
  - **Bleached**  
  - **Not Bleached (Unbleached)**
- 📊 Training loss & validation accuracy plots
- 💾 Saves trained model as `coral_bleaching_lightweight.pt`

---

## 🚀 Tech Stack
- **Python 3.x**
- **PyTorch** (deep learning framework)
- **Torchvision** (datasets & pretrained models)
- **Matplotlib** (for plotting)
- **PIL / Pillow** (image handling)

---

## ⚙️ Training Setup

1. **Dataset Structure**  
   Your dataset should be organized as:

```

dataset/

└── Train/

├── Bleached/

│   ├── img1.jpg

│   ├── img2.jpg

│   ...

└── Unbleached/

├── img3.jpg

├── img4.jpg
...

````

Modify the path in the script:
```python
DATA_DIR = "/path/to/Train"
````

2. **Install dependencies**

   ```bash
   pip install torch torchvision matplotlib pillow
   ```

3. **Run training**

   ```bash
   python train.py
   ```

---

## 📊 Training Results

* **Epochs:** 5
* **Validation Accuracy:** \~97%
* **Loss Curve & Accuracy Plot:**

The script generates training loss and validation accuracy plots:

* Training Loss ↓
* Validation Accuracy ↑

<img width="784" height="350" alt="image" src="https://github.com/user-attachments/assets/a9de3bca-0a11-4fef-95f0-a378169bb638" />


---

## 💾 Saved Model

After training, the model is saved as:

```
coral_bleaching_lightweight.pt
```

You can later load it for inference:

```python
import torch
from torchvision import models

model = models.mobilenet_v2(weights=None)
model.classifier[1] = torch.nn.Linear(model.classifier[1].in_features, 2)
model.load_state_dict(torch.load("coral_bleaching_lightweight.pt"))
model.eval()
```

---

## 🌍 Use Case

This model can be deployed to:

* Assist researchers in **coral reef monitoring**
* Provide **AI-powered tools** for marine conservation
* Raise **awareness about climate change impacts**

---

## 📜 License

This project is licensed under the **MIT License** – free to use and modify.

---

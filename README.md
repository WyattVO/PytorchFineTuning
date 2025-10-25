# 🧠 PyTorch Fine-Tuning: ResNet18 on CIFAR-10

Using **PyTorch**, this project demonstrates **transfer learning** by freezing all layers of a pretrained **ResNet18** model (trained on ImageNet) except for the final fully connected layer.  
Only the last layer is retrained for a few epochs on the **CIFAR-10** dataset, which contains 10 classes such as airplanes, cars, and birds.

---

## 🚀 Project Summary

- **Model:** `ResNet18 (pretrained on ImageNet)`
- **Dataset:** `CIFAR-10`
- **Method:** Freeze all convolutional layers → retrain final layer
- **Optimizer:** `SGD (lr = 0.01, momentum = 0.9)`
- **Epochs:** 5
- **Results:** Validation accuracy stabilized around **78–79%**, showing consistent learning and a well-generalized model.

---

## 📈 Validation Accuracy Over Epochs

<p align="center">
  <img width="437" height="770" alt="Validation Accuracy Plot"
       src="https://github.com/user-attachments/assets/18cbe212-788d-4191-ad86-1e448783f25d" />
</p>

---

## 🧩 Key Takeaways

✅ Transfer learning allows strong performance even with minimal training.  
✅ Freezing pretrained layers speeds up training dramatically.  
✅ Accuracy stability (~78-79%) indicates the model generalizes well without overfitting.

---

## 🛠️ How to Run

```bash
# 1️⃣ Install dependencies
pip install torch torchvision matplotlib

# 2️⃣ Run the training script
python train_finetune.py

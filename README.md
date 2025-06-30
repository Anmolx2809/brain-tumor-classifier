# 🧠 Brain Tumor Classifier using CNN

A deep learning-based image classification project that detects the presence of brain tumors in MRI scans using Convolutional Neural Networks (CNNs).

---

## 🚀 Overview

- Built using **Python, Keras, and TensorFlow**
- Achieved **~78% validation accuracy**
- Dataset: 200+ labeled MRI images
- Model: 4 Conv layers, MaxPooling, Dropout, Dense layers
- Final model saved as `best_model.h5`

---

## 🗂️ Project Structure

├── brain_tumor_classifier.ipynb # Main code (Colab-compatible)
├── test_mri.jpg # Sample MRI image (optional)
└── best_model.h5 # Trained model (hosted externally)

yaml
Copy
Edit

---

## 🧪 Sample Prediction

You can try the model on a real MRI image.

```python
# Load image
img = cv2.imread("test_mri.jpg")
img_resized = cv2.resize(img, (150, 150))
img_array = np.expand_dims(img_resized / 255.0, axis=0)

# Predict
prediction = model.predict(img_array)
print("Tumor Detected ✅" if prediction[0][0] > 0.5 else "No Tumor ❌")
📦 Dataset Info
Dataset used: Brain MRI images categorized into:

yes — with tumor

no — without tumor

Images were resized, augmented, and split into training & validation sets.

🧠 Model Architecture
4 Convolutional layers + ReLU

MaxPooling & Dropout layers

Flatten → Dense → Output

Early stopping + ModelCheckpoint

Binary classification using sigmoid

📥 Download Trained Model
🔗 Download best_model.h5
(File is hosted on Google Drive due to GitHub file size limits)

🙋‍♂️ About Me
Anmol Sinha
B.Tech CSE @ BML Munjal University
Built with passion to explore real-world AI & medical applications
LinkedIn | GitHub

⭐ Give a Star!
If you found this helpful, please ⭐ star the repo. It keeps me motivated!

## 🧬 Enhancing Spina Bifida Detection Using Conditional GAN (cGAN)

This project leverages a **Conditional Generative Adversarial Network (cGAN)** to enhance Spina Bifida detection using **textual data**. Instead of medical images, the model is trained on structured or semi-structured text (e.g., clinical notes, patient records, or encoded features), allowing for data augmentation in low-resource scenarios.

---

### 📁 Project Structure

```
├── dataset/             # Contains textual dataset (CSV, JSON, etc.)
├── cgan1.ipynb          # Jupyter notebook (Colab-compatible) with model pipeline
├── README.md            # Project overview and instructions
```

> ✅ Notebook is written in standard Jupyter format and works seamlessly on **Google Colab** for GPU-accelerated training.

---

### 🧠 Project Overview

- **Data Type**: Textual/spreadsheet-based patient data (e.g., diagnostic codes, symptom descriptions, lab values)
- **Goal**: Use cGAN to generate synthetic samples conditioned on Spina Bifida labels
- **Benefit**: Augments limited real-world clinical data, boosting downstream classifier performance

---

### 🚀 Getting Started

1. **Clone this repo**:
   ```bash
   git clone https://github.com/parzival82003/spina-bifida-cgan.git
   cd spina-bifida-cgan
   ```

2. **Run the notebook**:
   Open `cgan1.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.

3. **Upload your dataset**:
   - Place your textual dataset (e.g., `.csv`) inside the `dataset/` folder
   - The notebook includes preprocessing and formatting steps

4. **Train and Generate**:
   - Train the cGAN to learn the conditional distribution of textual features
   - Generate synthetic patient records or features for class balancing

---

### 🧪 Techniques Used

- **Conditional GAN** for generating tabular/textual data
- **Feature encoding & normalization**
- **ML classifiers (e.g., Random Forest, SVM, or Neural Nets)** to evaluate augmented data
- **Evaluation metrics**: Accuracy, Precision, Recall, F1-score

---

### 📊 Sample Outputs

- Real vs. generated feature distributions
- Classifier performance before/after augmentation
- Synthetic samples conditioned on target label (Spina Bifida)

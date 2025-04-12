# CGAN-TEXTUAL-DATA-CLASSIFICATION
This project explores the use of Conditional Generative Adversarial Networks (cGANs) to enhance the detection and diagnosis of Spina Bifida, a neural tube defect affecting the spinal cord. The aim is to improve medical image classification accuracy by generating high-quality, class-specific synthetic data to augment limited clinical datasets.
🔬 Key Features
cGAN-based Data Augmentation: Uses a Conditional GAN to generate synthetic medical images conditioned on Spina Bifida labels.

Improved Classification: Augmented datasets improve the performance of traditional CNN classifiers.

Medical Imaging Focus: Tailored for spinal cord MRI or CT datasets with labeled Spina Bifida cases.

Evaluation Metrics: Includes F1-score, precision, recall, and confusion matrix for robust performance assessment.

Customizable Pipeline: Modular architecture allows easy integration with different datasets or classifiers.

🧠 Why cGAN?
Conditional GANs provide more control over data generation compared to traditional GANs by conditioning the generation process on class labels. This is especially beneficial in medical imaging, where labeled data is often scarce and class imbalance is common.

bash
Copy
Edit
git clone https://github.com/your-username/spina-bifida-cgan.git
cd spina-bifida-cgan
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run training:

bash
Copy
Edit
python train_cgan.py
📊 Results
The enhanced dataset significantly boosts the model's ability to detect Spina Bifida in imbalanced datasets, demonstrating the potential of GAN-based augmentation in clinical applications.



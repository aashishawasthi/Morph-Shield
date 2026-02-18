Morph Shield: AI-Powered Deepfake Detection System
Project Overview
Morph Shield is a deep learning system that detects AI-generated images (deepfakes) using a Convolutional Neural Network trained on 80,000 images. It achieves 87.3% validation accuracy and runs entirely in Google Colab's free tier.

✨ Key Features
Accurate Detection: 87.3% validation accuracy on 16,000 test images

User-Friendly: Simple upload-and-test interface with confidence scores

Optimized for Colab: Complete training in under 25 minutes

Batch Processing: Handles 80,000+ images with smart naming system

Corrected Logic: Proper interpretation of prediction scores (>0.5 = REAL)

🏗️ Model Architecture
text
Input (96x96x3)
    ↓
Conv2D (32 filters, 3x3) → MaxPooling → Dropout (0.25)
    ↓
Conv2D (64 filters, 3x3) → MaxPooling → Dropout (0.25)
    ↓
Conv2D (128 filters, 3x3) → MaxPooling → Dropout (0.25)
    ↓
Flatten → Dense (128) → Dropout (0.5) → Dense (1, sigmoid)
📊 Performance Metrics
Metric	Value
Validation Accuracy	87.3%
Training Time	~22 minutes
Inference Time	~200ms per image
Model Size	~45 MB
🚀 How to Use
Training a New Model
Open notebooks/Morph_Shield_Training.ipynb in Google Colab

Run Cell 1 to set up directories

Upload dataset batches (Cells 2-5) when prompted

Run Cell 6 to train the model

Download the trained model when complete

Testing Images
Open notebooks/Morph_Shield_Testing.ipynb in Google Colab

Run Cell 1 to upload your trained model

Run Cell 2 to start the testing interface

Upload images to analyze

View results with confidence scores

📁 Project Structure
text
Morph-Shield/
│
├── 📁 notebooks/
│   ├── Morph_Shield_Training.ipynb
│   └── Morph_Shield_Testing.ipynb
│
├── 📁 model/
│   └── best_deepfake_model.h5
│
├── 📁 screenshots/
│   └── testing_results.png
│
├── README.md
└── requirements.txt
🧪 Sample Results
https://screenshots/testing_results.png

📦 Dependencies
text
tensorflow>=2.0.0
numpy>=1.19.0
matplotlib>=3.3.0
Pillow>=8.0.0
opencv-python>=4.5.0
👨‍💻 Author
Your Name

GitHub: @aashishawasthi

Email: aashishawasthi098@gmail.com

📄 License

MIT License

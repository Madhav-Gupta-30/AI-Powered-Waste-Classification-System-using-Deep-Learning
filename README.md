# AI-Powered-Waste-Classification-System-using-Deep-Learning
AI-powered waste classification system that identifies waste materials using Deep Learning and Transfer Learning (VGG16). The system supports image upload and real-time webcam classification through a FastAPI backend and web interface, achieving 92% accuracy across six waste categories.

♻️ AI-Powered Waste Classification System

An AI-powered waste classification system that automatically identifies waste materials using Deep Learning and Transfer Learning. The system helps users correctly classify waste and promotes sustainable recycling practices.

The model uses a VGG16 Convolutional Neural Network fine-tuned on a dataset of six waste categories. Users can classify waste through image upload or real-time webcam detection via a web-based interface powered by FastAPI.

🚀 Features

Deep Learning based waste classification

Transfer Learning using VGG16

Real-time webcam detection

Image upload prediction

FastAPI backend for model inference

User-friendly web interface

Provides disposal instructions for each waste type

Achieves ~92% classification accuracy

🧠 Waste Categories

The system classifies waste into six categories:

Cardboard

Glass

Metal

Paper

Plastic

Trash

🛠 Tech Stack
Machine Learning

Python

TensorFlow / Keras

VGG16 Transfer Learning

NumPy

Scikit-learn

OpenCV

Backend

FastAPI

Frontend

HTML

CSS

JavaScript

Axios

📂 Dataset

The dataset contains 2527 images across six waste categories.

Category	Images
Cardboard	403
Glass	501
Metal	410
Paper	594
Plastic	482
Trash	137

Dataset Split:

80% Training

20% Validation

🧠 Model Architecture

The model uses Transfer Learning with VGG16.

Architecture:

Input Image (224x224x3)
        ↓
VGG16 Base Model (Pretrained on ImageNet)
        ↓
Global Average Pooling
        ↓
Dense Layer (512 neurons)
        ↓
Dropout
        ↓
Dense Layer (256 neurons)
        ↓
Dropout
        ↓
Softmax Output (6 Classes)
⚙️ Training Strategy

The model is trained in two phases:

Phase 1 – Initial Training

Freeze VGG16 base layers

Train custom classification head

Phase 2 – Fine Tuning

Unfreeze all layers

Train entire network with a lower learning rate

Data augmentation techniques such as rotation, zooming, flipping, translation, and normalization are applied to improve generalization.

📊 Model Performance

Accuracy: 92.3%

Macro F1 Score: 0.91

Inference Time

< 1 second (CPU)

< 0.1 seconds (GPU)

🏗 System Architecture
User
 ↓
Web Interface (HTML / CSS / JS)
 ↓
FastAPI Backend
 ↓
Image Preprocessing
 ↓
Deep Learning Model (VGG16)
 ↓
Prediction + Disposal Instructions
📁 Project Structure
waste-classification-ai/
│
├── dataset/
│   ├── train/
│   └── validation/
│
├── model/
│   └── waste_classification_model.h5
│
├── backend/
│   ├── main.py
│   └── requirements.txt
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── notebooks/
│   └── model_training.ipynb
│
├── images/
│   ├── demo.png
│   └── architecture.png
│
├── README.md
└── requirements.txt

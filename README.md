# 🧠 Pathology Image Classification for colorectal cancer detection using Continual Learning

Using Experience Replay (ER) and Synaptic Intelligence (SI)

📌 Overview
This project implements continual learning for multi-class pathology image classification, preventing catastrophic forgetting as new disease classes are introduced over time.

Two techniques are used:

Experience Replay (ER): Stores and replays representative samples from past tasks.

Synaptic Intelligence (SI): Regularizes important weights to preserve previously learned knowledge.

🔬 Application
Helps build robust AI models for digital pathology that adapt to new disease classes incrementally, without retraining from scratch.

🚀 Key Features

Incremental training on multiple tasks (Classes 0–8)

Experience Replay with a dynamic memory buffer

Synaptic Intelligence to preserve important model parameters

CNN-based feature extraction and classification

Evaluation of forgetting, accuracy, and task-wise performance

📁 Dataset
PathMNIST (or your custom pathology dataset)

Each class corresponds to a pathology category (e.g., cancer type)

Dataset is split into incremental tasks (e.g., one new class per task)

🛠️ Technologies
Python

PyTorch / TensorFlow (specify what you used)

NumPy, Matplotlib

Scikit-learn (for evaluation metrics)

🧩 Training Workflow
Initialize model and replay buffer

Train on first task (e.g., classes 0 & 1)

For each new task:

Mix current task data with replay buffer

Train using ER and apply SI regularization

Update buffer with new representative samples

Output final model trained on all classes (0–8)

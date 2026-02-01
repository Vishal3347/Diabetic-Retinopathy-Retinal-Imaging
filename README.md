Diabetic-Retinopathy-Retinal-Imaging


A production-ready API for automated detection and classification of Diabetic Retinopathy (DR) severity using deep learning. The system classifies retinal fundus images into 5 severity grades (0-4) with clinical-grade accuracy.

📊 Project Overview
This project implements an end-to-end machine learning system for diabetic retinopathy screening, featuring a CNN-based classification model served through a scalable REST API. Designed for real-time inference with <200ms latency, it's deployed on AWS ECS with full CI/CD automation.

🏗️ Architecture

    A[Client Request] --> B[FastAPI Server]
    B --> C[Image Preprocessing]
    C --> D[TensorFlow Model]
    D --> E[Severity Classification 0-4]
    E --> F[JSON Response]
    
    G[GitHub Actions CI/CD] --> H[Docker Build]
    H --> I[AWS ECR Push]
    I --> J[AWS ECS Deployment]
    J --> K[Auto-scaling Group]


✨ Key Features
Multi-class Classification: Grades 0-4 diabetic retinopathy severity

High Performance: <200ms end-to-end inference latency

Production Ready: Fully containerized with Docker

Scalable Deployment: AWS ECS with auto-scaling

CI/CD Pipeline: Automated builds & deployments via GitHub Actions

RESTful API: Clean, documented API endpoints

Health Monitoring: Built-in health checks and metrics

🛠️ Tech Stack
Core Technologies
Python 3.9+ - Primary programming language

FastAPI - High-performance web framework

TensorFlow 2.x - Deep learning framework

OpenCV - Image processing

Pillow - Image manipulation

Deployment & Infrastructure
Docker - Containerization

AWS ECS - Container orchestration

AWS ECR - Container registry

GitHub Actions - CI/CD automation

Docker Compose - Local development

Monitoring & Observability
Prometheus (Optional) - Metrics collection

Grafana (Optional) - Visualization

AWS CloudWatch - Logging & monitoring

📁 Dataset
EyePACS Dataset
The model was trained on the EyePACS dataset containing:

88,702 retinal fundus images

5 severity grades (0-4) of diabetic retinopathy

Professional clinical labels from ophthalmologists

Dataset Structure:

Grade 0: No DR

Grade 1: Mild DR

Grade 2: Moderate DR

Grade 3: Severe DR

Grade 4: Proliferative DR

Access: EyePACS on Kaggle

📚 Model Details
Architecture
Backbone: EfficientNet-B3 (Transfer Learning)

Classification Head: Custom dense layers

Input Size: 512x512 RGB images

Output: 5-class softmax (0-4 severity)

Training Process
Dataset: EyePACS (88,702 images)

Augmentation: Rotation, flipping, brightness adjustment

Optimizer: AdamW with weight decay

Loss: Categorical Crossentropy

Validation: 5-fold cross-validation


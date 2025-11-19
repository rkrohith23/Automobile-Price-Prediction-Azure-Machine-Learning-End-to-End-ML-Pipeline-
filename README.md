# Automobile-Price-Prediction-Azure-Machine-Learning-End-to-End-ML-Pipeline-
Complete ML pipeline in Azure ML: data preprocessing, regression training, real-time inference, AKS deployment, endpoint testing. Demonstrates cloud ML engineering &amp; MLOps fundamentals.

📌 Project Overview

The goal of this project is to predict automobile prices using various vehicle features (engine size, horsepower, curb weight, etc.) using Azure Machine Learning.

This project covers:

✔ Data ingestion
✔ Data cleaning & transformations
✔ Training pipeline using Azure ML Designer
✔ Creating real-time inference pipeline
✔ Deploying the model to Azure Kubernetes Service (AKS)
✔ Testing the deployed REST API endpoint

This aligns strongly with real-world Microsoft Cloud & AI workflows and is highly relevant for Data Scientist, ML Engineer, and Cloud AI Engineer roles.

🏗 Architecture
🔵 1. Training Pipeline

The training pipeline includes:

Convert to Dataset

Select Columns in Dataset

Clean Missing Data (applied during transformation)

Train Model (Linear Regression)

Split Data

Evaluate Model

🟢 2. Real-Time Inference Pipeline

Web Service Input

Select Columns (remove target column price)

Apply Transformation (same transformations as training)

Score Model

Web Service Output

📊 Dataset

Source: Automobile Price Dataset
Type: Tabular
Format: CSV
Columns: Numeric + categorical features describing automobile characteristics
Target: price

Data is automatically profiled using Azure ML's Explore feature to inspect:

Missing values

Data types

Summary statistics

🤖 Model
Algorithm:

🔹 Linear Regression (Regression → Numeric Prediction)

Why Linear Regression?

Suitable for continuous numeric outputs

Fast training

Easy to interpret

Handles small-to-medium datasets well

🚀 Deployment
Compute Used

Training: Azure ML Compute Cluster

Deployment: Azure Kubernetes Service (AKS)

Deployment Steps

Convert training pipeline → inference pipeline

Add Web Service Input + Output

Deploy to AKS from the Designer interface

Wait for the endpoint to finish provisioning

Test using the Test pane in the endpoint

After deployment, endpoint information includes:

✔ REST endpoint URI
✔ Primary/Secondary keys
✔ Swagger definition (API contract)
✔ Deployment logs

🛠 Technologies & Tools Used
Area	Tools
Cloud	Microsoft Azure
ML Platform	Azure Machine Learning Studio
Pipelines	Azure ML Designer
Deployment	AKS (Azure Kubernetes Service)
Language	Python (for testing endpoint)
API	REST + Swagger

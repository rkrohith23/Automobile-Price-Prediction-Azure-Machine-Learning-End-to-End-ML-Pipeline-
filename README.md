# Automobile-Price-Prediction-Azure-Machine-Learning-End-to-End-ML-Pipeline-
Complete ML pipeline in Azure ML: data preprocessing, regression training, real-time inference, AKS deployment, endpoint testing. Demonstrates cloud ML engineering &amp; MLOps fundamentals.



## 📌 Project Overview

This project demonstrates an end-to-end Machine Learning workflow in **Azure Machine Learning**, including:

- Data ingestion & preprocessing  
- Automated data transformations  
- Model training using Azure ML Designer  
- Real-time inference pipeline  
- Deployment to Azure Kubernetes Service (AKS)  
- Testing a production-ready REST API endpoint  

The goal is to **predict automobile prices** using vehicle attributes.  
This project reflects real-world **MLOps + Cloud ML Engineering** practices used at Microsoft.


## 🏗 Architecture

### 🔵 1. Training Pipeline
Components used:
- Convert to Dataset  
- Select Columns in Dataset  
- Clean Missing Data  
- Split Data  
- Train Model (Linear Regression)  
- Evaluate Model  

### 🟢 2. Real-Time Inference Pipeline
Components used:
- Web Service Input  
- Select Columns (remove label)  
- Apply Transformation  
- Score Model  
- Execute Python Script (custom output formatting)  
- Web Service Output  

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

🚀 Deployment
Compute Used

-Training: Azure ML Compute Cluster

-Deployment: Azure Kubernetes Service (AKS)

-Deployment Steps

-Converted the training pipeline → real-time inference pipeline

-Added Web Service Input and Web Service Output components

-Published the pipeline as a real-time endpoint

-Selected AKS as the deployment compute target

-Waited for the AKS deployment to finish provisioning

-Verified deployment status in the endpoint Details tab

🛠 Technologies & Tools Used
Area	-Tools / Services Used
Cloud	-Microsoft Azure
ML Platform	-Azure Machine Learning Studio (Classic & Designer)
Pipelines	-Azure ML Designer – Training & Real-Time Inference Pipelines
Deployment	-Azure Kubernetes Service (AKS) – V1 Online Endpoint
Endpoint Type	-Azure ML V1 Real-Time Endpoint (Classic)

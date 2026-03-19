# 🚗 Vehicle Data MLOps Project

An end-to-end **Machine Learning Operations (MLOps)** project that demonstrates the complete lifecycle of a production-grade ML system — from data ingestion to deployment using **MongoDB, AWS, Docker, and CI/CD pipelines**.

---

## 📌 Project Overview

This project showcases how to:

* Build modular ML pipelines
* Work with cloud databases (MongoDB Atlas)
* Deploy models using AWS services (S3, EC2, ECR)
* Automate workflows using CI/CD (GitHub Actions)
* Containerize applications using Docker

---

## 🧠 Tech Stack

* **Programming Language:** Python 3.10
* **Database:** MongoDB Atlas
* **Cloud:** AWS (IAM, S3, EC2, ECR)
* **CI/CD:** GitHub Actions
* **Containerization:** Docker
* **ML Workflow:** Custom pipeline architecture

---

## 📂 Project Structure

```
├── src/
│   ├── components/
│   ├── configuration/
│   ├── entity/
│   ├── aws_storage/
│   ├── data_access/
│
├── notebook/
├── templates/
├── static/
├── .github/workflows/
├── app.py
├── requirements.txt
├── setup.py
├── pyproject.toml
```

---

## ⚙️ Setup Instructions

### 1️⃣ Project Initialization

```bash
python template.py
```

---

### 2️⃣ Setup Local Package Imports

* Configure:

  * `setup.py`
  * `pyproject.toml`

---

### 3️⃣ Create Virtual Environment

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
pip list
```

---

## 🍃 MongoDB Setup

1. Create account on MongoDB Atlas
2. Create project & cluster (M0 free tier)
3. Create DB user
4. Allow access from anywhere:

   ```
   0.0.0.0/0
   ```
5. Get connection string (Python driver)

---

### 📊 Data Upload

* Create notebook:

  ```
  notebook/mongoDB_demo.ipynb
  ```
* Upload dataset
* Push data to MongoDB
* Verify in Atlas UI

---

## 📝 Logging & Exception Handling

* Implement:

  * `logger.py`
  * `exception.py`
* Test via:

  ```
  demo.py
  ```

---

## 🔄 ML Pipeline Components

### 1. Data Ingestion

* MongoDB connection
* Data extraction → DataFrame conversion

### 2. Data Validation

* Schema-based validation (`schema.yaml`)

### 3. Data Transformation

* Feature engineering
* Data preprocessing

### 4. Model Trainer

* Model training pipeline
* Custom estimator class

---

## 🔐 Environment Variables

### MongoDB

**Bash:**

```bash
export MONGODB_URL="your_connection_string"
```

**PowerShell:**

```powershell
$env:MONGODB_URL="your_connection_string"
```

---

## ☁️ AWS Setup

### IAM Configuration

* Create user: `firstproj`
* Attach: `AdministratorAccess`
* Generate access keys

---

### Set AWS Environment Variables

```bash
export AWS_ACCESS_KEY_ID="your_key"
export AWS_SECRET_ACCESS_KEY="your_secret"
```

---

### S3 Configuration

* Bucket name: `my-model-mlopsproj`
* Used for model storage & versioning

---

## 📦 Model Deployment Pipeline

* Model Evaluation
* Model Pusher (to S3)
* Model Registry system

---

## 🌐 Web Application

* Built using `Flask`
* Entry point: `app.py`
* Routes:

  * `/` → Home
  * `/training` → Trigger model training

---

## 🐳 Docker Setup

* Create:

  * `Dockerfile`
  * `.dockerignore`

---

## 🔁 CI/CD Pipeline

### GitHub Actions Workflow

* Located in:

  ```
  .github/workflows/aws.yaml
  ```

### Steps:

1. Build Docker Image
2. Push to AWS ECR
3. Deploy on EC2

---

## 🖥️ EC2 Deployment

### Instance Setup

* Ubuntu Server 24.04
* Install Docker:

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

---

### Self-Hosted Runner

* Connect GitHub → EC2
* Run:

```bash
./run.sh
```

---

## 🔐 GitHub Secrets

Add these in repo settings:

* `AWS_ACCESS_KEY_ID`
* `AWS_SECRET_ACCESS_KEY`
* `AWS_DEFAULT_REGION`
* `ECR_REPO`

---

## 🌍 Access Application

* Open browser:

```
http://<EC2-PUBLIC-IP>:5080
```

---

## 🚀 Key Highlights

✔ End-to-End ML Pipeline
✔ Cloud Integration (AWS + MongoDB)
✔ CI/CD Automation
✔ Dockerized Deployment
✔ Scalable Architecture

---

## 📈 Future Improvements

* Add monitoring (Prometheus/Grafana)
* Add model drift detection
* Use Kubernetes for scaling
* Add API authentication

---

## 👨‍💻 Author

**Zohaib Ali Singay**

---

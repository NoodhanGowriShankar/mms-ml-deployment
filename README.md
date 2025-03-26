# 🚀 Predictive Maintenance Project – FastAPI Deployment on AWS EC2

This repository contains the **Fault Classification API** for rotating machinery, built with **FastAPI**, powered by a **1D CNN model**, and deployed on **AWS EC2**. The project was developed during my internship, where I served as the **Product Manager**, leading the entire product lifecycle — from scoping and team coordination to deployment and documentation.

---

## 🧠 Project Summary

- ✅ Led product vision, scope, and roadmap
- ✅ Collaborated with ML team to define model requirements and success metrics
- ✅ Built and deployed a FastAPI-based ML inference API on AWS EC2
- ✅ Developed a clean frontend for uploading data and viewing predictions
- ✅ Provided pre-labeled `.npy` samples for easy testing

---

## 📦 Sample Input Files

The `label_samples/` folder contains example `.npy` files representing real sensor data with known fault classes. These can be used to try out the API without needing to format your own inputs.

> 📎 Shape: Each `.npy` file should be (4, 1013) representing 4 vibration channels over time.  
> 🧪 Prediction will return the fault class and model confidence.

---

## 📌 Connecting to the AWS EC2 Instance

> ⚠️ AWS credentials and public IP are intentionally excluded for security.

```bash
ssh -i "path/to/your-key.pem" ec2-user@<public_ip>
```

Replace `<public_ip>` with the actual IP of your EC2 instance.

---

## 📂 Navigate to the Project Directory

```bash
cd fault-classification
```

---

## 🔄 Pull the Latest Changes from GitHub

```bash
git pull origin main
```

Check current branch:
```bash
git branch
```

Switch if needed:
```bash
git checkout main
```

---

## 🧪 Activate the Python Virtual Environment

```bash
source venv/bin/activate
```

---

## 🚀 Run the FastAPI Server

```bash
uvicorn app:app --host 0.0.0.0 --port 8000 --reload
```

---

## 🌐 Access the App

- Main UI: `http://<public_ip>/`
- Swagger API docs: `http://<public_ip>:8000/docs`

---

## 📁 Project Structure

```
├── app.py                   # FastAPI backend logic
├── model.py                 # CNN model definition
├── train.py                 # Training + evaluation
├── data_loader.py           # Load + preprocess data
├── main.py                  # End-to-end ML workflow
├── best_model.keras         # Saved trained model
├── requirements.txt
├── templates/index.html     # Frontend form
├── static/                  # CSS, background, logo
├── label_samples/           # Pre-labeled test data
│   ├── sample_label_class_0_sample_0.npy
│   ├── sample_label_class_1_sample_1.npy
│   └── ...
└── README.md
```

---

## 🧾 Attribution

> ⚠️ Original model code was developed in collaboration with a few data science team member. This repo showcases my ownership of product requirements, technical integration, UI planning, deployment on AWS EC2, and cross-functional execution.

---

## 🧑‍💼 My Product Management Contributions

- 📌 Defined the problem statement and user needs for predictive maintenance  
- 🧪 Worked with ML team to align on model specs and performance criteria  
- 🛠️ Implemented FastAPI server with model integration  
- 🎨 Designed web interface with clear UI/UX for data upload and result display  
- ☁️ Set up EC2 instance, productionized the API, and configured deployment  
- 🧾 Created clear documentation for future use, testing, and stakeholder hand-off  

---

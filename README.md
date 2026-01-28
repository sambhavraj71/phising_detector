# 🛡️ ML-Based Phishing Website Detection System

A Machine Learning based web application that detects whether a given URL is **Phishing** or **Legitimate**.  
The system uses URL-based features and a trained ML model, deployed using a Flask web framework.

---

## 📌 Problem Statement
Phishing websites are a major cybersecurity threat where attackers trick users into revealing sensitive information by impersonating legitimate websites.  
This project aims to automatically identify phishing URLs using Machine Learning techniques.

---

## 🎯 Objectives
- Detect phishing websites using URL analysis
- Classify URLs as **Phishing** or **Legitimate**
- Provide a simple and user-friendly web interface
- Increase user awareness of malicious websites

---

## 🧠 Project Overview
The system takes a URL as input from the user, extracts important features from the URL, and passes them to a trained Machine Learning model.  
The model predicts whether the website is **safe** or **phishing** and displays the result on the web interface.

---

## 🏗️ Project Architecture

User → Web Interface → Flask Server → ML Model → Prediction Result


---

## 📂 Project Structure

phishing-website-detection/
│
├── app.py # Flask backend
├── model.pkl # Trained ML model
├── requirements.txt # Required Python libraries
├── README.md # Project documentation
├──train_model.py # For train the model
│
├── dataset/
│ └── dataset.csv # URL dataset
│
├── templates/
│ └── index.html # Frontend HTML
│
└── screenshots/
└── output.png # Application output screenshot


---

## 📊 Dataset Description
The dataset contains URLs labeled as:

| Label | Description   |
|------:|--------------|
| 1     | Phishing URL |
| 0     | Legitimate URL |

### Sample Dataset Format:
url,label
http://secure-paypal-login.com,1
https://google.com,0
http://bank-verification-update.net,1
https://github.com,0


---

## 🤖 Machine Learning Details
- Algorithm Used: **Logistic Regression / Random Forest / Decision Tree** *(as applicable)*
- Feature Type: URL-based features
- Model Output:
  - `1` → Phishing Website
  - `0` → Legitimate Website

---

## 🛠️ Technologies Used
- **Python**
- **Flask**
- **Machine Learning (Scikit-learn)**
- **HTML, CSS**
- **Git & GitHub**

---

## 🚀 How to Run the Project Locally

### 🔹 Step 1: Clone the Repository
```bash
git clone https://github.com/USERNAME/phishing-website-detection.git
cd phishing-website-detection
🔹 Step 2: Install Dependencies
pip install -r requirements.txt
🔹 Step 3: Train the model
python train_model.py
🔹 Step 4: Run Flask App
python app.py
🔹 Step 5: Open in Browser
http://127.0.0.1:5000/
🖥️ Application Output
The system displays one of the following results:

✅ Safe Website

⚠️ Phishing Website
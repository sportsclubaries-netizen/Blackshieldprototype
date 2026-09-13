# 🛡️ BLACKSHIELD

### Offline AI-Powered Cybersecurity & Threat Detection for Bitcoin Exchanges

BLACKSHIELD is an **offline-first AI-powered cybersecurity platform** designed to monitor Bitcoin exchange activity and detect unusual behavior that may indicate a potential security breach.

It combines **Bitcoin transaction analysis, Linux system activity, authentication events, API activity, and withdrawal behavior** to identify suspicious patterns and generate explainable risk alerts.

---

## 🚨 Problem

Bitcoin exchanges handle large volumes of transactions and sensitive financial operations. Traditional monitoring may focus mainly on blockchain transactions and can miss suspicious activity occurring within the exchange infrastructure.

BLACKSHIELD addresses this by combining **blockchain-level behavior with exchange-side security events**.

---

## 💡 Solution

BLACKSHIELD continuously monitors:

* ₿ Bitcoin transactions
* 👛 Wallet activity
* 🔐 Authentication/login events
* 🌐 API activity
* 💸 Withdrawal activity
* 🖥️ Linux system activity

The collected data is processed locally and analyzed using **AI/ML anomaly detection**.

### Basic Flow

```text
Bitcoin Transactions
        +
Exchange Security Events
        ↓
   Data Collection
        ↓
 Data Processing & Storage
        ↓
   Feature Engineering
        ↓
 AI/ML Anomaly Detection
        ↓
     Risk Analysis
        ↓
   Event Correlation
        ↓
 Risk Score & Explanation
        ↓
   Security Alert
        ↓
   Owner Dashboard
```

---

## 🤖 AI/ML

BLACKSHIELD uses **Isolation Forest**, an unsupervised machine-learning algorithm, to identify unusual behavior.

The system analyzes features such as:

* Transaction amount
* Transaction frequency
* Wallet activity
* Withdrawal frequency
* API request frequency
* Authentication activity
* Failed authentication attempts
* New withdrawal addresses
* Time-based transaction behavior

The ML model produces an **anomaly score**, which is combined with security signals to generate a final **risk score from 0–100**.

> The system identifies suspicious or anomalous behavior; it does not automatically claim that an activity is criminal.

---

## 🔗 Event Correlation

One of BLACKSHIELD's main features is correlating multiple security events.

For example:

```text
Failed Login
      ↓
API Activity Spike
      ↓
New Withdrawal Address
      ↓
Large Withdrawal
      ↓
Transaction Activity Spike
      ↓
⚠️ POTENTIAL EXCHANGE BREACH
```

Instead of treating each event independently, BLACKSHIELD combines related signals to prioritize potentially serious incidents.

---

## 📊 Dashboard

The security dashboard provides:

* Overall security status
* Risk score
* Active alerts
* Transaction monitoring
* Suspicious wallet monitoring
* Threat detection
* System activity
* AI/ML model status
* Investigation details

### Main Modules

| Module           | Purpose                              |
| ---------------- | ------------------------------------ |
| Overview         | Security status and risk summary     |
| Transactions     | Analyze Bitcoin transactions         |
| Data Center      | Upload and process local datasets    |
| Threat Detection | Identify correlated threats          |
| Alerts           | View and investigate security alerts |
| Wallet Monitor   | Monitor wallet behavior              |
| System Activity  | Monitor exchange-side events         |
| AI / ML          | View anomaly detection status        |
| Settings         | Configure monitoring and thresholds  |

---

## 🏗️ Architecture

```text
                    BLACKSHIELD
                         │
              ┌──────────┴──────────┐
              │                     │
       Bitcoin Data            Linux Events
              │                     │
              └──────────┬──────────┘
                         ↓
                FastAPI Backend
                         ↓
                Data Processing
                         ↓
                  SQLite Database
                         ↓
                Feature Engineering
                         ↓
                 Isolation Forest
                         ↓
                   Risk Engine
                         ↓
                 Alert Engine
                         ↓
                 React Dashboard
```

---

## 🛠️ Technologies

### Frontend

* React.js
* Vite
* JavaScript
* Recharts
* Lucide React

### Backend

* Python
* FastAPI
* Uvicorn

### AI / ML

* Scikit-learn
* Isolation Forest
* Pandas
* NumPy
* Joblib

### Database

* SQLite
* SQLAlchemy

### Security Monitoring

* Linux
* Python
* psutil

---

## 📁 Project Structure

```text
BLACKSHIELD/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── data/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── styles/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── ml/
│   ├── tests/
│   └── requirements.txt
│
├── agent/
│   ├── monitor.py
│   ├── collectors/
│   └── detectors/
│
├── data/
│   ├── uploads/
│   └── demo/
│
├── README.md
└── .gitignore
```

---

## 📚 Dataset & Research

BLACKSHIELD can be developed and tested using publicly available Bitcoin datasets.

### Recommended Dataset

**Elliptic Bitcoin Dataset**

The dataset contains Bitcoin transaction information suitable for transaction-graph analysis and machine-learning research.

Other useful references include:

* Bitcoin Blockchain datasets on Kaggle
* BitcoinHeist ransomware dataset
* Bitcoin Developer Documentation
* Scikit-learn Isolation Forest documentation
* Chainalysis transaction-monitoring research

---

## 🔒 Privacy & Offline Design

BLACKSHIELD is designed with a **local-first architecture**.

Sensitive exchange data can remain within the organization's infrastructure.

```text
Exchange Data
     ↓
Local Processing
     ↓
Local Database
     ↓
Local AI/ML
     ↓
Local Security Dashboard
```

No cloud AI service is required for the core detection workflow.

---

## ⚠️ Important Limitations

BLACKSHIELD is a security-monitoring and research prototype.

* ML results depend on the quality of available data.
* Anomalies do not automatically mean malicious activity.
* False positives are possible.
* Risk thresholds require tuning for the deployment environment.
* Security events may need additional investigation by security personnel.
* The prototype should be thoroughly tested before production deployment.

---

## 🚀 Future Improvements

* Real-time Linux security-agent monitoring
* More advanced behavioral models
* Improved event correlation
* Graph-based wallet investigation
* Automated model retraining
* Threat-intelligence integration
* Role-based access control
* Real-time notifications
* Production-grade Linux deployment
* Larger and more diverse datasets

---

## 🎯 Project Goal

The goal of BLACKSHIELD is to provide Bitcoin exchanges with an **offline, intelligent security monitoring system** capable of detecting unusual behavior early, connecting related security events, and helping the exchange owner investigate potential security threats.

> **Detect early. Correlate intelligently. Respond faster.**

---

## 👩‍💻 Project Status

**Status:** 🚧 Prototype / Development

BLACKSHIELD is being developed as an AI/ML-based cybersecurity project focused on Bitcoin exchange security and offline anomaly detection.

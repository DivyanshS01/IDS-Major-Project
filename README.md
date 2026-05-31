# AI-Powered Hybrid Intrusion Detection System (IDS) for Home Networks

## Overview

This project is a real-time Hybrid Intrusion Detection System (IDS) developed for monitoring and analyzing network traffic in home networks. It combines machine learning, anomaly detection, behavioral analysis, and threat intelligence to identify suspicious activities and potential cyber attacks.

The system captures live network packets using Scapy, processes them through trained AI models, and displays the results on a Streamlit dashboard.

---

## Features

* Real-time packet capture using Scapy
* Machine learning-based attack detection using Random Forest
* Zero-day anomaly detection using Isolation Forest
* DDoS attack detection
* Brute force attack detection
* Threat intelligence integration using AbuseIPDB
* Live alert generation
* Streamlit dashboard for traffic monitoring

---

## Architecture

```text
Network Traffic
       ↓
Packet Capture (Scapy)
       ↓
Feature Extraction
       ↓
Detection Engine
       ↓
 ┌─────────────────────┐
 │ Random Forest       │
 │ Isolation Forest    │
 │ DDoS Detection      │
 │ Brute Force Logic   │
 │ AbuseIPDB Check     │
 └─────────────────────┘
       ↓
Alert Generation
       ↓
Dashboard Visualization
```

---

## Project Structure

```text
.
├── data/
├── models/
├── src/
│   ├── sniffer.py
│   ├── realtime_detect.py
│   ├── train_model.py
│   ├── dataset_prep.py
│   └── threat_intel.py
│
├── dashboard/
│   └── app.py
│
├── requirements.txt
└── README.md
```

---

## Dataset

The project uses the NSL-KDD dataset for training the machine learning models. The dataset contains both normal and malicious network traffic records and is widely used for intrusion detection research.

---

## Machine Learning Models

### Random Forest

Used for detecting known attack patterns based on network traffic features.

### Isolation Forest

Used for detecting unknown or zero-day attacks by identifying abnormal network behavior.

---

## Running the Project

### 1. Start Packet Capture

```bash
python src/sniffer.py
```

### 2. Start Detection Engine

```bash
python src/realtime_detect.py
```

### 3. Launch Dashboard

```bash
python -m streamlit run dashboard/app.py
```

Open:

http://localhost:8501

---

## Detection Mechanisms

* Machine Learning Detection
* Zero-Day Detection
* DDoS Detection
* Brute Force Detection
* Threat Intelligence Verification

---

## Dashboard

The dashboard provides:

* Total Packets Captured
* ML Attack Detection Count
* Zero-Day Alerts
* DDoS Alerts
* Brute Force Alerts
* Live Traffic Monitoring
* Recent Alerts

---

## Future Enhancements

* Deep Learning Models
* Automatic Firewall Blocking
* Cloud Deployment
* Advanced Threat Intelligence Integration
* Enhanced Encrypted Traffic Analysis

---

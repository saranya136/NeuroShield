# 🧠 NeuroShield

### Adaptive Computing Based on Your Personal Interaction Baseline

NeuroShield is a **personalized adaptive-computing system** that monitors computer interaction patterns, learns the user's normal baseline, detects changes in interaction load, and activates adaptive responses when sustained or rapid increases are detected.

> NeuroShield is an experimental interaction-monitoring system, not a medical or clinical diagnostic tool.

---

## Problem Statement

* Traditional systems use **fixed thresholds** and do not adapt to individual user behavior, along with privacy concerns.

## Proposed Solution
* NeuroShield builds a **personalized baseline** from interaction patterns such as **WPM, correction rate, typing rhythm, and application switching**.
* It **does not store or analyze the actual words typed**; it uses **WPM as a numerical typing-speed metric**, improving privacy.
* The system compares current behavior with the user's baseline to **predict interaction-load changes and trigger personalized adaptive responses**.


---

## 🚀 Project Overview

Traditional computer systems respond mainly to **what the user does**.

NeuroShield explores a different approach — understanding **how the user interacts with the computer** and adapting accordingly.

```text
User Interaction
       ↓
Activity Collection
       ↓
Feature Extraction
       ↓
Personal Baseline
       ↓
Interaction Load Score
       ↓
Adaptive Response
```

---

## ✨ Features

* ✅ Personal interaction baseline learning
* ✅ Keyboard and mouse activity monitoring
* ✅ Typing speed analysis
* ✅ Correction-rate analysis
* ✅ Typing rhythm analysis
* ✅ Application switching detection
* ✅ Interaction-load scoring
* ✅ Rapid interaction-spike detection
* ✅ Real-time PyQt5 dashboard
* ✅ SQLite-based local data storage
* ✅ Adaptive mode activation

---

## 🧠 How It Works

### 1. Activity Collection

NeuroShield monitors interaction signals such as:

* Keyboard activity
* Mouse activity
* Typing intervals
* Application/window changes
* Idle time

### 2. Feature Extraction

Raw activity is converted into measurable features:

```text
WPM
Correction Rate
Typing Variability
Mouse Activity
Application Switching
Idle Time
```

### 3. Personal Baseline

Instead of using the same threshold for everyone, NeuroShield first learns the user's normal interaction pattern.

The baseline is stored locally and used for future comparisons.

### 4. Interaction Scoring

Current activity is compared against the personal baseline to generate an **interaction-load score from 0–100**.

```text
0 ─────────────── 35 ─────────────── 60 ─────────────── 100
      NORMAL             ELEVATED             HIGH
```

When high interaction load is sustained or a rapid spike is detected, NeuroShield can activate its adaptive mode.

---

## 🏗️ System Architecture

```text
Keyboard / Mouse / Window Activity
                │
                ▼
        Activity Collector
                │
                ▼
        Feature Extraction
                │
                ▼
       Personal Baseline
                │
                ▼
       Interaction Scoring
                │
        ┌───────┴───────┐
        ▼               ▼
     Normal          High Load
        │               │
        ▼               ▼
   Monitoring      Adaptive Mode
        │               │
        └───────┬───────┘
                ▼
          SQLite Storage
                │
                ▼
         PyQt5 Dashboard
```

---

## 🛠️ Tech Stack

| Category            | Technology |
| ------------------- | ---------- |
| Language            | Python     |
| GUI                 | PyQt5      |
| Input Monitoring    | pynput     |
| Windows Integration | pywin32    |
| System Monitoring   | psutil     |
| Data Processing     | NumPy      |
| Database            | SQLite     |

---

## 📂 Project Structure

```textdi
NeuroShield/
│
├── main.py
├── collector.py
├── features.py
├── baseline.py
├── scorer.py
├── adaptation.py
├── dashboard.py
├── database.py
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### Clone the repository

```bash
git clone https://github.com/saranya136/NeuroShield.git
cd NeuroShield
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run

```bash
python main.py
```

> **Platform:** The current implementation is designed primarily for Windows because it uses Windows-specific foreground-window APIs.

---

## Personal Baseline Learning
```
During the initial calibration period, NeuroShield learns the user's normal interaction pattern.
```
<img width="1098" height="752" alt="Screenshot 2026-08-23 201705" src="https://github.com/user-attachments/assets/b7de920d-ba92-45fe-9d89-d79fb9eb5d55" />


## Personal Baseline
```
After calibration, the system establishes the user's personal interaction reference.
```
<img width="633" height="217" alt="Screenshot 2026-08-23 201755" src="https://github.com/user-attachments/assets/fc3d48b8-aad3-4acc-af92-3caeeb20ebdb" />


## Good to Go
```
When the current interaction remains within the learned range, the system allows the user to continue normally.
```
<img width="1102" height="757" alt="Screenshot 2026-08-23 201823" src="https://github.com/user-attachments/assets/e1decd5f-e0c2-40b2-8bb9-c2b140240f7a" />


## Above Personal Threshold
```
When sustained interaction exceeds the personal threshold, NeuroShield recommends recovery.
```
<img width="1081" height="743" alt="Screenshot 2026-08-22 152029" src="https://github.com/user-attachments/assets/5d96cbb8-d54e-4787-af27-5f3e584d2a35" />


## Adaptive Mode
```
When elevated interaction persists, the adaptive response is activated.
```
<img width="1092" height="750" alt="Screenshot 2026-08-23 201946" src="https://github.com/user-attachments/assets/d580eef2-e2c4-4443-af86-8bb4fc673577" />


## Backend Activity Log
```
Computed interaction metrics and system states are recorded in the local SQLite backend.
```
<img width="1452" height="341" alt="Screenshot 2026-08-22 140925" src="https://github.com/user-attachments/assets/ded1142a-9ade-4428-a1fc-b394eb33413c" />


## 🔐 Privacy

NeuroShield is designed around **local processing**.

The system focuses on interaction metrics such as keystroke counts, timing, mouse activity, application switching, and interaction scores rather than intentionally storing the text typed by the user.

Data is stored locally using SQLite.

---

## 📈 Future Improvements

* Machine-learning-based personalization
* Improved anomaly detection
* Cross-platform support
* Advanced historical analytics
* OS-level focus mode integration
* Automatic notification suppression
* Personalized adaptive strategies
* Improved privacy and data controls

---

## 💡 Key Learnings

This project provides hands-on experience with:

* Real-time desktop activity monitoring
* Behavioral feature engineering
* Personal baseline modeling
* Python system programming
* PyQt5 application development
* SQLite data persistence
* Adaptive software architecture
* Human-computer interaction

---

## ⚠️ Disclaimer

NeuroShield is an **experimental software project**.

The interaction-load score represents changes in computer interaction behavior relative to a personal baseline. It should **not** be interpreted as a medical, psychological, or neurological measurement.

---

## 👨‍💻 Author

**SARANYA SHREE**

If you find NeuroShield interesting, consider giving the project a ⭐ on GitHub.

**Repository:**
https://github.com/saranya136/NeuroShield

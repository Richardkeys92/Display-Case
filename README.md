# Blue Team Project: Python File Integrity Monitor (FIM)

## 📌 Overview
This is a lightweight, host-based File Integrity Monitor (FIM) written in Python. It is designed to enforce Data Integrity—a core pillar of the CIA Triad—by continuously monitoring critical directories for unauthorized modifications, deletions, or new file creations. 

The system utilizes cryptographic hashing to generate a secure baseline and alerts security administrators in real-time if a file's digital fingerprint changes.

## 🚀 Features
* **Cryptographic Baselines:** Automatically scans a target directory and hashes files using the SHA-256 algorithm.
* **Real-Time Monitoring:** Runs an infinite verification loop to compare live file states against the trusted baseline.
* **Dynamic Alerting:** Triggers explicit terminal alerts for three distinct security events:
  * `🔥 [CRITICAL ALERT]` - File tampering/modification detected.
  * `💀 [ALERT]` - File deletion or missing asset.
  * `⚠️ [ALERT]` - New un-baselined file detected.
* **Interactive CLI:** Built-in switchboard menu allowing users to easily reset baselines or initiate the active monitor.

## 🛠️ Tech Stack & Concepts
* **Language:** Python 3
* **Libraries:** `hashlib`, `os`, `time`
* **Environment:** Windows PowerShell / VS Code
* **Core Concepts:** Data Integrity, Cryptographic Hashing (SHA-256), Continuous Monitoring, Automation

## 🔍 How It Works
1. **Baseline Generation:** The script reads the raw binary bits of all files in a protected directory, calculates their SHA-256 hex digests, and logs them into a gold-standard `baseline.txt` file using a pipe (`|`) delimiter.
2. **Comparison Loop:** When monitoring is active, the script re-hashes live files every second, evaluating them against the baseline dictionary loaded into memory.
## 👥 Acknowledgments & Tools
* Developed utilizing **Visual Studio Code** and **Windows PowerShell**.
* Built using **AI-assisted engineering methodologies** to accelerate debugging, optimize syntax, and enhance learning frameworks for neurodivergent professional development.   

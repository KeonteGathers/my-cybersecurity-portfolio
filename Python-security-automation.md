<p align="center">
  <img src="images/banner4.png" width="800">
</p>

🧰 Skills Applied

Python scripting

File integrity monitoring (FIM)

SHA-256 hashing

Baseline creation and comparison

Change detection logic

Logging and alerting

Automation for security operations

🛠 Tools Used

Python 3

hashlib (SHA-256)

OS / File system modules

Logging

Terminal / CLI

✔ Summary of Findings

Developed a Python-based File Integrity Monitoring (FIM) tool

Generated baseline hashes of critical system files

Detected unauthorized or unexpected file modifications

Logged file changes and produced simple alerts

Demonstrated ability to automate SOC tasks and reduce manual work

🧩 MITRE ATT&CK Techniques (Optional but adds credibility)

T1565 — Data Manipulation

T1490 — Inhibit System Recovery

T1059 — Command and Scripting Interpreter

# 🐍 Python Security Automation: File Integrity Monitoring (FIM)

## Overview  
Developed a Python-based security automation tool that detects unauthorized file modifications using SHA-256 hashing. This simulates enterprise file integrity monitoring (FIM) systems and improves detection capabilities for tampering or data manipulation.

---

## 🛠 Tools & Technologies  
- Python  
- hashlib  
- os module  
- time module  
- Logging  

---

## 🔍 Key Features  
- Generates SHA-256 hash for baseline file integrity  
- Detects any changes in monitored files  
- Logs modifications with timestamps  
- Supports ongoing automated monitoring  
- Provides audit trail for forensic investigations  

---

## 🧠 How It Works  

### **1. Generates a baseline hash**
On first run, the script reads the file and creates a SHA-256 hash.

### **2. Compares new hashes to the baseline**
If the hash changes, the file was modified.

### **3. Creates security logs**
Logs include:
- Timestamp  
- Old hash  
- New hash  
- Alert message  

### **4. Supports continuous monitoring**
With a loop like:

```python
while True:
    check_file()
    time.sleep(60)  # run every 1 minute
```

---

## 📘 Code Snippet

```python
import hashlib, os, time

def generate_hash(filename):
    h = hashlib.sha256()
    with open(filename, "rb") as f:
        h.update(f.read())
    return h.hexdigest()
```

---

## ✔ Final Outcome  
The automation script provides a lightweight but effective method for detecting file tampering, building the foundation for security monitoring and incident response.

This demonstrates your ability to:
- Automate security workflows  
- Apply Python to real cybersecurity problems  
- Build tools that enhance integrity and detection  

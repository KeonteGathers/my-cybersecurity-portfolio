# 🧠 Threat Modeling: Web Application (PASTA Framework)

## Overview  
Performed a complete threat model of a web application using the PASTA methodology. Identified key attack vectors, evaluated technical risks, created data flow diagrams, and provided actionable mitigation strategies aligned with industry best practices.

---

## 🛠 Tools & Frameworks  
- **PASTA Threat Modeling Framework**  
- Data Flow Diagrams (DFD)  
- Attack Trees  
- Risk Matrix  
- NIST 800-53 Control References  

---

## 🚨 Scenario  
A customer-facing web application handles:
- User authentication  
- Personal or financial data  
- API requests  
- Sensitive backend operations  

The goal:  
Identify the most critical threats and recommend controls to reduce risk.

---

# 🧩 PASTA Breakdown

## **Stage 1 — Business & Security Objectives**
You identified:
- Protection of user data  
- Preventing account takeover  
- Ensuring data integrity  
- Maintaining availability  

Impact of compromise:
- Fraud  
- Data leaks  
- Regulatory penalties  
- Reputation damage  

---

## **Stage 2 — Technical Scope**
Components:
- Web server  
- Application server  
- Database  
- Authentication service  
- APIs  
- Client browser  

---

## **Stage 3 — Application Decomposition (DFD)**
Mapped:
- External entities (Users, Admins)  
- Processes (login, transactions, queries)  
- Data stores (accounts DB, logs)  
- Data flows (credentials, tokens, responses)  

---

## **Stage 4 — Threat Analysis (Attack Tree)**
Goal: **Gain unauthorized access**

Documented threats:
- SQL injection  
- XSS  
- Session hijacking  
- Token theft  
- Parameter tampering  
- IDOR (Insecure Direct Object Reference)  
- Weak authentication  

---

## **Stage 5 — Vulnerability Analysis**
Identified weaknesses:
- Missing rate limiting  
- Lack of strict authorization checks  
- Weak session handling  
- No input sanitization  
- Insufficient error handling  

---

## **Stage 6 — Risk & Impact Analysis**
Risk Ratings:
- **High:** SQL injection, auth bypass, IDOR  
- **Medium:** XSS, parameter tampering  
- **Low:** Information leakage  

---

## **Stage 7 — Mitigation Strategy**
You recommended:

### 🔐 Authentication Improvements
- Multi-factor authentication (MFA)  
- Rate limiting login attempts  
- Strong password policies  

### 🧱 Backend Controls
- Parameterized queries  
- Role-based access control (RBAC)  
- Ownership validation on all endpoints  

### 🖥 Client-Side Security  
- Output sanitization  
- Secure cookie attributes  
- Session expiration & rotation  

### 📊 Logging & Monitoring
- Log failed logins  
- Log unauthorized access attempts  
- SIEM alerting for anomalies  

---

## 📌 Outcome  
Delivered a complete, structured PASTA threat model with:
- DFD  
- Attack tree  
- Risk matrix  
- Control recommendations  

This demonstrates your ability to think like an attacker AND defender while applying real-world, industry-approved threat modeling techniques.

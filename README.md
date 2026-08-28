# ERP-Security-Architecture-Case-Study

# Cloud ERP Security Architecture & Risk Assessment

> **Security architecture assessment and defense-in-depth redesign for a global ERP organization transitioning to an AWS-based SaaS platform and adopting AI capabilities.**

![AWS](https://img.shields.io/badge/AWS-Cloud%20Security-orange)
![IAM](https://img.shields.io/badge/IAM-Identity%20%26%20Access-blue)
![Zero Trust](https://img.shields.io/badge/Architecture-Zero%20Trust-purple)
![DevSecOps](https://img.shields.io/badge/DevSecOps-Secure%20Development-green)
![AI Security](https://img.shields.io/badge/AI-Security-red)
![NIST AI RMF](https://img.shields.io/badge/Framework-NIST%20AI%20RMF-lightgrey)

## 📌 Project Overview

This project involved conducting a **security architecture and risk assessment** for a global software company transitioning from a partially on-premises environment to a **cloud-based SaaS ERP platform hosted in AWS** while planning to introduce AI-driven capabilities.

The assessment evaluated the organization's existing security posture, identified critical security gaps, researched applicable cloud security practices, and proposed an improved **defense-in-depth security architecture** designed to strengthen identity, application, network, AI, data governance, and DevSecOps security.

The project was completed collaboratively as part of a **3-member team**.

---

## 🎯 Security Objectives

The proposed architecture was designed around five primary security objectives:

1. **Secure the Cloud ERP Platform**
2. **Enable Secure AI Adoption**
3. **Protect Customer Data & Ensure Compliance**
4. **Secure Cloud Transition & Expansion**
5. **Maintain Service Availability & Trust**

These objectives guided the risk assessment, architecture redesign, security recommendations, and implementation roadmap.

---

## 🔎 Security Assessment

The assessment examined the existing environment across **5 primary security domains**:

| Domain                            | Key Security Concerns                                                   |
| --------------------------------- | ----------------------------------------------------------------------- |
| 🌐 Network & Application Security | Unauthenticated microservices and insecure API authorization            |
| 🔐 Identity & Access Management   | Unmanaged cloud credentials and weak centralized identity controls      |
| 🤖 AI Security                    | Excessive AI-agent privileges and lack of human oversight               |
| 🗄️ Data Governance & Compliance  | Lack of data residency strategy and AI tool governance                  |
| ⚙️ DevSecOps                      | Unvalidated codebase and lack of governance for AI-assisted development |

### Key Findings

The assessment identified **7+ security risks**, including **5+ critical or high-impact security gaps**.

#### 🔴 Unauthenticated Microservice Communication

Microservices implicitly trusted one another without authentication or verification. A compromised service could therefore enable an attacker to move laterally across the environment.

**Risk:** Critical
**Impact:** Lateral movement, unauthorized access, and exposure of sensitive ERP data

#### 🔴 Insecure API Authorization

The existing API relied primarily on an account number for authorization without sufficient identity verification, session tracking, or authorization controls.

**Risk:** Critical
**Impact:** Account impersonation, unauthorized transactions, and potential financial loss

#### 🔴 Unmanaged Cloud Credentials

Developer AWS accounts were not integrated with the organization's corporate identity system and lacked centralized MFA and audit visibility.

**Risk:** Critical
**Impact:** Credential compromise, unauthorized access, and ineffective offboarding

#### 🟠 Excessive AI-Agent Privileges

Planned AI agents could perform sensitive operations such as account creation and contract management without sufficient human oversight or guardrails.

**Risk:** High
**Impact:** Privilege escalation, unauthorized actions, financial loss, and compliance violations

#### 🟠 Data Residency & AI Governance Gaps

The organization lacked a defined data residency strategy across its global operating regions and did not have sufficient governance over external AI tools.

**Risk:** High
**Impact:** Regulatory violations, financial penalties, and potential customer loss

---

## 🏗️ Proposed Security Architecture

The redesigned architecture follows a **defense-in-depth and zero-trust approach**, introducing multiple layers of security controls across external access, network security, identity, data governance, AI security, and DevSecOps.

### Architecture Layers

**1. External Access Layer**

* Zero Trust Network Access (ZTNA)
* Multi-Factor Authentication (MFA)
* Mobile Device Management (MDM)
* OAuth 2.0
* Amazon Cognito
* Web Application Firewall (WAF)

**2. Network Security Layer**

* Firewall
* IDS/IPS
* API Gateway
* Network segmentation
* Rate limiting

**3. Identity & Access Management Layer**

* AWS IAM
* SSO
* RBAC
* Privileged Identity Management
* Managed identities
* Least-privilege access

**4. Data Governance Layer**

* Region-based data residency
* Data classification
* PIPEDA / PDPL considerations
* Centralized governance
* AWS Control Tower
* Amazon Macie

**5. AI Security Layer**

* Least-privilege AI agents
* Human-in-the-Loop (HITL)
* AI activity auditing
* AWS Bedrock guardrails
* NIST AI Risk Management Framework

**6. DevSecOps Layer**

* AWS CodePipeline
* AWS CodeCommit
* Static Application Security Testing (SAST)
* Automated code analysis
* AI-assisted coding governance
* Secure CI/CD practices

---

## 🛡️ Security Controls Researched

Research was conducted into cloud security technologies and industry practices to develop the proposed architecture.

Key technologies and controls evaluated included:

* **AWS IAM & IAM Identity Center**
* **Amazon Cognito**
* **Amazon API Gateway**
* **AWS WAF**
* **AWS App Mesh / Istio**
* **OAuth 2.0**
* **Mutual TLS (mTLS)**
* **Zero Trust Architecture**
* **MFA / SSO / RBAC**
* **Privileged Identity Management**
* **AWS Bedrock**
* **AWS Control Tower**
* **Amazon Macie**
* **AWS CodePipeline**
* **AWS CodeCommit**
* **Amazon CodeGuru Reviewer**
* **NIST AI Risk Management Framework**
* **ISO 27001**

---

## 🤖 AI Security Strategy

A dedicated AI security strategy was developed because the organization planned to introduce AI agents into business-critical ERP workflows.

### Recommended Controls

| Control           | Purpose                                                               |
| ----------------- | --------------------------------------------------------------------- |
| Least Privilege   | Limit AI agents to only the resources required for their tasks        |
| Human-in-the-Loop | Require human approval for sensitive actions                          |
| AI Auditing       | Record and monitor AI activities for accountability and investigation |
| Guardrails        | Prevent unsafe or unauthorized AI behavior                            |
| AI Governance     | Establish policies for secure and responsible AI adoption             |
| NIST AI RMF       | Provide a structured approach to identifying and managing AI risks    |

---

## 📊 Risk Prioritization

The assessment prioritized risks based on **likelihood, business impact, and feasibility of remediation**.

Immediate priorities included:

```text
Identity & Access Management
          ↓
API Authentication & Authorization
          ↓
Microservice Authentication
          ↓
Network Segmentation
          ↓
AI Governance & Security
          ↓
Advanced Zero Trust Architecture
```

The assessment intentionally prioritized identity and API security before longer-term initiatives because weaknesses in these areas could directly expose critical ERP systems and customer information.

---

## 🗺️ Implementation Roadmap

A **3-phase, 0–12 month implementation roadmap** was proposed.

### Phase 1 — 0–3 Months

**Immediate Risk Reduction**

* Implement MFA
* Enforce SSO
* Strengthen API authentication
* Introduce OAuth 2.0
* Establish centralized identity management

### Phase 2 — 3–6 Months

**Structured Security Controls**

* Deploy API Gateway
* Implement centralized logging and monitoring
* Establish data classification
* Introduce AI activity logging
* Establish AI governance controls

### Phase 3 — 6–12 Months

**Advanced Security Architecture**

* Implement Zero Trust Architecture
* Introduce service mesh security
* Implement mutual TLS for microservices
* Establish comprehensive AI governance
* Deploy Human-in-the-Loop controls
* Expand automated AI auditing

---

## 💡 Key Takeaways

This project demonstrated how security architecture can be used to address security risks during a **cloud transformation and AI adoption initiative**.

### Key areas explored

* ☁️ Cloud security architecture
* 🔐 Identity & Access Management
* 🌐 API and microservice security
* 🛡️ Zero Trust Architecture
* 🤖 AI security and governance
* 🗄️ Data governance and residency
* ⚙️ DevSecOps
* 📊 Cybersecurity risk assessment
* 🗺️ Security roadmap development
* 📋 Security control evaluation

---

## 📚 Frameworks & References

The assessment incorporated concepts from:

* **NIST AI Risk Management Framework**
* **ISO 27001**
* **Zero Trust principles**
* **Defense-in-depth security**
* **Least-privilege principles**
* **PIPEDA**
* **PDPL**

AWS documentation and security resources were also researched to evaluate appropriate cloud security controls and services.

---

## 👥 Team

**Project Team:**

* Jugadbeer Sangha
* Brendan Lasko
* Parth Patel

**Date:** April 2026

---

## ⚠️ Disclaimer

This project represents a **security architecture assessment and proposed design** based on a fictionalized organizational scenario. AWS services and security controls described in this repository were researched and recommended as part of the architecture design; they were **not deployed into a production environment**.

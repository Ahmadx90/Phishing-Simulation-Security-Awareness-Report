# Phishing Simulation & Security Awareness Project 🔒

> *A controlled, ethical phishing simulation that tests human response, teaches better behaviors, and helps organizations harden their last line of defense — their people.*

## 📖 Overview

This repository contains a fully documented, ethically conducted phishing simulation built with the open-source **GoPhish** framework. The campaign was executed against **controlled test accounts only** to evaluate user behavior, gather measurable metrics, and convert results into a practical security awareness and training framework for organizations.

Included in this repository:

* A professional, reproducible simulation methodology
* Raw and anonymized campaign results with analysis
* A comprehensive Security Awareness Training Framework (10-point)
* Strategic recommendations and responsible disclosure guidance
* Reusable GoPhish templates (email & landing page) and deployment notes

---

## 🎯 Key Objectives

* **Test employee awareness:** Measure susceptibility to phishing via realistic simulation.
* **Educate:** Turn campaign findings into concrete training material.
* **Security hardening:** Recommend operational changes that reduce human risk.
* **Risk mitigation:** Identify gaps in policies, tooling, and human-factor controls.

---

## 🛠️ Technical Implementation

### Tools & Technologies

| Tool                |                                  Purpose | Version / Notes                                  |
| ------------------- | ---------------------------------------: | ------------------------------------------------ |
| GoPhish             |            Phishing simulation framework | v0.12.1 (used in this project)                   |
| Kali Linux          |        Security assessment / VM platform | 2023.3+ recommended                              |
| Gmail SMTP          |    Mail delivery for sending test emails | Use App Passwords / authorized test account only |
| VirtualBox / VMware | Virtualization environment for isolation | Use snapshotting for quick rollback              |

> **Important:** Always run simulations in isolated, non-production environments using authorized test accounts.

### Architecture & Workflow

Phishing Simulation Workflow:

1. Provision GoPhish instance (isolated VM)
2. Create sending profile (SMTP)
3. Design phishing email template
4. Clone a target landing page (test-only replica)
5. Create test user groups (explicitly authorized)
6. Launch campaign and monitor events
7. Collect and anonymize results
8. Analyze metrics and behavior
9. Produce a professional report and training plan

---

## 📊 Project Highlights

### 🎣 Campaign Details

* **Email Subject (example):** `Action Required: Verify Your Internee.pk Account`
* **Landing Page:** Test replica of Internee.pk login portal (used for demonstration only)
* **Target:** Controlled, consented test accounts (e.g. `test+user@example.com`)
* **Success Metrics:** Open rate, click-through rate (CTR), credential submission rate

> **NOTE:** Do **not** reuse real user credentials or target real users without explicit, documented authorization.

### 📈 Example Results (Anonymized)

> The figures shown here are illustrative of this controlled test scope. Real campaigns should use larger sample sizes for reliable statistics.

| Metric                | Result | Percentage |
| --------------------- | -----: | ---------: |
| Emails Sent           |      1 |       100% |
| Emails Opened         |      1 |       100% |
| Links Clicked         |      1 |       100% |
| Credentials Submitted |      1 |       100% |

> These toy-metrics demonstrate how a perfectly executed lure can succeed in a controlled environment. In production-scale testing you should expect more variance and should NEVER rely on single-data-point conclusions.

---

## 🚀 Getting Started (Quick Guide)

> **Prerequisites (minimal):**

* A non-production VM (Kali or similar)
* GoPhish downloaded and installed
* A Gmail account configured with an App Password for SMTP (or another authorized SMTP server)
* Test email accounts created explicitly for this exercise

### Installation & Run (Linux / Kali example)

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Download GoPhish
wget https://github.com/gophish/gophish/releases/download/v0.12.1/gophish-v0.12.1-linux-64bit.zip
unzip gophish-v0.12.1-linux-64bit.zip -d /opt/gophish
sudo chmod +x /opt/gophish/gophish

# Run GoPhish from its directory
cd /opt/gophish
sudo ./gophish
```

### Access the Web UI

* Open: `https://127.0.0.1:3333` (or the IP/port shown in your VM)
* **Important:** On first run GoPhish will display the admin credentials or instructions in the terminal — follow those prompts rather than assuming defaults.

### Running a Simulation (Summary)

1. Create a **Sending Profile** (use an authorized SMTP account).
2. Design an **Email Template** (realistic, but ethical phrasing).
3. Clone a **Landing Page** (test-only replica; remove third-party elements).
4. Create **User Groups** and import only authorized test accounts.
5. Launch the **Campaign** and monitor the dashboard for events.
6. Export/anonymize results for analysis and report generation.

---

## 📋 Professional Report (Included)

The full report in this repository covers:

* Executive Summary & Key Findings
* Scope, Assumptions & Authorization
* Methodology (detailed, reproducible steps)
* Campaign Analysis with screenshots and anonymized logs
* Security Awareness Guide: red flags & detection heuristics
* 10-Point Training Framework (practical modules)
* Strategic Recommendations and Operational Playbook
* References & Compliance Considerations

---

## 🛡️ Educational & Organizational Value

This repository is designed for the following audiences:

* **Security Professionals:** Reusable templates and methodology to run internal awareness programs.
* **IT Teams / SOCs:** Practical guidance for detecting and responding to phishing risks.
* **Management:** Clear, executive-friendly findings and mitigation roadmap.
* **Students & Researchers:** Hands-on, ethical example of social-engineering assessment.

---

## ⚠️ Legal & Ethical Disclaimer

This project is for **educational and authorized security testing purposes only**. By using or reproducing any content from this repository you agree to the following rules:

* ✅ Only run simulations with **explicit permission** from the system owner and documented approval.
* ✅ Use **only** test accounts and isolated environments.
* ✅ Follow responsible disclosure and local laws and regulations.
* ❌ Never use these techniques for malicious purposes.
* ❌ Never target unauthorized individuals or production systems.

Failure to follow these rules can result in legal, civil, and professional consequences.

---

## 🔗 References & Resources

* Verizon — *Data Breach Investigations Report (DBIR)*
* CISA — *Security Tip: Avoiding Social Engineering and Phishing Attacks*
* GoPhish — Official Documentation and Project Page
* NIST — Cybersecurity Framework (PR.PT, ID.AM, and relevant controls)

(See the `REPORT` folder for full citations used in the professional report.)

---

## 👨‍💻 Author

**Ahmad Sameer** (`Ahmadx90`)

* GitHub: [https://github.com/Ahmadx90](https://github.com/Ahmadx90)
* LinkedIn: [https://www.linkedin.com/in/ahmad-sameer-17b339371/](https://www.linkedin.com/in/ahmad-sameer-17b339371/)
* Email: [ahmadsameer0990@gmail.com](mailto:ahmadsameer0990@gmail.com)

---

## 📄 License

This project is released under the **Sameer's Lab 🔬 License** — see the `LICENSE` file for details.

---

## 🏷️ Tags

`cybersecurity` `phishing-simulation` `security-awareness` `gophish` `social-engineering` `penetration-testing` `security-training` `ethical-hacking`

---

If this README sings to you and you want it adapted for a GitHub front page (short intro + badges + collapsing sections), or converted into a one-page PDF or Word report — say the word and I’ll format it ready-to-publish.

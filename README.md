# 🚀 AWS Red Team & Penetration Testing Playbook 2026

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![AWS](https://img.shields.io/badge/AWS-Cloud%20Security-orange.svg)](https://aws.amazon.com/security/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Bash](https://img.shields.io/badge/Bash-Automation-green.svg)](https://www.gnu.org/software/bash/)

> **The ultimate, safety-first, fully automated AWS Penetration Testing and Red Team Operations Manual.** 
> Designed for modern cloud environments, integrating **pathfinding.cloud** IAM paths, **EKS/ECS** container attacks, **OIDC/CI-CD** supply chain abuses, and **Stratus Red Team** telemetry evasion.

---

## 🎯 Overview
Most AWS pentest checklists are outdated, dangerous, or lack automation. This repository bridges the gap between **compliance auditing** (Prowler/ScoutSuite) and **true Red Team adversary emulation**. 

It provides a complete, phased methodology—from Pre-Engagement Legal Setup to Cleanup—backed by **ready-to-deploy Bash and Python automation scripts**.

## 🛡️ Safety First: Zero-Destructive Testing
Unlike amateur repositories that suggest running `aws iam create-access-key` or launching EC2 instances, this playbook enforces **elite operational safety**:
* ✅ **`DryRun=True`** mandated for all EC2/API mutations.
* ✅ **`iam:SimulatePrincipalPolicy`** used for safe permission checking without side effects.
* ✅ **Credential Handling Best Practices** to prevent accidental leakage in logs.

## 🗺️ The Attack Lifecycle (Phases 0-9)
| Phase | Name | Description |
| :--- | :--- | :--- |
| **0** | **Pre-Engagement** | Legal RoE, Scoping, AWS Policy Compliance. |
| **1** | **Setup** | Automated tool installation (Pacu, Prowler, CloudFox). |
| **2** | **Recon** | External OSINT & Internal Asset Enumeration. |
| **3** | **IAM Enum** | Automated permission discovery & Principal Mapper. |
| **4** | **Service Test** | Deep dives into S3, EC2, Lambda, RDS, EKS, ECS. |
| **5** | **Privilege Esc** | Classic & Modern paths (pathfinding.cloud, OIDC). |
| **6** | **Exploitation** | Controlled PoC execution & IMDS/SSRF testing. |
| **7** | **Post-Exploit** | Lateral movement, Cross-Account (RAM) pivoting. |
| **8** | **Reporting** | MITRE ATT&CK mapping & Executive summaries. |
| **9** | **Cleanup** | Evidence preservation (SHA256) & artifact removal. |

## 🔥 Modern Attack Vectors Covered
Stop testing like it's 2018. This playbook includes cutting-edge attack surfaces:
* 🧠 **Modern IAM Privesc:** `pathfinding.cloud` methodologies (CodeBuild, Glue, SageMaker).
* 📦 **Container & Orchestration:** EKS IRSA abuse, ECS Task Metadata theft, IMDSv1 checks.
* 🔗 **CI/CD & Supply Chain:** GitHub Actions OIDC wildcard `sub` claim abuses, Terraform `.tfstate` poisoning.
* 🕵️ **Detection & Evasion:** Testing GuardDuty and CloudTrail visibility using **Stratus Red Team**.
* 🌐 **Cross-Account Pivoting:** AWS RAM (Resource Access Manager) boundary bypasses.
* 🧩 **Logic Bypasses:** S3 `aws:Referer` spoofing, `StringNotEquals` unauthenticated bypasses, KMS Grant abuses.

## 🛠️ The Automation Stack
* **Enumeration:** `CloudFox`, `enumerate-iam`, `Prowler`, `ScoutSuite`
* **Exploitation:** `Pacu` (RhinoSecurityLabs)
* **Privesc Mapping:** `Principal Mapper (pmapper)`
* **Telemetry Testing:** `Stratus Red Team` (Datadog)

## 📊 MITRE ATT&CK Cloud Matrix Mapping
Findings are mapped directly to enterprise threat models:
| Attack Vector | Technique ID | Technique Name |
| :--- | :--- | :--- |
| **IMDS / ECS Metadata Theft** | `T1552.005` | Credentials from Cloud Instance Metadata API |
| **IAM Privilege Escalation** | `T1098.001` | Additional Cloud Credentials |
| **GitHub OIDC Abuse** | `T1550.001` | Application Access Token |
| **Terraform State Poisoning** | `T1546.010` | Add/Modify Cloud Account |
| **Disabling CloudTrail** | `T1562.001` | Disable or Modify Cloud Logging |

## ⚡ Quick Start Guide
```bash
# 1. Clone the repository
git clone https://github.com/CeevitWonder/aws-red-team-playbook.git
cd aws-red-team-playbook

# 2. Run the master setup script (Installs all tools safely)
chmod +x scripts/master_setup.sh
./scripts/master_setup.sh

# 3. Configure your AWS Profile
aws configure --profile pentest

# 4. Execute the full automated assessment
chmod +x scripts/execute_pentest.sh
./scripts/execute_pentest.sh pentest target.com
```
## ⚠️ Legal & Disclaimer

**THIS TOOLKIT IS FOR EDUCATIONAL AND AUTHORIZED TESTING PURPOSES ONLY.**

- You **must** have explicit, written permission (Rules of Engagement) from the AWS account owner before running any scripts.
- The authors are **not responsible** for any misuse, billing spikes, or legal consequences resulting from unauthorized testing.
- Always use `DryRun=True` and test in non-production environments first.

---

## 🤝 Contributing

Found a new IAM privilege escalation path?  
Discovered a better Stratus Red Team evasion technique?  

**Pull Requests are welcome!**  

Please ensure all new scripts follow the **Safety First** doctrine.

---

## 🌟 Show Your Support

If this playbook helped you:
- Ace a cloud security interview
- Find a critical bug
- Secure your organization's cloud environment

Please consider **starring** ⭐ this repository and sharing it with the InfoSec community!


---

## 👤 About the Author

<div align="center">
  <img src="https://github.com/CeevitWonder.png?size=100" style="border-radius: 50%;" width="100" height="100"/>
  <br>
  <b>MD Nahid Hasan (Ceevit Wonder)</b>
  <br>
  <i> eJPT | Penetration Tester | Cybersecurity Compliance Auditor | NIST/CIS Frameworks | Red Team Practitioner | Cloud Offensive Security Researcher </i>
</div>

<p align="center">
  <a href="https://www.linkedin.com/in/nahidmohammadhasan/">🔗 LinkedIn</a> •
  <a href="mailto:your.mnahid.infosec@gmail.com">📧 Email</a> •
  <a href="https://ceevitwonder.netlify.app/">🌐 Live Website</a>
</p>

> **💼 Open to Global Remote Opportunities:** I am currently available for remote Cloud Red Team, AWS Pentesting and DevSecOps engagements. If you need an operator who builds safety-first, automated exploitation frameworks, let's talk.

<sub>© 2026 Ceevit Wonder. Licensed under the MIT License. Built with ☕ and a relentless pursuit of cloud security excellence.</sub>

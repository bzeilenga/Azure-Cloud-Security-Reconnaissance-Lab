# ☁️ Azure Cloud Security Foundations & Reconnaissance (Free Tier)

## Project Summary

This project demonstrates the deployment and security hardening of cloud infrastructure in **Microsoft Azure** using **free-tier services**. The lab focuses on core cloud engineering tasks including resource organization, virtual machine provisioning, secure remote access, and enabling native cloud security monitoring with **Microsoft Defender for Cloud**.

This repository represents the **foundation phase** of a larger cloud security automation project and mirrors real-world responsibilities of **Cloud Engineers and Cloud Security Engineers**.

---

## Cloud Skills Demonstrated

- Azure resource management and governance
- Infrastructure provisioning (IaaS)
- Secure remote access using SSH
- Native cloud security monitoring
- Understanding security telemetry and alert behavior
- Cost-aware cloud design (free-tier usage)

---

## Target Roles

- Cloud Engineer  
- Cloud Security Engineer  
- DevOps / Platform Engineer  
- Site Reliability Engineer (SRE)  
- Junior Solutions Architect  

---

## Prerequisites

- Microsoft Azure subscription (Free Tier)
- Basic Linux administration
- SSH client (Terminal, PowerShell, or PuTTY)

---

## Step 1: Azure Subscription Setup

1. Create an Azure Free Tier account at:
   - https://azure.microsoft.com/free
2. Activate the trial subscription with included credits

This lab is intentionally designed to remain within **free-tier limits**, reflecting real-world cost controls in cloud environments.

---

## Step 2: Resource Group Design

1. In the Azure Portal, navigate to **Resource Groups**
2. Create a new resource group :
   - **Name:** `[insert-resource-group-name]` 
   - **Region:** Select a preferred Azure region
3. Review and create
<img width="1600" height="586" alt="image" src="https://github.com/user-attachments/assets/18ef7060-ba5a-43b8-bfcb-f3cb482b75fc" />

---

## Step 3: Virtual Machine Provisioning (IaaS)

1. Navigate to **Virtual Machines** → **Create**
2. Configure the VM:
   - **Image:** Ubuntu Server 20.04 LTS
   - **Size:** B1s (free-tier eligible)
   - **Authentication:** SSH key or password
3. Networking:
   - Allow inbound **SSH (TCP 22)** only
4. Create the VM

<img width="1273" height="588" alt="image" src="https://github.com/user-attachments/assets/dd1386da-22d7-4eea-981a-d014ec768de2" />

Once deployed, record the **public IP address** and **admin username** for secure access.

---

## Step 4: Enable Native Cloud Security Monitoring

1. Open **Microsoft Defender for Cloud**
2. Navigate to **Environment Settings**
3. Select the active subscription
4. Enable:
   - **Servers - Status ON**
5. Save configuration

![Screenshot 2026-01-29 093014](https://github.com/user-attachments/assets/0611ecc3-6621-42ae-86c0-08dbf2834456)

This enables continuous security posture monitoring using **Azure-native tooling**, reducing reliance on third-party agents.

Cloud Security Insight

Host-based reconnaissance does not always generate immediate alerts

Defender for Cloud evaluates behavior over time

Alert generation may be delayed or suppressed in low-risk scenarios

This reflects real-world cloud security operations, where detection is contextual and telemetry-driven rather than event-based.
---

## Step 5: Secure Access and Telemetry Generation

### SSH Access

From a local terminal or PowerShell session:
<img width="740" height="700" alt="image" src="https://github.com/user-attachments/assets/1f681624-36a2-4488-8b9c-f8a7a7fe3da3" />
<img width="1066" height="346" alt="image" src="https://github.com/user-attachments/assets/e1df2299-3a90-4e39-a9b3-5c99a6390857" />
<img width="498" height="156" alt="image" src="https://github.com/user-attachments/assets/c1973de7-e976-4098-b9fc-888d403fd9d8" />

This activity simulates local discovery behavior, commonly associated with early-stage attack techniques.

## Cloud Security Insight

- Host-based reconnaissance does not always generate immediate alerts
- Microsoft Defender for Cloud evaluates behavior over time
- Alert generation may be delayed or suppressed in low-risk scenarios. Below you can see sample alerts that can be generated to visualize what they may look like. From there - actions can be taken to secure your environment.

<img width="2479" height="1160" alt="image" src="https://github.com/user-attachments/assets/3bbe870a-87d0-4adf-a888-60347668b487" />

This reflects real-world cloud security operations, where detection is **contextual and telemetry-driven rather than event-based**.

---

## Why This Matters for Cloud Roles

This lab demonstrates the following core cloud competencies:

- Secure infrastructure deployment
- Cost-aware cloud design
- Integration of native cloud security tooling
- Understanding of cloud detection mechanics
- Operational realism, including alert latency and environment baselining

These skills are fundamental for modern cloud-focused roles such as **Cloud Engineer, Cloud Security Engineer, DevOps, and SRE**.

### Linux Command to SSH from an outside VM into the Azure VM
---
```bash
ssh <username>@<public-ip>

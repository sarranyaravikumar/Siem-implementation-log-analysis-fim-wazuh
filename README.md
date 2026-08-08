#  Security Information and Event Management (SIEM) System with File Integrity Monitoring Using Wazuh

## 📌 Overview

This project implements a real-time Security Information and Event Management (SIEM) system using Wazuh with File Integrity Monitoring (FIM).

The Wazuh Manager is deployed on Ubuntu 22.04.5 LTS, while a Windows system is configured with the Wazuh Agent. The agent collects Windows system and security events and sends them to the Wazuh Manager for centralized analysis.

File Integrity Monitoring is configured to detect file creation, modification, and deletion activities on the Windows endpoint. The collected events and security alerts are visualized through the Wazuh Dashboard.

This project was implemented as a small-scale cybersecurity laboratory environment using Oracle VirtualBox.

---

## 🎯 Objectives

- Deploy and configure the Wazuh Manager on Ubuntu.
- Install and register the Wazuh Agent on a Windows endpoint.
- Collect and analyze Windows security and system events.
- Implement File Integrity Monitoring (FIM).
- Detect file creation, modification, and deletion.
- Generate security alerts.
- Provide centralized visualization through the Wazuh Dashboard.

---
## Components
Component	Role
Ubuntu 22.04.5 LTS	Wazuh Manager
Windows	Monitored Endpoint
Wazuh Agent 4.14.7	Endpoint monitoring
Wazuh Dashboard	Visualization and alert analysis
Oracle VirtualBox	Virtualization platform

The project architecture follows:

Windows Endpoint → Wazuh Agent → Wazuh Manager → Event Processing → Rule Engine → Alerts / Dashboard / Log Storage

## 🛠️ Technologies Used
Wazuh
Ubuntu 22.04.5 LTS (Jammy Jellyfish)
Windows
Wazuh Agent 4.14.7
Oracle VirtualBox
File Integrity Monitoring (FIM)
SIEM
Linux Command Line
PowerShell


## 📚 Learn

This project includes step-by-step learning materials covering SIEM concepts, Wazuh architecture, implementation, File Integrity Monitoring, and project results.

| Module | Topic |
|--------|-------|
| [00 - Overview](./learn/00-OVERVIEW.md) | Project overview, prerequisites, objectives, and quick start |
| [01 - Concepts](./learn/01-CONCEPTS.md) | SIEM, Wazuh, security events, agents, managers, and File Integrity Monitoring concepts |
| [02 - Architecture](./learn/02-ARCHITECTURE.md) | Wazuh Manager, Windows Agent, communication flow, and system architecture |
| [03 - Implementation](./learn/03-IMPLEMENTATION.md) | Wazuh installation, Windows Agent configuration, agent registration, and FIM configuration |
| [04 - Results](./learn/04-RESULTS.md) | FIM testing, detected events, dashboard verification, and project results |

## ⚙️ Project Workflow
1. Wazuh Manager Deployment

Wazuh Manager was installed and configured on an Ubuntu 22.04.5 LTS virtual machine, including the repository, GPG key, required components, and services.

2. Wazuh Dashboard Configuration

The Wazuh Dashboard was accessed through a web browser to monitor agents, security events, alerts, and FIM events.

3. Windows Agent Deployment

The Wazuh Agent was installed on the Windows endpoint, configured with the Ubuntu Manager IP, and registered successfully.

4. Agent Verification

The Windows Agent connection was verified through the Wazuh Dashboard, allowing system and security events to be monitored.

5. File Integrity Monitoring

FIM was configured on a selected Windows directory to detect file creation, modification, deletion, and other integrity changes.

6. FIM Testing

FIM was tested by creating, modifying, and deleting files in the monitored directory. The events were collected by the agent and sent to the manager.

7. Alert Verification

The generated security and FIM events were verified and analyzed through the Wazuh Dashboard.

## 📊 Wazuh Dashboard
<img width="1282" height="807" alt="wazuh manager" src="https://github.com/user-attachments/assets/40d2162e-cfda-43e5-acfa-dddfd39b7885" />



## 🔒 Security Benefits
Centralized collection and analysis of endpoint security information.
Real-time visibility into monitored file changes.
Faster identification of potentially unauthorized file activity.
Open-source and cost-effective security monitoring.
Dashboard-based visualization for easier investigation of events and alerts.

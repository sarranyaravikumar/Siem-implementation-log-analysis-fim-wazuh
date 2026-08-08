# A Real-Time Security Information and Event Management (SIEM) System with File Integrity Monitoring Using Wazuh

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

## 🏗️ Architecture

```text
┌─────────────────────────┐
│    Windows Endpoint     │
│                         │
│ Windows Logs & Events   │
│ File Integrity Changes  │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│      Wazuh Agent        │
│                         │
│ Log Collection          │
│ FIM Monitoring          │
└────────────┬────────────┘
             │
             │ Secure Communication
             ▼
┌─────────────────────────┐
│    Ubuntu Server        │
│     Wazuh Manager       │
│                         │
│ Event Processing        │
│ Event Analysis          │
│ Rule Engine             │
│ Alerting                │
└────────────┬────────────┘
             │
      ┌──────┼──────┐
      ▼      ▼      ▼
   Logs    Alerts Dashboard
   Storage          │
                   ▼
              Visualization
Components
Component	Role
Ubuntu 22.04.5 LTS	Wazuh Manager
Windows	Monitored Endpoint
Wazuh Agent 4.14.7	Endpoint monitoring
Wazuh Dashboard	Visualization and alert analysis
Oracle VirtualBox	Virtualization platform

The project architecture follows:

Windows Endpoint → Wazuh Agent → Wazuh Manager → Event Processing → Rule Engine → Alerts / Dashboard / Log Storage

🛠️ Technologies Used
Wazuh
Ubuntu 22.04.5 LTS (Jammy Jellyfish)
Windows
Wazuh Agent 4.14.7
Oracle VirtualBox
File Integrity Monitoring (FIM)
SIEM
Linux Command Line
PowerShell

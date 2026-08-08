# 02 - Architecture

## System Architecture

```text
Windows Endpoint
       |
       | Wazuh Agent
       |
       | Logs + FIM Events
       v
Ubuntu Server
Wazuh Manager
       |
       | Event Processing
       v
Security Alerts
       |
       v
Wazuh Dashboard

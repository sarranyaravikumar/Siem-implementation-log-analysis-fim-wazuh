
#### `03-IMPLEMENTATION.md`

```markdown
# 03 - Implementation

## 1. Wazuh Manager Installation

The Wazuh Manager was installed on Ubuntu 22.04.5 LTS.

The implementation included:

- Preparing the Ubuntu environment
- Adding the Wazuh GPG key
- Downloading the Wazuh installation assistant
- Installing the Wazuh components
- Verifying the installation
- Accessing the Wazuh Dashboard

Detailed installation commands are available in:

`Wazuh-SIEM-FIM-Documentation.pdf`

## 2. Windows Agent Installation

The Wazuh Agent 4.14.7 was installed on the Windows endpoint.

The agent was configured with the IP address of the Ubuntu Wazuh Manager.

## 3. Agent Registration

The Windows Agent was registered with the Wazuh Manager using the Wazuh agent management utility.

After registration, the agent was started and its connection was verified.

## 4. File Integrity Monitoring

A directory on the Windows endpoint was selected for monitoring.

The Wazuh Agent configuration was updated to enable real-time monitoring of the selected directory.

## 5. Agent Restart

After updating the configuration, the Wazuh Agent service was restarted so that the FIM configuration could take effect.

## 6. Testing

The following activities were performed:

- File creation
- File modification
- File deletion

The resulting events were checked through the Wazuh Dashboard.

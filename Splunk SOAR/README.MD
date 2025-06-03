# Splunk SOAR Playbooks

This directory contains playbooks designed to automate the closure of ASM Issues and DTM Alerts on the Google Threat Intelligence platform when a container is closed in Splunk SOAR. It also includes an example playbook for working with IOC stream artifacts.

## Playbooks

### 1. Close DTM Alerts

This playbook automatically closes DTM alerts on the Google Threat Intelligence platform when a container is closed in Splunk SOAR.

**Note:** This playbook only triggers when a container is closed.

---

### 2. Close ASM Issues

This playbook automatically closes ASM issues on the Google Threat Intelligence platform when a container is closed in Splunk SOAR.

**Note:** This playbook only triggers when a container is closed.

_See [Basic Playbook Configuration in Splunk SOAR](#basic-playbook-configuration-in-splunk-soar) for setup instructions._

---

### Basic Playbook Configuration in Splunk SOAR

_The following configuration steps apply to both the **Close DTM Alerts** and **Close ASM Issues** playbooks:_

After importing the playbook (tgz), make sure to:

1. **Select the Asset:**
    - In the playbook editor, locate the action block (`update dtm alert status` or `update asm issue status`).
    - Click on the action block.
    - Under **Asset**, select the asset configured for the Google Threat Intelligence platform.

2. **Configure the Label:**
    - In the top-right corner of the playbook editor, click **Settings**.
    - Locate the field **Operates on**.
    - Select the label assigned to the containers/events where DTM or ASM events are ingested.
    - This ensures the playbook runs only on relevant events.

3. **Mark as Active:**
    - In the playbook settings, toggle the **Active** switch to enable the playbook so it can be triggered automatically.

---

### 3. Example Playbook: Extract IOC from IOC Stream and Run Action

This example playbook demonstrates how to extract Indicators of Compromise (IOCs) from a single artifact in an IOC stream and take actions based on the extracted IOCs.

In this example, the playbook is triggered on an IOC Stream container with a specific artifact. It uses the **get ioc report** action from the Google Threat Intelligence integration for the corresponding IOC.

**Note:** This is just an example demonstrating how to extract an IOC from a single artifact using a playbook.

---

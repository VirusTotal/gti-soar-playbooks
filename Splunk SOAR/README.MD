# Splunk SOAR Playbooks

This directory contains playbooks designed to automate security operations with Google Threat Intelligence platform on Splunk SOAR.

---

## Playbooks Overview

### 1. Close DTM Alerts

This playbook automatically closes DTM alerts on the Google Threat Intelligence platform when a container is closed in Splunk SOAR.

### 2. Close ASM Issues

This playbook automatically closes ASM issues on the Google Threat Intelligence platform when a container is closed in Splunk SOAR.

### 3. Vulnerability Enrichment and Ticket Creation

This playbook enriches CVE artifacts using Google Threat Intelligence and creates a ServiceNow ticket when the vulnerability presents a significant risk.

### 4. IOC Enrichment Orchestrator

This automation playbook extracts IOC values from incoming artifacts and orchestrates enrichment by invoking the input playbook [IOC Enrichment and Blocking](#5.IOC Enrichment and Blocking).

### 5.IOC Enrichment and Blocking

This playbook enriches a single IOC using Google Threat Intelligence and determines whether it is malicious based on verdict and threat score.

### 6. Phishing Triage and Response

This automation playbook extracts email addresses and domains from artifacts and orchestrates domain enrichment by invoking the input playbook [Phishing Domain Enrichment](#6.Phishing Domain Enrichment).

### 7. Phishing Domain Enrichment

This input playbook enriches a phishing-related domain using Google Threat Intelligence and applies response actions when the domain is malicious.

### 8. DTM Alert Incident Response

This playbook evaluates the severity of Google Threat Intelligence DTM alerts and automatically escalates high-severity events by creating a ServiceNow incident.

### 9. ASM Alert Incident Response

This playbook evaluates the severity of Google Threat Intelligence ASM alerts and automatically escalates high-severity events by creating a ServiceNow incident.

### 10. IOCs Curated Threat Intelligence Enrichment

This playbook enriches IOCs using Google Threat Intelligence curated associations to provide analyst-verified threat context and relationships.

### 11. Scan Private File

This playbook performs a private scan of a URL using Google Threat Intelligence, evaluates the scan result, and applies enforcement and documentation based on maliciousness.

### 12. Scan Private URL

This playbook performs a private scan of a URL using Google Threat Intelligence, evaluates the scan result, and applies enforcement and documentation based on maliciousness.

### 13. Close RS Alert

This playbook automatically updates the status of the an RS alert to **Resolved** on the Google Threat Intelligence platform when a container is closed in Splunk SOAR.




---

_See [Basic Playbook Configuration in Splunk SOAR](#basic-playbook-configuration-in-splunk-soar) for setup instructions._

---

## Playbooks Configuration

### Basic Playbook Configuration in Splunk SOAR

The following configuration steps apply to all playbooks, with notes for specific ones.

After importing the playbook (tgz), make sure to:

1. **Select the Asset:**
    - In the playbook editor, locate the action block (e.g. `Get Vulnerability Report`,  `update dtm alert status`).
    - Click on the action block.
    - Under **Asset**, select the asset configured for the Google Threat Intelligence platform.

2. **Configure the Label:**
    - In the top-right corner of the playbook editor, click **Settings**.
    - Locate the field **Operates on**.
    - Select the specific label assigned to the containers/events where GTI events are ingested.
    - This ensures the playbook runs only on relevant events.

3. **Mark as Active:**
    - For the automation playbooks, In the settings, toggle the **Active** switch to enable the playbook so it can be triggered automatically.


### Configuration Notes Specific to Playbook


1. **Vulnerability Enrichment and Ticket Creation**
   - In the playbook editor, configure the `Create SNow Ticket` action to enable automatic ticket creation.

2. **IOC Enrichment and Blocking** 
   - For blocking of IPs, URLs, and domains, configure the Block action with a valid Zscaler asset, as Zscaler is currently used for enforcement.
   - For malicious FileHash it is creating ServiceNow Ticket, so configure the `Create SNow Ticket` action.

3. **DTM Alert Incident Response**
   - In the playbook editor, configure the `Create SNow Ticket` action to enable automatic ticket creation.

4. **ASM Alert Incident Response**
   - In the playbook editor, configure the `Create SNow Ticket` action to enable automatic ticket creation.

5. **Scan Private File** 
   - In the playbook editor, configure the `Create SNow Ticket` action to enable automatic ticket creation.

6. **Scan Private URl**
   - For blocking of  URL, configure the Block action with a valid Zscaler asset, as Zscaler is currently used for enforcement.

---

## Notes  
- For **automated playbooks**, confirm trigger conditions (e.g., artifact creation).  
- For **manual execution**, ensure correct event label assignment.  
- Use **SOAR debug logs** for troubleshooting failures.  


---

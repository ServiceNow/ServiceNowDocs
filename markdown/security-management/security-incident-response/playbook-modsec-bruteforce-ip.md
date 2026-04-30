---
title: Playbook for ModSec Brute force by IP Burst
description: This playbook provides systematic remediation steps to investigate incidents of brute force attempts on the login pages from multiple IPs detected by ModSec. The event conditions could be set at the ModSec policy itself and will raise an alert at Splunk when the event is created at ModSec.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for ModSec Brute force by IP Burst

This playbook provides systematic remediation steps to investigate incidents of brute force attempts on the login pages from multiple IPs detected by ModSec. The event conditions could be set at the ModSec policy itself and will raise an alert at Splunk when the event is created at ModSec.

This playbook helps in detecting abnormal traffic counts on the login page. In this example, two successive bursts of more than 50 hits/minute should be from an IP to the login page, which indicates a brute-force attempt to log in.

-   **[Set up the ModSec Brute force by IP Burst playbook](../task/playbook-setup-modsec-bruteforce.md)**  
Use the following steps to set up the ModSec Brute force by IP Burst playbook.
-   **[Use the ModSec Brute force by IP Burst playbook](../task/using-modsec-bruteforce-ip-playbook.md)**  
Use this playbook to investigate incidents of brute force attempts on the login pages from multiple IPs detected by ModSec. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the ModSec Brute force by IP Burst playbook.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)


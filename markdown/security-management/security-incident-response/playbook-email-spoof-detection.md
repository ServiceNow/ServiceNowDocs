---
title: Playbook for Email Domain Spoofing Detection
description: This playbook helps with the early stage triage of user-reported phishing submissions by alerting the analyst to the possibility of a look-alike domain in the Phisher's email address.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Email Domain Spoofing Detection

This playbook helps with the early stage triage of user-reported phishing submissions by alerting the analyst to the possibility of a look-alike domain in the Phisher's email address.

The Email Domain Spoofing Detection playbook looks to find a similarity match between the Phisher's sender email domain with a trusted domain name exists in the observable repository. When a spoofed sender email domain match has been identified by the playbook, the analysts are alerted with a tag.

The workflow is created based on an existing playbook, which provides a consistent and efficient approach for incident investigation. Each decision point in the playbook has been converted into an outcome driven task and flow changes direction based on the outcome of such tasks.

-   **[Set up the Email Spoof Detection playbook](../task/playbook-setup-email-spoof-detection.md)**  
Use the following steps to set up the Email Spoof Detection playbook.
-   **[Use the Email Domain Spoofing Detection playbook](../task/playbook-using-email-spoof-detection.md)**  
Use this playbook to find a similarity match between the Phisher's sender email domain with a trusted domain name exists in the observable repository. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Email Domain Spoofing Detection playbook.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)


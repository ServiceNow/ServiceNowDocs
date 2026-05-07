---
title: Playbook for Attempted Access to Deactivated Accounts
description: This playbook triggers when an employee whose account is terminated, disabled, or separated attempts to log in with their credentials. User’s identity state in Sail point generally gets updated to disabled on their termination date.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Attempted Access to Deactivated Accounts

This playbook triggers when an employee whose account is terminated, disabled, or separated attempts to log in with their credentials. User’s identity state in Sail point generally gets updated to disabled on their termination date.

30 days is the ideal time from the termination date for it to get updated to a separated state. You can use business logic in Sail point to delete the RSA accounts and remove the Active Directory \(AD\) group memberships after 30 days.

-   **[Set up the Attempted Access Deactivated Account playbook](../task/playbook-setup-attempted-access-deactivated-accounts.md)**  
Use the following steps to set up the Attempted Access Deactivated Account playbook.
-   **[Use the Attempted Access to Deactivated Accounts playbook](../task/playbook-using-attempted-access-deactivated-accounts.md)**  
Use this playbook when an employee whose account is terminated, inactive, or separated attempts to log in with their credentials. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Attempted Access to Deactivated Accounts playbook.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)


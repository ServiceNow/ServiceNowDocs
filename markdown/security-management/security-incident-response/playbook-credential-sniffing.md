---
title: Playbook for Credential Sniffing
description: This playbook provides system remediation steps to investigate an incident involving credential sniffing activities performed through the sys\_installation\_exit table in a ServiceNow instance.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Credential Sniffing

This playbook provides system remediation steps to investigate an incident involving credential sniffing activities performed through the **sys\_installation\_exit** table in a ServiceNow instance.

The Credential Sniffing playbook provides a script field to process the Database \(DB\) logins, Single sign-on \(SSO\), and LDAP \(Lightweight Directory Access Protocol\) by using the records on the **sys\_installation\_exit** table. These privileged scripting fields enable listening of user requests and parameters to the instances during login, including user credentials such as username and password.

A malicious user may create a script to listen to the user requests and log these requests on the instance. The **sys\_installation\_exit** table on an instance defines the rules of processing the login and logout activities of all users on that instance.

-   **[Set up the Credential Sniffing playbook](../task/playbook-setup-credential-sniffing.md)**  
Use the following steps to set up the Credential Sniffing playbook.
-   **[Use the Credential Sniffing playbook](../task/playbook-using-credential-sniffing.md)**  
Use this playbook to investigate an incident involving credential sniffing activities performed through the **sys\_installation\_exit** table in a ServiceNow instance. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Credential Sniffing playbook.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)


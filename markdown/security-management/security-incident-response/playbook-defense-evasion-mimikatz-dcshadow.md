---
title: Playbook for T1003 - Defense Evasion - Mimikatz DCShadow
description: This playbook provides systematic remediation steps to investigate incidents suspected to be caused by Mimikatz DCShadow. DCShadow is a feature in Mimikatz that simulates the behavior of a Domain Controller \(a server controlling Active Directory\) to inject its own data, bypassing most of the standard security controls \(including SIEMs\).
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for T1003 - Defense Evasion - Mimikatz DCShadow

This playbook provides systematic remediation steps to investigate incidents suspected to be caused by Mimikatz DCShadow. DCShadow is a feature in Mimikatz that simulates the behavior of a Domain Controller \(a server controlling Active Directory\) to inject its own data, bypassing most of the standard security controls \(including SIEMs\).

Mimikatz DCShadow helps the attacker establish a rogue Domain Controller \(DC\) that becomes part of the Active Directory \(AD\). Once registered, it can act as a legitimate DC and cause damage.

-   **[Set up the T1003 - Defense Evasion - Mimikatz DCShadow playbook](../task/playbook-setup-defense-evasion-mimikatz-dcshadow.md)**  
Use the following steps to set up the T1003 - Defense Evasion - Mimikatz DCShadow playbook.
-   **[Use the T1003 - Defense Evasion - Mimikatz DCShadow playbook](../task/playbook-using-defense-evasion-mimikatz-dcshadow.md)**  
Use this playbook to investigate security incidents suspected to be caused by Mimikatz DCShadow. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Defense Evasion - Mimikatz DCShadow playbook.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)


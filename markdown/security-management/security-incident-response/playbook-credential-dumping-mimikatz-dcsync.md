---
title: Playbook for T1003 - Credential Dumping - Mimikatz DCSync
description: This playbook provides systematic remediation steps to investigate incidents suspected to be caused by Mimikatz DCSync. This playbook triggers when one of the Mimikatz functions \(lsadump::dcsync\) is used. The function is typically used on attacked Domain Controllers \(DC\).
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for T1003 - Credential Dumping - Mimikatz DCSync

This playbook provides systematic remediation steps to investigate incidents suspected to be caused by Mimikatz DCSync. This playbook triggers when one of the Mimikatz functions `(lsadump::dcsync`\) is used. The function is typically used on attacked Domain Controllers \(DC\).

Mimikatz is a popular hacking tool that enables users to issue commands that help retrieve confidential data from the attacked system. The confidential data includes passwords, their hashes, and others.

**Note:** This is a high-fidelity alert, which is assumed to be rarely triggered. When it triggers, you should notify a senior team member or Manager immediately.

-   **[Set up the T1003 - Credential Dumping - Mimikatz DCsync playbook](../task/playbook-setup-credential-dumping-mimikatz-dcsync.md)**  
Use the following steps to set up the T1003 - Credential Dumping - Mimikatz DCsync playbook.
-   **[Use the T1003 - Credential Dumping - Mimikatz DCsync playbook](../task/playbook-using-credential-dumping-mimikatz-dcsync.md)**  
Use this playbook to investigate incidents suspected to be caused by Mimikatz DCSync. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Credential Dumping - Mimikatz DCsync playbook.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)


---
title: Use the T1003 - Defense Evasion - Mimikatz DCShadow playbook
description: Use this playbook to investigate security incidents suspected to be caused by Mimikatz DCShadow. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Defense Evasion - Mimikatz DCShadow playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for T1003 - Defense Evasion - Mimikatz DCShadow, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the T1003 - Defense Evasion - Mimikatz DCShadow playbook

Use this playbook to investigate security incidents suspected to be caused by Mimikatz DCShadow. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Defense Evasion - Mimikatz DCShadow playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, find out which account is responsible for the creation of the new DC \(Domain Controller\).

2.  In Action 2, reach out to the user to validate the business justification.

    You can use the provided email template to contact the user.

3.  In Action 3, check whether the user provided a valid business justification.

4.  In Action 4, if the user provided a valid business justification, perform the following steps:

    ![Response task to check whether the user provided a valid business justification](../image/playbook-mimikatz-dcshadow-overview.png "T1003 - Defense Evasion - Mimikatz DCShadow playbook")

    1.  In Action 5, document the findings so far.

    2.  In Action 6, initiate a post incident review.

        In Action 7, after the post incident review, the flow ends.

5.  In Action 8, if the user didn’t provide a valid business justification, perform the following steps:

    ![Response tasks when the user didn't provide a valid business justification.](../image/playbook-mimikatz-dcshadow-investigate.png "Using the T1003 - Defense Evasion - Mimikatz DCShadow playbook")

    1.  In Action 9, lock down or quarantine all the accounts, computers, and other devices involved.

    2.  In Action 10, perform a forensic investigation on the locked-down accounts and identify if any data has been exfiltrated or any malicious code has been injected.

    3.  In Action 11, reimage the affected resources.

    4.  In Action 12, lift containment and bring systems back to operational standards.

    5.  In Action 13, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for T1003 - Defense Evasion - Mimikatz DCShadow](../concept/playbook-defense-evasion-mimikatz-dcshadow.md)


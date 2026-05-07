---
title: Use the T1003 - Credential Dumping - Mimikatz DCsync playbook
description: Use this playbook to investigate incidents suspected to be caused by Mimikatz DCSync. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Credential Dumping - Mimikatz DCsync playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for T1003 - Credential Dumping - Mimikatz DCSync, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the T1003 - Credential Dumping - Mimikatz DCsync playbook

Use this playbook to investigate incidents suspected to be caused by Mimikatz DCSync. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Credential Dumping - Mimikatz DCsync playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, check the host activity on Splunk and look for any suspicious activities.

2.  In Action 2, identify the owner of the server/endpoint/VM.

    If the user is online, run the CrowdStrike EDR to gather a better scope of the system's activities.

3.  In Action 3, gather information on the user's other account activities.

4.  In Action 4, based on the investigation, verify if the server/endpoint/VM was ever used for credential dumping.

5.  In Action 5, if the server/endpoint/VM wasn’t used for credential dumping, perform the following actions:

    1.  In Action 6, update the alert query if necessary.

    2.  In Action 7, update the allow list if necessary.

    3.  In Action 8, document the findings so far.

    4.  In Action 9, initiate a post incident review.

        In Action 10, the flow ends.

6.  If the server/endpoint/VM was used for credential dumping, then in Action 11, reach out the user.

7.  In Action 12, reach out to the user to validate the business justification.

8.  In Action 13, if the user provided a valid business justification, perform the following Actions:

    1.  In Action 14, document the findings so far.

    2.  In Action 15, initiate a post incident review.

        In Action 16, the flow ends.

9.  If the user didn't provide a valid business justification, then in Action 17, quarantine the system.

10. In Action 18, remove any unwanted files that may have been created or deleted by the rogue accounts.

11. In Action 19, lift containment and bring systems back to operational standards.

12. In Action 20, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for T1003 - Credential Dumping - Mimikatz DCSync](../concept/playbook-credential-dumping-mimikatz-dcsync.md)


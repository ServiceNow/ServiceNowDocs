---
title: Use the T1003 - Detect Credential Dumping Tools playbook
description: Use this playbook to investigate an incident involving credential dumping activities. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Detect Credential Dumping Tools playbook.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Playbook for T1003 - Detect Credential Dumping Tools, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the T1003 - Detect Credential Dumping Tools playbook

Use this playbook to investigate an incident involving credential dumping activities. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1003 - Detect Credential Dumping Tools playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, you need to gather information on the user's account.

    -   You need to check the host activity to look for any suspicious activities.
    -   You need to identify the owner of the Server/Endpoint/VM and capture the data correlating to the tool.
    -   You need to gather information on the user's other accounts.
2.  In Action 2, you need to check whether this is a possible Acceptable Use Policy \(AUP\) violation case.

    You can do a peer review with the evidence gathered and consult with your regional Incident Manager whether to contact the user.

3.  In Action 3, if this is a case of Acceptable Use Policy \(AUP\) violation, then perform the following actions:

    1.  In Action 4, you need to update the security incident that this is a case of AUP violation

    2.  In Action 5, the flow ends.

4.  In Action 6, based on the investigation done so far, you need to check whether this is a possible case of insider threat or not.

    ![Response tasks to investigate if is this a possible case of insider threat.](../image/playbook-credential-dump-insider.png "T1003 - Detect Credential Dumping Tools playbook")

5.  In Action 7, if this is a case of insider threat, perform the following actions:

    1.  In Action 8, you need to contact IT support and request an account freeze.

    2.  In Action 9, you need to block malicious IPs.

    3.  In Action 10, you need to contact internal employees through an email.

        You can use the provided email template to contact your internal employees.

    4.  In Action 11, you need to lift the containment and bring the systems back to operational standards.

        The flow ends.

        ![Response tasks to lift the containment and bring systems back to operational standards.](../image/playbook-credential-dump-contain.png "Response tasks to lift the containment")

6.  In Action 12, if this isn't a case of insider threat, then in Action 13, you need to perform a peer review to determine if this needs to be added to the exclusion list.

    The flow ends.

7.  In Action 14, a response task is created to complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for T1003 - Detect Credential Dumping Tools](../concept/playbook-detect-credential-dumping-tools.md)


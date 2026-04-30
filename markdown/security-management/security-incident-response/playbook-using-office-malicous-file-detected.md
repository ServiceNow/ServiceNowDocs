---
title: Use the Office 365 Malicious File Detected playbook
description: Use this playbook to investigate malicious files detected in Office 365. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Office 365 Malicious File Detected playbook.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Playbook for Office 365 - Malicious File Detected, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Office 365 Malicious File Detected playbook

Use this playbook to investigate malicious files detected in Office 365. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Office 365 Malicious File Detected playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, you need to extract the malicious file from the Office 365 console.

2.  In Action 2, you need to analyze whether the file or hash has been added as an observable in the Threat Intel Platform.

3.  In Action 3, you need to investigate the file name and path to determine whether it is a known or non-malicious file/application.

    ![Response tasks to determine whether it is a known or non-malicious file/application.](../image/playbook-office365-investigate.png "Office 365 Malicious File Detected playbook")

4.  In Action 4, you need to submit the file to Sandbox for analyzing the results.

5.  In Action 5, based on the investigation done so far, you need to check whether the file or hash is malicious or not.

    If the file or hash isn’t malicious, a manual response task is created in Action 5 and the flow ends.

6.  In Action 6, if the file or hash is malicious, then Actions 7 and 8 are executed.

7.  In Action 7, you need to reach out to the end user for a valid business justification as to why they have a malicious file on the device.

    If the file or hash is malicious, you can use the pre-existing Email Template in the playbook to email the end user asking for clarification.

8.  In Action 8, you need to check whether the end user provided a valid business justification or not.

    If the end user provided a valid business justification, a manual response task is created in Action 5 and the flow ends.

9.  In Action 9, if the user didn’t provide a valid business justification then Actions 10, 11, and 12 are executed.

    ![Response tasks if there was no valid business justification for the malicious file](../image/playbook-office365-justification.png "Business justification for the malicious file")

10. In Action 10, since there was no valid business justification, you can forward the malicious file or hash to the Threat Intel Team for review.

11. In Action 11, you need to run the Malware bytes scanner script to check if the file or hash is malicious.

12. In Action 12, you need to perform a Forensic Analysis to check if the file or hash is malicious.

13. In Action 13, a response task is created for the user to complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Office 365 - Malicious File Detected](../concept/playbook-office-malicious-file-detected-.md)

**Related topics**  


[Set up the Office Malicous File Detected playbook](playbook-setup-office-malicous-file-detected.md)


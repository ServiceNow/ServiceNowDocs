---
title: Set up the Office Malicous File Detected playbook
description: Use the following steps to set up the Office Malicous File Detected playbook.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbook for Office 365 - Malicious File Detected, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Office Malicous File Detected playbook

Use the following steps to set up the Office Malicous File Detected playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Office 365 - Malicious File Detected** playbook.

3.  You can create a copy of the Office 365 - Malicious File Detected playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, click the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Office 365 - Malicious File Detected playbook](../image/playbook-office365.png "Office 365 - Malicious File Detected playbook")

4.  Activate the playbooks.

    -   Activate the main flow to use the playbook available in the base system.
    -   Activate the copied flows after making the required changes.
5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the **Category** is **Malicious code activity**.

    ![Trigger condition for Office 365 - Malicious File Detected playbook.](../image/playbook-office365-trigger.png)


**Parent Topic:**[Playbook for Office 365 - Malicious File Detected](../concept/playbook-office-malicious-file-detected-.md)

**Related topics**  


[Use the Office 365 Malicious File Detected playbook](playbook-using-office-malicous-file-detected.md)


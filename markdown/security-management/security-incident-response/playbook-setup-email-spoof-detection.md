---
title: Set up the Email Spoof Detection playbook
description: Use the following steps to set up the Email Spoof Detection playbook.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook for Email Domain Spoofing Detection, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Email Spoof Detection playbook

Use the following steps to set up the Email Spoof Detection playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Email Domain Spoofing Detection playbook** playbook.

3.  You can create a copy of the Email Domain Spoofing Detection playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, click the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Email Domain Spoofing Detection playbook](../image/playbook-email-spoof-detect.png "Email Domain Spoofing Detection playbook")

4.  Activate the playbooks.

    -   Activate the main flow to use the playbook available in the base system.
    -   Activate the copied flows after making the required changes.
5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the following conditions are met:

    -   **From** is not **empty**.
    -   **Security incident** is not **empty**.
    ![Trigger condition for Email Domain Spoofing Detection playbook.](../image/playbook-email-spoof-detect-trigger.png)


**Parent Topic:**[Playbook for Email Domain Spoofing Detection](../concept/playbook-email-spoof-detection.md)


---
title: Set up the Spoofed Emails playbook
description: Use the following steps to set up the Spoofed Emails playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for Spoofed Emails \(using the same Display name\), Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Spoofed Emails playbook

Use the following steps to set up the Spoofed Emails playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Spoofed Emails \(using the same Display name\)** playbook.

3.  You can create a copy of the Repeat Detection playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, click the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Spoofed Emails playbook](../image/playbook-spoofed-email-name.png "Spoofed Emails playbook")

4.  Activate the playbooks.

    -   Activate the main flow to use the playbook available in the base system.
    -   Activate the copied flows after making the required changes.
5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the **Category** is **Phishing**.

    ![Trigger condition for Spoofed Emails playbook.](../image/playbook-spoofed-email-name-trigger.png)


**Parent Topic:**[Playbook for Spoofed Emails \(using the same Display name\)](../concept/playbook-spoofed-emails-display-name.md)


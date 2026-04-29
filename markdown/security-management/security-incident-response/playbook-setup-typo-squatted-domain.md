---
title: Set up the Typo Squatted Domain playbook
description: Use the following steps to set up the Typo Squatted Domain playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for Typo Squatted Domain, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Typo Squatted Domain playbook

Use the following steps to set up the Typo Squatted Domain playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Typo Squatted Domain** playbook.

3.  You can create a copy of the Typo Squatted Domain playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, click the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Typo Squatted Domain playbook](../image/playbook-typo-squatted.png "Typo Squatted Domain playbook")

4.  Activate the playbooks.

    -   Activate the main flow to use the playbook available in the base system.
    -   Activate the copied flows after making the required changes.
5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the following conditions are met:

    -   **Category** is **Phishing**.
    -   **Short description** contains **Typo Squatted Domain**.
    ![Trigger condition for Typo Squatted Domain playbook.](../image/playbook-typo-squatted-trigger.png)


**Parent Topic:**[Playbook for Typo Squatted Domain](../concept/playbook-typo-squatted-domain.md)


---
title: Set up the User Deleting Bash History playbook
description: Use the following steps to set up the User Deleting Bash History playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for User Deleting Bash History - Cloud, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the User Deleting Bash History playbook

Use the following steps to set up the User Deleting Bash History playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **User Deleting .bash\_history - Cloud** playbook.

3.  Create a copy of the User Deleting .bash\_history - Cloud playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the User Deleting Bash History - Cloud playbook.](../image/playbook-bash-history-overview.png "User Deleting Bash History - Cloud playbook")

4.  Activate the playbooks.

    1.  Activate the main flow to use the playbook available in the base system.

    2.  Activate the copied flows after making the required changes.

5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the **Category** is **Insider Breach**.

    ![Trigger condition for User Deleting Bash History playbook.](../image/playbook-bash-history-trigger.png "User Deleting Bash History - Cloud playbook trigger condition")


**Parent Topic:**[Playbook for User Deleting Bash History - Cloud](../concept/playbook-deleting-bash-history.md)


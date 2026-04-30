---
title: Set up the Attempted Access Deactivated Account playbook
description: Use the following steps to set up the Attempted Access Deactivated Account playbook.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook for Attempted Access to Deactivated Accounts, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Attempted Access Deactivated Account playbook

Use the following steps to set up the Attempted Access Deactivated Account playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Attempted Access Deactivated Account** playbook.

3.  Create a copy of the Attempted Access Deactivated Account playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Attempted Access to Deactivated Accounts playbook.](../image/playbook-attempted-access-deactivated-overview.png "Attempted Access to Deactivated Accounts playbook")

4.  Activate the playbooks.

    1.  Activate the main flow to use the playbook available in the base system.

    2.  Activate the copied flows after making the required changes.

5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered when the security incident is created or updated based on your required conditions. For example, when **Category** is **Insider Breach**

    ![Trigger condition for Attempted Access to Deactivated Accounts playbook.](../image/playbook-attempted-access-deactivated-trigger.png "Attempted Access to Deactivated Accounts playbook trigger condition")


**Parent Topic:**[Playbook for Attempted Access to Deactivated Accounts](../concept/playbook-attempted-access-deactivated-accounts.md)


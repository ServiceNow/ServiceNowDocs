---
title: Set up the OSquery of External Address in the /etc/hosts file playbook
description: Use the following steps to set up the OSquery of External Address in the /etc/hosts file playbook.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook for OSquery of External Address in /etc/hosts file, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the OSquery of External Address in the /etc/hosts file playbook

Use the following steps to set up the OSquery of External Address in the /etc/hosts file playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **OSquery External Address in /etc/hosts** playbook.

3.  Create a copy of the OSquery External Address in /etc/hosts playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the OSquery of External Address in /etc/hosts playbook.](../image/playbook-osquery-overview.png "OSquery of External Address in /etc/hosts playbook")

4.  Activate the playbooks.

    1.  Activate the main flow to use the playbook available in the base system.

    2.  Activate the copied flows after making the required changes.

5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the **Category** is **Insider Breach**.

    ![Trigger condition for OSquery of External Address in /etc/hosts playbook](../image/playbook-osquery-trigger.png "OSquery of External Address in /etc/hosts playbook trigger condition")


**Parent Topic:**[Playbook for OSquery of External Address in /etc/hosts file](../concept/playbook-osquery-external-address.md)


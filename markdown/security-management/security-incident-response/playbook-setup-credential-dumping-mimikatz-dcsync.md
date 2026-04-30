---
title: Set up the T1003 - Credential Dumping - Mimikatz DCsync playbook
description: Use the following steps to set up the T1003 - Credential Dumping - Mimikatz DCsync playbook.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbook for T1003 - Credential Dumping - Mimikatz DCSync, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the T1003 - Credential Dumping - Mimikatz DCsync playbook

Use the following steps to set up the T1003 - Credential Dumping - Mimikatz DCsync playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **T1003 - Credential Dumping - Mimikatz DCsync** playbook.

3.  Create a copy of the T1003 - Credential Dumping - Mimikatz DCsync playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the T1003 - Credential Dumping - Mimikatz DCSync playbook.](../image/playbook-mimikatz-dcsync-overview.png "T1003 - Credential Dumping - Mimikatz DCSync playbook")

4.  Activate the playbooks.

    1.  Activate the main flow to use the playbook available in the base system.

    2.  Activate the copied flows after making the required changes.

5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the **Category** is **Rogue server or service**.

    ![Trigger condition for T1003 - Credential Dumping - Mimikatz DCSync playbook.](../image/playbook-mimikatz-dcsync-trigger.png "T1003 - Credential Dumping - Mimikatz DCSync playbook trigger condition")


**Parent Topic:**[Playbook for T1003 - Credential Dumping - Mimikatz DCSync](../concept/playbook-credential-dumping-mimikatz-dcsync.md)


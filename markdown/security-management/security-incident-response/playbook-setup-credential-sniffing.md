---
title: Set up the Credential Sniffing playbook
description: Use the following steps to set up the Credential Sniffing playbook.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Playbook for Credential Sniffing, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Credential Sniffing playbook

Use the following steps to set up the Credential Sniffing playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Credential Sniffing** playbook.

3.  Create a copy of the Credential Sniffing playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Credential Sniffing playbook.](../../secops-analyst-workspace/image/playbook-credential-sniff-investigate.png "Credential Sniffing Playbook")

4.  Activate the playbooks.

    1.  Activate the main flow to use the playbook available in the base system.

    2.  Activate the copied flows after making the required changes.

5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the **Category** is **Malicious code activity**.

    ![Trigger condition for Credential Sniffing playbook](../../secops-analyst-workspace/image/playbook-credential-sniff.png "Credential Sniffing Playbook trigger condition")


**Parent Topic:**[Playbook for Credential Sniffing](../concept/playbook-credential-sniffing.md)


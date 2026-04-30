---
title: Set up the Okta User Login Failures from Multiple IPs playbook
description: Use the following steps to set up the Okta User Login Failures from Multiple IPs playbook.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbook for Okta User Login Failures from Multiple IPs, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Okta User Login Failures from Multiple IPs playbook

Use the following steps to set up the Okta User Login Failures from Multiple IPs playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Okta User Login Failures from Multiple IPs** playbook.

3.  Create a copy of the Okta User Login Failures from Multiple IPs playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the ![More actions menu](../image/more-action-menu.png) icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

    ![Overview of the Okta User Login Failures from Multiple IPs playbook.](../image/playbook-okta-login-failures-ips-overview.png "Okta User Login Failures from Multiple IPs playbook")

4.  Activate the playbooks.

    1.  Activate the main flow to use the playbook available in the base system.

    2.  Activate the copied flows after making the required changes.

5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the **Category** is **Failed Login**.

    ![Trigger condition for Okta User Login Failures from Multiple IPs playbook.](../image/playbook-okta-login-failures-ips-trigger.png "Okta User Login Failures from Multiple IPs playbook trigger condition")


**Parent Topic:**[Playbook for Okta User Login Failures from Multiple IPs](../concept/playbook-okta-user-login-failures-ips.md)


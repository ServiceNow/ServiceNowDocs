---
title: Set up the Possible Password Spray playbook
description: Use the following steps to set up the Possible Password Spray playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/playbook-setup-possible-password-spray.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for Possible Password Spray, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Possible Password Spray playbook

Use the following steps to set up the Possible Password Spray playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Possible Password Spray** playbook.

3.  You can create a copy of the Possible Password Spray playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the \[Omitted image "more-action-menu.png"\] Alt text: More actions menu icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

4.  Activate the playbooks.

    -   Activate the main flow to use the playbook available in the base system.
    -   Activate the copied flows after making the required changes.
5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the following conditions are met:

    -   **Category** is **Unauthorized access**.
    -   **Sub-category** is **Brute force password cracking attempts**.

**Parent Topic:**[Playbook for Possible Password Spray](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/playbook-possible-password-spray.md)


---
title: Set up the Successful VPN Attempts from the Service Accounts playbook
description: Use the following steps to set up the Successful VPN Attempts from the Service Accounts playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/playbook-setup-successful-vpn-attempts.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for successful VPN attempts from service accounts, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Successful VPN Attempts from the Service Accounts playbook

Use the following steps to set up the Successful VPN Attempts from the Service Accounts playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  Login as a user with sn\_si.user and flow\_designer roles.

2.  Navigate to **All** &gt; **Flow Designer** and select the **Successful VPN Attempts from the Service Accounts** playbook.

3.  Create a copy of the Successful VPN Attempts from the Service Accounts playbook flow and make the necessary modifications.

    To create a copy of the playbook's flow, select the \[Omitted image "more-action-menu.png"\] Alt text: More actions menu icon and select **Copy flow**. Perform this step only if you plan to customize or make specific changes to the flow.

4.  Activate the playbooks.

    1.  Activate the main flow to use the playbook available in the base system.

    2.  Activate the copied flows after making the required changes.

5.  Set a **Trigger Condition** for the playbook.

    This playbook is triggered and associated with the security incident when the security incident is created or updated based on your required conditions. For example, when **Category** is **Insider Breach**.


**Parent Topic:**[Playbook for Successful VPN Attempts from the Service Accounts - Corp/Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/playbook-successful-vpn-attempts.md)


---
title: Use the Successful VPN Attempts from the Service Accounts playbook
description: Use this playbook to investigate incidents that track successful login attempts from service accounts through VPN. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Successful VPN Attempts from the Service Accounts playbook.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbook for successful VPN attempts from service accounts, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Successful VPN Attempts from the Service Accounts playbook

Use this playbook to investigate incidents that track successful login attempts from service accounts through VPN. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Successful VPN Attempts from the Service Accounts playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, raise the security incident to high priority and immediately notify your manager.

2.  In Action 2, reach out to the service account's owner to validate the business justification.

    You can use the provided email template to contact the service account's owner to validate the business justification.

3.  In Action 3, check whether the service account owner provided a valid business justification.

    ![Response task to check whether the service account owner provided a valid business justification.](../image/playbook-successful-vpn-attempts-overview.png "Successful VPN Attempts from the Service Accounts - Corp/Cloud playbook")

4.  In Action 4, if the service account owner provided a valid business justification, perform the following steps:

    1.  In Action 5, add the Source IP to the allow list if necessary.

    2.  In Action 6, document the findings so far.

    3.  In Action 7, initiate a post incident review.

        In Action 8, after the post incident review, the flow ends.

    ![Response task to check if the service account owner provided a valid business justification.](../image/playbook-successful-vpn-attempts-investigate.png "Using the Successful VPN Attempts from the Service Accounts - Corp/Cloud playbook")

5.  In Action 9, if the service account owner didn’t provide a valid business justification, perform the following steps:

    1.  In Action 10, temporarily lock the service account while the investigation occurs.

    2.  In Action 11, reset the passwords for the compromised service account.

    3.  In Action 12, check the logs for all kinds of activity the account could use.

        Look out for authentication logs like Active Directory logs, Audit logs, Okta logs, Office 365 logs, and so on.

    4.  In Action 13, find the machine certification details used to authenticate with the IT Support team's assistance.

    5.  In Action 14, lift containment and bring systems back to operational standards.

    6.  In Action 15, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Successful VPN Attempts from the Service Accounts - Corp/Cloud](../concept/playbook-successful-vpn-attempts.md)


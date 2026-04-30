---
title: Use the ModSec Brute force by IP Burst playbook
description: Use this playbook to investigate incidents of brute force attempts on the login pages from multiple IPs detected by ModSec. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the ModSec Brute force by IP Burst playbook.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Playbook for ModSec Brute force by IP Burst, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the ModSec Brute force by IP Burst playbook

Use this playbook to investigate incidents of brute force attempts on the login pages from multiple IPs detected by ModSec. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the ModSec Brute force by IP Burst playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1 check whether the Source IP belongs to a customer or to the organization's internal IP address.

2.  In Action 2, if the Source IP belongs to a customer or to the organization's internal IP address, perform the following steps:

    ![Response tasks if the Source IP belongs to a customer or the organization's internal IP address.](../image/playbook-modsec-bruteforce-overview.png "ModSec Brute force by IP Burst playbook")

    1.  In Action 3, check whether there were any suspicious activities.

        -   Check the activity from the source IP in the last few days. If the IP had negligible traffic, it indicates an actual attack.
        -   Check the spraying usernames. For example, check if the usernames are arranged in an alphabetic order.
        -   Look for generic account names involved. For example, admin, sysadmin, root, administrator, and other application account names.
        If there are no suspicious activities, then the flow ends.

    2.  In Action 4, if there were any suspicious activities, then in Action 5, check if the instance access history and the username look genuine.

        Check the **Appnode** logs for any indications of failure. There could be SAML, SSO, or LDAP fail events, which could be due to an operational issue.

        If the instance access history and the username don't look genuine, then the flow ends.

    3.  In Action 6, if the instance access history and the username look genuine, then perform the following steps:

        1.  In Action 7, coordinate with the appropriate team to fix the issue.
        2.  In Action 8, document the findings so far.
        3.  In Action 9, complete the post-incident review before closing the task.

            In Action 10, the flow ends.

3.  If the Source IP doesn't belong to a customer or the organization's internal IP address, then in Action 11, raise an IT Support ticket to block the source IPs.

    ![Response tasks if the Source IP doesn't belong to a customer or the organization's internal IP address.](../image/playbook-modsec-bruteforce-investigate.png "Using the ModSec Brute force by IP Burst playbook")

4.  In Action 12, reset the potentially compromised credentials.

5.  In Action 13, block the network access to compromised host systems.

6.  In Action 14, patch the affected devices.

7.  In Action 15, lift the containment and bring the systems back to operational standards.

8.  In Action 16, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for ModSec Brute force by IP Burst](../concept/playbook-modsec-bruteforce-ip.md)


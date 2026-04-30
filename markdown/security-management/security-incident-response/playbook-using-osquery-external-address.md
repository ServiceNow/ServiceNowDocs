---
title: Use the OSquery of External Address in the /etc/hosts file playbook
description: Use this playbook to investigate incidents that indicate that an internal hostname or domain has been assigned to an external IP address on the local DNS\(/etc/hosts\) of a Linux server. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the OSquery of external address in the /etc/hosts file playbook.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Playbook for OSquery of External Address in /etc/hosts file, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the OSquery of External Address in the /etc/hosts file playbook

Use this playbook to investigate incidents that indicate that an internal hostname or domain has been assigned to an external IP address on the local DNS\(/etc/hosts\) of a Linux server. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the OSquery of external address in the /etc/hosts file playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, identify the hostname or domain name corresponding to the external IP translation from the raw log.

2.  In Action 2, gather the details of the IP address and the hostname.

3.  In Action 3, check whether this IP address belongs to the internal organization's public/private IP range or not.

    ![Response task to check whether this IP address belongs to the internal organization's public/private IP range.](../image/playbook-osquery-overview.png "OSquery of External Address in /etc/hosts file playbook")

4.  In Action 4, if the IP address belongs to the internal organization's public/private IP range, perform the following steps:

    1.  In Action 5, document the findings so far.

    2.  In Action 6, initiate a post incident review.

        In Action 7, after the post incident review, the flow ends.

5.  If the IP address doesn’t belong to the internal organization's public/private IP range, then in Action 8, identify the user who logged in to the server during the alert timeframe.

6.  In Action 9, if the IP address seems suspicious, raise an IT ticket to the owner or the server's team to change the configuration as soon as possible.

7.  In Action 10, check whether there was any malicious activity on the server before and after adding the DNS entry.

8.  In Action 11, check for any connections to the external IP address from the server.

9.  In Action 12, document the findings so far.

10. In Action 13, check whether the owner or team information is available or not.

11. In Action 14, if the owner or team information is available, perform the following steps:

    1.  In Action 15, reach out to the owner or the server’s team to see if they recognize the activity.

        You can use the provided email template to contact the owner or the server's team.

    2.  In Action 16, check whether the owner or team provided a valid business justification or not.

    3.  In Action 17, if the owner or team provided didn’t provide a valid business justification, then the flow ends.

        But, if the owner or team provided a valid business justification, perform the following steps:

        1.  In Action 18, document the findings so far.
        2.  In Action 19, initiate a post incident review.

            In Action 20, after the post incident review, the flow ends.

        ![Response task to check whether the owner or team information is available.](../image/playbook-osquery-investigate.png "Using the OSquery of External Address in /etc/hosts file playbook")

12. In Action 21, if the owner or team information is unavailable, isolate the host system.

13. In Action 22, reset the potentially compromised credentials.

14. In Action 23, block the network access to the compromised host.

15. In Action 24, patch the affected devices.

16. In Action 25, lift containment and bring systems back to operational standards.

17. In Action 26, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for OSquery of External Address in /etc/hosts file](../concept/playbook-osquery-external-address.md)


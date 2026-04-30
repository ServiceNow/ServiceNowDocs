---
title: Use the Possible Password Spray playbook
description: Use this playbook to investigate password spray alerts triggered by multiple failed logins \(too many authentication failures from more than one IP address for the same user\). The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Possible Password Spray playbook.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Playbook for Possible Password Spray, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Possible Password Spray playbook

Use this playbook to investigate password spray alerts triggered by multiple failed logins \(too many authentication failures from more than one IP address for the same user\). The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Possible Password Spray playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, you need to check whether the activities are originating from the customer's IP address.

    Identify the IP addresses performing the Password Spray attack. For example, use the TXIDs \(Transaction IDs\) from the alert and look them up against the F5 logs.

2.  In Action 2, if the activities originated from the customer’s IP address, then perform the following actions:

    1.  In Action 3, you need to initiate a post-incident review of the Possible Password Spray attack.

    2.  In Action 4, the flow ends.

3.  In Action 5, if the activities didn't originate from the customer’s IP address then determine the attacker’s source IP from the alert details.

4.  In Action 6, you need to validate the IP reputation using Open-Source Intelligence \(OSINT\) tools and the traffic pattern from these IPs in the last seven days.

    ![Response tasks to validate the IP reputation using the OSINT tools.](../image/playbook-password-spray-ip.png "Possible Password Spray playbook")

5.  In Action 7, you need to identify the usernames that successfully logged in using the Password Spray attack.

6.  In Action 8, you need to identify the number of failed logins and patterns.

7.  In Action 9, you need to identify the indicators of true positive.

    -   Check the traffic from the source IPs in the last 60 days. No historic traffic can be an indication of a true positive.
    -   Check the username patterns having authentication failures and the count. The higher the count, the higher the probability that it’s a true positive.
    -   The username looks like a dictionary base \(starting from A to Z\) and might have common admin names like admin, sysadmin, root, and so on
    -   The same username might have different patterns in the spray attack like the same alert might have failures for john.doe, johnd, jdoe, john\_doe, jdoe7,etc., indicating attackers guessing the username pattern based on common use cases.
    -   Notice the User Agent and URIs from the F5 logs in the step above, and see if the IOCs are related to the Red Condor alerts. If they match, then it’s a true positive event.
8.  In Action 10, based on the investigation done so far, you need to check whether this is a case of Possible Password Spray attack or not.

9.  In Action 11, if this is case of Possible Password Spray attack, perform the following actions:

    1.  In Action 12, you need to coordinate with appropriate teams to lock out any necessary accounts and investigate malicious activity.

        ![Response tasks to lock out any necessary accounts and investigate malicious activity.](../image/playbook-password-spray-pattern.png "Possible Password Spray playbook")

    2.  In Action 13, you need to initiate a post-incident review of the Possible Password Spray attack.

    3.  In Action 14, the flow ends.

10. In Action 15, you need to check whether this isn’t a case of Possible Password Spray attack.

11. In Action 16, if this isn’t a case of Possible Password Spray attack, perform the following actions:

    1.  In Action 17, you need to document the findings so far.

    2.  In Action 18, you need to initiate a post-incident review of the Possible Password Spray attack.

    3.  In Action 19, the flow ends.

12. In Action 20, you need to consult with the peers and GIR manager for guidance.

13. In Action 21, a response task is created to complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Possible Password Spray](../concept/playbook-possible-password-spray.md)


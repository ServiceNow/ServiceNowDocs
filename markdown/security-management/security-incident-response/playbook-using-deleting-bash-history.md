---
title: Use the User Deleting Bash History playbook
description: Use this playbook to investigate incidents that indicate if someone was trying to remove the bash history file from a Linux server. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the User Deleting the Bash History \(.bash\_history\) playbook.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Playbook for User Deleting Bash History - Cloud, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the User Deleting Bash History playbook

Use this playbook to investigate incidents that indicate if someone was trying to remove the bash history file from a Linux server. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the User Deleting the Bash History \(`.bash_history`\) playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, check whether the server is a test or demo instance.

2.  In Action 2, if the server isn’t a test or demo instance, perform the following steps:

    1.  In Action 3, collect the following information for the alert:

        -   Username
        -   IP Address
        -   Malicious commands attempting to delete bash history
        -   All the commands run by the user, if available on the CrowdStrike logs.
    2.  In Action 4, log in to the server and run the `last` command to view the most recent logged-in user.

    3.  In Action 5, identify if there were any lateral movement activities from the user \(Source: Splunk, CrowdStrike, localhost\).

    4.  In Action 6, examine the activities occurring around these suspicious actions.

        ![Response task to examine the activities occurring around these suspicious actions.](../image/playbook-bash-history-overview.png "User Deleting Bash History playbook")

    5.  In Action 7, continue working with peers and involve the incident response Regional Manager in deciding whether to continue monitoring the user.

    6.  In Action 8, determine whether the activity is malicious or not.

    7.  In Action 9, if the activity is malicious, perform the following steps:

        1.  In Action 10, during the investigation, contact IT Support and request an account freeze.
        2.  In Action 11, ensure that the instance is restored to a normal state free of malicious activity.
        3.  In Action 12, lift containment and bring systems back to operational standards.
        4.  In Action 13, initiate a post incident review.

            In Action 14, after the post incident review, the flow ends.

        ![Response task to check if the activity is malicious.](../image/playbook-bash-history-investigate.png "Using the User Deleting Bash History playbook")

    8.  In Action 15, if the activity is not malicious, then in Action 16, reach out to the user’s manager.

        You can use the provided email template to contact the user's manager and inform them about the recommended approach.

3.  In Action 17, document the findings so far.

4.  In Action 18, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for User Deleting Bash History - Cloud](../concept/playbook-deleting-bash-history.md)


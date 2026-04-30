---
title: Use the Attempted Access to Deactivated Accounts playbook
description: Use this playbook when an employee whose account is terminated, disabled, or separated attempts to log in with their credentials. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Attempted Access to Deactivated Accounts playbook.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Playbook for Attempted Access to Deactivated Accounts, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Attempted Access to Deactivated Accounts playbook

Use this playbook when an employee whose account is terminated, disabled, or separated attempts to log in with their credentials. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Attempted Access to Deactivated Accounts playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, check if the attempted access to the deactivated accounts were made by an active user.

2.  In Action 2, check whether the attempted access to the deactivated accounts were made by an active employee.

    ![Response task to check whether the attempted access to the deactivated accounts were made by an active employee.](../image/playbook-attempted-access-deactivated-overview.png "Attempted Access to Deactivated Accounts playbook")

3.  If the attempted access to the deactivated accounts were made by an active employee, perform the following steps:

    1.  In Action 3, check if the user had a project or test case that caused the user to become an inactive employee.

    2.  In Action 4, if the user did not have a project or test case that caused the user to become an inactive employee, then work with the IT Support team to fix the misconfiguration.

        The flow ends.

    3.  In Action 5, if the user had a project or test case that caused the user to become an inactive employee, then perform the following steps:

        1.  In Action 6, document the findings so far.
        2.  In Action 7, initiate a post incident review.

            In Action 8, after the post incident review, the flow ends.

4.  In Action 9, if the attempted access to the deactivated account were not made by an active employee, perform the following steps:

    1.  In Action 10, verify if the user had any successful logins.

    2.  In Action 11, check when the employee was off-boarded.

    3.  In Action 12, investigate the events on Splunk to examine the user's activities during the time period.

    4.  In Action 13, based on the investigation so far, determine whether the user exfiltrated any data.

    5.  In Action 14, if the user did not exfiltrate any data, perform the following steps:

        1.  In Action 15, work with the IT Support team to terminate any active sessions and disable the accounts.
        2.  In Action 16, document the findings so far.
        3.  In Action 17, initiate a post incident review.
        In Action 18, after the post incident review, the flow ends.

        ![Response tasks if the attempted access to the deactivated accounts were not made by an active employee](../image/playbook-attempted-access-deactivated-investigate.png "Using the Attempted Access to Deactivated Accounts playbook")

5.  In Action 19, if the user exfiltrated any data, perform the following steps:

    1.  In Action 20, lock out the malicious user and destroy any active sessions.

    2.  In Action 21, work with IT Support team to disable all accounts.

    3.  In Action 22, ensure the resources are restored to the normal state and free of any malicious activity.

        You can reimage the resources if necessary.

    4.  In Action 23, lift containment and bring systems back to operational standards.

    5.  In Action 24, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Attempted Access to Deactivated Accounts](../concept/playbook-attempted-access-deactivated-accounts.md)


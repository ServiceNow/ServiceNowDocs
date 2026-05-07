---
title: Use the T1070 - Windows Events Logs Cleared playbook
description: Use this playbook to investigate incidents that track event types where the user removes security logs. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1070 - Windows Events Logs Cleared playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbook for T1070 - Windows Events Logs Cleared, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the T1070 - Windows Events Logs Cleared playbook

Use this playbook to investigate incidents that track event types where the user removes security logs. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1070 - Windows Events Logs Cleared playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, obtain the user details from the alert.

2.  In Action 2, check whether the user has been identified or not.

3.  In Action 3, if the user has not been identified, perform the following steps:

    1.  In Action 4, check the CMDB \(Configuration management database\) for the host owner details.

    2.  In Action 5, check whether the user has been identified from the CMDB or not.

        If the user has been identified from the CMDB, a manual response task is created in Action 5 and the flow ends.

    3.  In Action 6, if the user has not been identified from the CMDB, perform the following steps:

        1.  In Action 7, create an incident to identify the system owner and the individual who deleted the logs.
        2.  In Action 8, check whether the user been identified after raising an incident or not.

            If the user has been identified after raising an incident, a manual response task is created in Action 8 and the flow ends.

        3.  In Action 9, if the user has not been identified after raising an incident, perform the following steps:
            1.  In Action 10, discuss the next course of action with peers.
            2.  In Action 11, isolate the host system.
            3.  In Action 12, remove any unwanted files that may have been created, and delete the rogue accounts.
            4.  In Action 13, lift the containment and bring the systems back to operational standards.
            5.  In Action 14, complete the post-incident review before closing the task.

                In Action 15, the flow ends.

4.  In Action 16, if the user has been identified, then check the user's role to see if the user is authorized to clear or remove logs.

5.  In Action 17, reach out to the user for validation of their business justification.

    You can use the provided email template to contact the user.

6.  In Action 18, check whether a valid business justification is provided or not.

7.  In Action 19, if there was a valid business justification provided, then in Action 20, document the findings so far.

    The flow ends.

8.  In Action 21, if there was no valid business justification provided, perform the following steps:

    1.  In Action 22, discuss the next course of action with peers.

    2.  In Action 23, isolate the host system.

    3.  In Action 24, remove any unwanted files that may have been created, and delete the rogue accounts.

    4.  In Action 25, lift the containment and bring the systems back to operational standards.

        The flow ends.

9.  In Action 26, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for T1070 - Windows Events Logs Cleared](../concept/playbook-windows-events-log.md)


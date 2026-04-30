---
title: Use the Repeat Detection playbook
description: Use this playbook to investigate if the incident response has been provided on an exact or similar phishing report in the past and automatically works on the new report similarly. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Repeat Detection playbook.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Playbook for Repeat Detection, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Repeat Detection playbook

Use this playbook to investigate if the incident response has been provided on an exact or similar phishing report in the past and automatically works on the new report similarly. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Repeat Detection playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, the playbook retrieves the relative date of the security incident using the day configuration.

2.  In Action 2, the playbook looks up the Task Observable records on the table `sn_ti_m2m_task_observable` that match the incident based on the Message ID.

    ![Look up task observable records based on Message ID.](../image/playbook-repeat-detection-observables.png "Repeat Detection playbook")

3.  In Action 3, the playbook compares the Task Observables and Email body using the Levenshtein algorithm for incidents that matched the Message ID.

4.  In Action 4, based on the investigation done so far, the playbook checks whether the matching incident is found based on the Message ID or not.

    In Action 5, if the matching incident is found, the playbook automatically updates the worknote that a match has been found based on the automation for Repeat Detection. In Action 6, the flow ends.

5.  If the matching incident is not found, then in Action 7, the playbook looks up the Task Observable records on the table `sn_ti_m2m_task_observable` that match the incident based on the Subject.

6.  In Action 8, the playbook compares the Task Observables and Email body using the Levenshtein algorithm for incidents that matched the Subject.

7.  In Action 9, the playbook checks whether the matching incident is found or not.

    In Action 10, if the matching incident is found, the playbook automatically updates the worknote that a match has been found based on the automation for Repeat Detection. In Action 11, the flow ends.

    ![When the matching incident is found, the worknotes is updated.](../image/playbook-repeat-detection-worknotes.png "Matching incident")

8.  In Action 12, the playbook looks up the Task Observable records on the table `sn_ti_m2m_task_observable` that match the incident based on the Address.

9.  In Action 13, the playbook compares the Task Observables and Email body using the Levenshtein algorithm for incidents that matched the Address.

10. In Action 14, the playbook checks whether the matching incident is found based on the Address or not.

    In Action 15, if the matching incident is found, the playbook automatically updates the worknote that a match has been found based on the automation for Repeat Detection. In Action 16, the flow ends.


**Parent Topic:**[Playbook for Repeat Detection](../concept/playbook-repeat-detection.md)


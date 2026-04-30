---
title: Use the Typo Squatted Domain playbook
description: Use this playbook to investigate misspelled domains and collaborating with the organization’s legal department for take-downs. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Typo Squatted Domain playbook.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbook for Typo Squatted Domain, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Typo Squatted Domain playbook

Use this playbook to investigate misspelled domains and collaborating with the organization’s legal department for take-downs. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Typo Squatted Domain playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, you need to check whether the observables are added to the Security Incident Response \(SIR\).

    If the observables aren’t added to SIR, please add the observables before proceeding. If the observables aren’t available, then Action 10 is executed and the security incident is closed.

2.  In Action 2, if the observables are added to the security incident, then the following actions are executed.

3.  In Action 3, you need to attach the screenshot of the Typo Squatted domain to the security incident.

    ![Response tasks to check if the observables are added to the security incident.](../image/playbook-typo-squatted-observables.png "Typo Squatted Domain playbook")

4.  In Action 4, you need to attach the Whois information to the security incident.

5.  In Action 5, based on the investigation done so far, the playbook checks whether this is a case of Typo Squatted domain or not.

    If this isn’t a case of Typo Squatted domain, a manual response task is created in Action 5 and the flow ends.

6.  In Action 6, if this is a case of Typo Squatted domain, then action 7 is executed.

7.  In Action 7, you need to email and inform the Legal and other required teams that this is a case of Typo Squatted domain and take the necessary actions to eradicate it.

    If this isn’t a case of Typo Squatted domain, a manual response task is created in Action 5 and the flow ends.

    ![Response tasks if this is a case of Typo Squatted Domain](../image/playbook-typo-squatted-response.png "Case of Typo Squatted Domain")

8.  In Action 9, a response task is created for you to complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Typo Squatted Domain](../concept/playbook-typo-squatted-domain.md)


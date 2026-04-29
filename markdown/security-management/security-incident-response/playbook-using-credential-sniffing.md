---
title: Use the Credential Sniffing playbook
description: Use this playbook to investigate an incident involving credential sniffing activities performed through the sys\_installation\_exit table in a ServiceNow instance. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Credential Sniffing playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for Credential Sniffing, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Credential Sniffing playbook

Use this playbook to investigate an incident involving credential sniffing activities performed through the **sys\_installation\_exit** table in a ServiceNow instance. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Credential Sniffing playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, review the following alert details.

    -   Instance
    -   Session ID
    -   Transaction ID
    -   \_raw: Provides the whole script.

        Example script:

        ```
        Var pass= request.getParameter(“user_password”);
        Gs.log(pass);
        ```

2.  In Action 2, based on the data collected so far, check whether an end user ticket is required for this alert or not.

3.  In Action 3, if the alert does not require an end user ticket, then in Action 4, document the findings so far.

    The flow ends.

    ![Response tasks to investigate if this alert is a possible case of credential sniffing](../../secops-analyst-workspace/image/playbook-credential-sniff-investigate.png "Credential Sniffing Playbook")

4.  In Action 5, if the alert requires an end user ticket, then perform the following steps:

    1.  In Action 6, inform the end user that the alert requires an end user ticket.

    2.  In Action 7, investigate further based on the user's response and the user's sessions during the last couple of days.

    3.  In Action 8, discuss with peers about the remediation steps for the instance like locking out the user and detecting which user’s passwords might have been read.

    4.  In Action 9, raise an incident or ticket to reset the compromised user credentials.

    5.  In Action 10, lift the containment and bring the systems back to operational standards

        The flow ends.

5.  In Action 11, complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Credential Sniffing](../concept/playbook-credential-sniffing.md)


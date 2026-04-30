---
title: Use the Spoofed Emails \(using the same Display name\) playbook
description: Use this playbook to investigate Spoofed Emails, which get triggered when spoofed names for emails are sent to the organization's employees. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Spoofed Emails \(using the same Display name\) playbook.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbook for Spoofed Emails \(using the same Display name\), Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Spoofed Emails \(using the same Display name\) playbook

Use this playbook to investigate Spoofed Emails, which get triggered when spoofed names for emails are sent to the organization's employees. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Spoofed Emails \(using the same Display name\) playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, you need to check if there are any continuous spoofed emails in Proofpoint.

2.  In Action 2, if there are continuous emails in Proofpoint, then check whether this an internal spoofed email or not.

3.  In Action 3, if this is an internal spoofed email, perform the following actions:

    1.  In Action 5, you need to perform URL analysis using any sources like Virus Total, Anomali Threat stream Sandbox, urlquery.net, PhishTank \(For example, check PhiskTank and Anomali\).

    2.  In Action 6, you need to investigate the URL on a Linux VM \(For example, Ubuntu\).

        ![Response task to investigate the URL on a Linux VM.](../image/playbook-spoofed-email-url.png "Spoofed Emails (using the same Display name) playbook")

    3.  In Action 7, you need to look up when the domain was created on WHOIS.

        Look for recently registered domains \(within the last week\) that are suspicious and have a high probability of phishing attacks.

    4.  In Action 8, based on the investigation done so far, you need to check whether this email contains a malicious attachment or link.

        If this email doesn't contain a malicious attachment or link, then the flow ends.

        ![Response tasks to check if the spoofed email contains malicious attachments or links.](../image/playbook-spoofed-email-users.png "Spoofed email contains malicious attachments or links")

    5.  In Action 9, if the email contains malicious attachments or links, perform the following actions.

        1.  In Action 10, you need to reach out to the affected user to check if the credentials are compromised. You can use the provided email template to contact the affected user.
        2.  In Action 11, you need to check whether the credentials are compromised based on the email response. If the credentials weren’t compromised, then the flow ends.
            1.  In Action 12, if the credentials are compromised, then in Action 13, you need to check if additional users are impacted. If no additional users are impacted, then the flow ends.
            2.  In Action 14, if additional users are impacted, then perform the following actions:
                1.  In Action 15, you need to search and delete emails using Microsoft Exchange Online.
                2.  In Action 16, you need to block the sender and the malicious files or attachments on Office 365 and Proofpoint.
4.  In Action 17, if this isn’t an internal spoofed email, then you need to check if the affected user's system is impacted.

5.  In Action 18, if the user's system is impacted, then in Action 19, raise an IT ticket to reimage the impacted system.

    ![Response task to check if the affected user's system is impacted.](../image/playbook-spoofed-email-system.png "Check if the affected user's system is impacted")

6.  In Action 20, a response task is created for you to complete the post-incident review before closing the task.


**Parent Topic:**[Playbook for Spoofed Emails \(using the same Display name\)](../concept/playbook-spoofed-emails-display-name.md)


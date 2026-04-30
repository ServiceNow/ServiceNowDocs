---
title: Playbook for T1070 - Windows Events Logs Cleared
description: This playbook provides remediation steps to investigate incidents that track event types where the user removes security logs. Whenever the Security log is cleared, the events 517 and 1102 are logged regardless of the Audit System Event policy status.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for T1070 - Windows Events Logs Cleared

This playbook provides remediation steps to investigate incidents that track event types where the user removes security logs. Whenever the Security log is cleared, the events 517 and 1102 are logged regardless of the Audit System Event policy status.

This alert can track the following types of events:

-   **Event 517**: The Primary username and Client username fields identifies the user who cleared the log. The Primary username corresponds to the system, and the Client username indicates the user who cleared the log.
-   **Event 1102**: The Account Name and Domain Name fields identifies the user who cleared the log. The Logon ID enables you to correlate backwards to the log on event and other events logged during the same logon session.

-   **[Set up the T1070 - Windows Events Logs Cleared playbook](../task/playbook-setup-windows-events-logs.md)**  
Use the following steps to set up the T1070 - Windows Events Logs Cleared playbook.
-   **[Use the T1070 - Windows Events Logs Cleared playbook](../task/playbook-using-windows-events-logs.md)**  
Use this playbook to investigate incidents that track event types where the user removes security logs. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the T1070 - Windows Events Logs Cleared playbook.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)


---
title: Security Incident Response playbooks
description: You can invoke the security incident playbook flow automatically or manually.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response playbooks

You can invoke the security incident playbook flow automatically or manually.

A Playbook is visible only if at least one playbook is associated with a security incident. The playbook component works only for the Process Automation Designer \(PAD\) built processes and not for the flow designer-built flows. For the existing flow designer enabled flows, it will continue to work, and the activities will be continuing to be rendered as response tasks.

Security Incident Response supports two types of Playbooks:

-   [Process-based Playbooks](playbooks-process-based.md)
-   [Flow-based Playbooks](playbook-flow-based.md)

In addition to the listed playbooks, there are also subflows in Security Operations Spoke that can be called from the flows playbook. Ransomware is one of that subflows.

Activate these flows before you use them. For more information, see [Activate a Security Incident Response flow](../task/getting-started-phishing-playbook.md).

-   **[Process-based Playbooks](playbooks-process-based.md)**  
The playbook component works only for playbooks built in Workflow Studio and not for flows. However, existing flow-based playbooks will continue to work and the activities will be continuing to be rendered as response tasks.
-   **[Flow-based Playbooks](playbook-flow-based.md)**  
Using the Flow Designer, security administrators and flow design authors can more easily transition from manual or undocumented playbooks to automated and repeatable playbooks. The drag-and-drop feature provides flexibility in moving objects, condition checks, parallel branching, decision tables, and more.

**Parent Topic:**[Playbook Resources](cj-sir-flow-library.md)


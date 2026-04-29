---
title: HR Service Delivery Agent Workspace integration with Universal Request
description: With the integration of HR Service Delivery Agent Workspace and Universal Request applications, you can provide a consistent user experience for employees while creating service requests.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Workspace, HR Service Delivery, Employee Service Management]
---

# HR Service Delivery Agent Workspace integration with Universal Request

With the integration of HR Service Delivery Agent Workspace and Universal Request applications, you can provide a consistent user experience for employees while creating service requests.

**Important:**

-   HR Service Delivery Agent Workspace \(Classic\) is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.
-   If you are an existing user of HR Service Delivery Agent Workspace \(Classic\), you can migrate to the Agent Workspace for HR Case Management \(Configurable\) for enhanced features and capabilities. See [Migration Guidelines](https://www.servicenow.com/community/hrsd-articles/hr-agent-workspace-migration-guidelines-from-classic-to/ta-p/2310606).

## Overview

A universal request gets created when an employee clicks the **Request help** option in Employee Center. A universal request routing agent analyses the issue \(as HR department related\) and creates an HR case from that universal request. After the case gets resolved by an HR agent, the state of the HR case changes to **Awaiting Acceptance**. Automatically, the state of the universal request changes to **Awaiting response**. Finally, after the employee accepts the resolution, the universal request gets closed and in turn, the HR case gets closed.

At any point in time, the HR agent can [route the HR case back](../task/route-hrcase-ur-workspace.md) to the universal request queue with or without resolution.

All the important details, such users who are working on the issue, inter-department transfers, and work notes, are recorded in the universal request ticket providing complete visibility to the employee who has raised the request.

## Activating the necessary plugins

After you have activated the Human Resources Scoped App: Workspace \(com.sn\_hr\_agent\_workspace\) and Universal Request \(com.snc.universal\_request\) plugins, you will notice that:

-   The Universal Request form has the UI action to create an HR case.
-   The **Universal Request** field appears on the HR case form only when an HR case is associated with a universal request record.
-   The **Transfer** button appears on the HR case form to let an HR agent route an HR case back to the universal request, another department, or service.


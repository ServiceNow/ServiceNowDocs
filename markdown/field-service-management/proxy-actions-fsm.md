---
title: Proxy actions in Field Service Management
description: Proxy actions let authorized managers, dispatchers, and agents perform work order task actions on behalf of a technician who can't act in the moment. This keeps task progress moving without blocking on a missed connection or an unreachable field agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/proxy-actions-fsm.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [proxy actions, Field Service Management, work order task]
breadcrumb: [Explore, Field Service Management]
---

# Proxy actions in Field Service Management

Proxy actions let authorized managers, dispatchers, and agents perform work order task actions on behalf of a technician who can't act in the moment. This keeps task progress moving without blocking on a missed connection or an unreachable field agent.

Field Service technicians often work without reliable connectivity or device access. When a technician can't accept, reject, or close out a task in real-time, proxy actions let another authorized user step in. That user performs the action on the technician's behalf without reassigning or transferring task ownership. The task stays assigned to the original technician throughout.

## Key features

Proxy actions are policy-driven, so administrators control exactly who can act on whose behalf and under what conditions. Key aspects of proxy actions include:

-   **Policy-based access**

    Administrators create policies that define which users or roles can perform proxy actions and which work order tasks are in scope. Each policy covers either a specific set of actions or all of them.

-   **Covered actions**

    Accept, reject, start travel, start work, close complete, and close incomplete.

-   **No ownership transfer**

    Performing a proxy action doesn't reassign the task or change who it's assigned to. The original technician remains the assignee. The work order task activity stream indicates the proxy action was taken and who took it.

-   **Time zone-aware backdating**

    For actions that record a time — start travel, start work, close complete, and close incomplete — the proxy user enters the actual time the action occurred. The time displays in the technician's time zone, so the entry stays accurate across time zones.

-   **Full attribution**

    Every proxy action is logged to the activity stream and an audit trail, identifying the proxy user, the technician, the action taken, and when it was submitted.


**Related topics**  


[Configure proxy actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/configure-proxy-fsm.md)

[Complete a proxy action in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/proxy-action-dispatcher.md)

[Complete proxy actions on Field Service Manager Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/proxy-action-manager.md)

[Complete a proxy action in Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-manager-workforce/proxy-action-workforce.md)


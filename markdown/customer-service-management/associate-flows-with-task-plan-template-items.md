---
title: Flow-based automation for task plan template items
description: A task plan template item stamps its number on each record it creates. A flow can use that stamped value as a trigger condition, so the flow runs automatically for the records that one specific template item creates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/associate-flows-with-task-plan-template-items.html
release: brazil
topic_type: concept
last_updated: "2026-09-04"
reading_time_minutes: 2
keywords: [task plan template, flow, template item, automation, AI agent, subflow]
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Flow-based automation for task plan template items

A task plan template item stamps its number on each record it creates. A flow can use that stamped value as a trigger condition, so the flow runs automatically for the records that one specific template item creates.

## Overview

Some steps in a task plan need work that a task plan template cannot do on its own. For example, a router setup plan can include an address verification step, where an external system must confirm the customer address before the next step starts.

You can run a flow for an individual step in a task plan. A template item does not store a reference to a flow. Instead, the template item stamps its number on every record it creates, and the flow uses that stamped value as its trigger condition. Because the flow is triggered by the record, its actions can do anything a flow can do, including calling a subflow or an AI agent.

## Key benefits

-   Automates individual steps of a task plan without rebuilding the whole process as a flow.
-   Removes the need for an agent to start a flow manually after the task is created.
-   Runs a different flow for each template item in the same task plan.
-   Calls an existing subflow or an AI agent from the triggered flow.

## How it works

The following describes the general behavior of a flow that runs for a template item:

1.  The target table of the template item has a reference field that points to the template item.
2.  The **Template item field** field on the template item is set to that reference field, so the template item stamps it on each record it creates. For more information, see [Template item form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/task-plan-template-item-form.md).
3.  A flow is created on the target table with a trigger of **Created** and a condition that matches the number of the template item.
4.  When the task plan template is applied, the template item creates its record and the system stamps the template item number on that record.
5.  The new record meets the trigger condition, and the flow runs its actions. For example, the flow can set fields on the new task, notify the assigned agent, or hand the work to an AI agent.

## Considerations

-   The trigger condition matches one template item number, so a flow created for one template item does not run for any other template item.
-   The reference field must exist on the target table of the template item before the template item can stamp it.

**Related topics**  


[Trigger a flow from a task plan template item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-a-flow-with-a-task-plan-template-item.md)

[Template item form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/task-plan-template-item-form.md)


---
title: Generate approvals using Workflow flows
description: Workflow Studio flows are a powerful and flexible method of generating approvals. Use workflow flows to create group approvals and user approvals.
locale: en-US
release: australia
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Generate approvals using Workflow flows

Workflow Studio flows are a powerful and flexible method of generating approvals. Use workflow flows to create group approvals and user approvals.

A variety of variables are available to fine-tune the approval process, including the actions that occur when approval or rejection take place. When a Workflow Studio flow generates an approval record, the system populates the **Flow** field on the approval record with a reference to the flow and the Ask for Approval action. Do not use this field when creating business logic. For more information, see .

**Note:** Conflicts can arise when the approval process for a table is managed by both the Workflow Studio engine and the approval engine. In general, if there is a Workflow Studio flow that manages the approval process for a table, the [approval engine](c_ApprovalEngines.md) should be turned off for that table.

**Parent Topic:**[Classic approvals](../reference/r_Approvals.md)

**Related topics**  


[Classic approvals](../reference/r_Approvals.md)


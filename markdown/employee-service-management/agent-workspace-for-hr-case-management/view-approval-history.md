---
title: View approval history in Agent Workspace for HR Case Management
description: Review the approval history in the activity stream. Get a better understanding of when the approval request was created, who were the approvers, and when was the request rejected or approved.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with approvers for a case, Use, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# View approval history in Agent Workspace for HR Case Management

Review the approval history in the activity stream. Get a better understanding of when the approval request was created, who were the approvers, and when was the request rejected or approved.

## Before you begin

-   Role required: sn\_hr\_core.case\_writer
-   Ensure that the following plugins are installed: Human Resources Scoped App:Core, Human Resources Scoped App:Lifecycle Events, Human Resources Scoped App:Lifecycle Events for Enterprise, HRSD Configurable Workspace, and Human Resources Scoped app Workspace.

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**.

2.  Open a case that is in Ready state.

3.  Activity stream contains the approval history, for example, when was the approval request created, who were the approvers, and when was the request rejected or approved.

    **Note:**

    -   Approval history appears in activity stream only when the **glide.workflow.user\_approval\_history** property in **sys\_properties.list** is set to true.
    -   If this property is set to true in HR Service Delivery workspace, it will be also to be true for all other installations within ServiceNow AI Platform.


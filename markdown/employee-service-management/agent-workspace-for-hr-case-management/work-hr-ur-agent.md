---
title: Work on an HR case of Universal Request in HR Service Delivery Agent Workspace
description: Provide resolution to an HR case that is initiated from a Universal Request.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Agent Workspace integration with Universal Request, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Work on an HR case of Universal Request in HR Service Delivery Agent Workspace

Provide resolution to an HR case that is initiated from a Universal Request.

## Before you begin

Role required: routing\_agent and sn\_hr\_core.case\_writer

## About this task

The state changes described in the procedure can be configured to suit your requirements. For more information, see [Universal Request state mapping](../../universal-request/task/ur-state-mapping.md)

## Procedure

1.  Open the HR case that is created from a Universal Request.

2.  Click **Start Work**.

    The state of the case changes to **Work in Progress**.

3.  Click **Closed Complete** when the resolution is provided.

    The state of the HR case is changed to **Awaiting acceptance** and the state of the universal request is automatically changed to **Awaiting response**. On the Employee Center:

    -   If the user accepts the resolution, the state of the universal request is changed to **Closed**. The state of the HR case is automatically changed to **Closed Complete**.
    -   If the user rejects the resolution, the state of the universal request is changed to **In progress**. The state of the HR case is automatically changed to **Work in progress.**
    **Important:** If for some reason the HR agent clicks **Closed Incomplete** without routing the HR case back to universal request, then the behavior is as follows:

    -   If the **Needs Additional Review** check box is selected on the universal request, the universal request will be in the **In progress** state, and the HR case will be in the **Close Incomplete** state.
    -   If the **Needs Additional Review** check box is deselected on the universal request, the universal request gets closed based on the state mapping.


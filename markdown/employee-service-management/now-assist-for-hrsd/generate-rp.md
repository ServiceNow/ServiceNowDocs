---
title: Generate a fulfillment plan
description: Auto-generate a fulfillment/execution plan for a case, helping in faster resolution of the HR case.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-08-01"
reading_time_minutes: 1
breadcrumb: [Resolve HR cases agentic workflow, Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate a fulfillment plan

Auto-generate a fulfillment/execution plan for a case, helping in faster resolution of the HR case.

## Before you begin

Role required: sn\_hr\_core.case\_writer, now\_assist\_panel\_user

You can generate a case fulfillment plan from either Core UI or Agent Workspace for HR Case Management.

## Procedure

1.  Navigate to **Workspaces** &gt; **HR Agent Workspace**.

    Alternatively, you can navigate to **All** &gt; **HR Case Management** &gt; **All HR Cases**.

2.  Open an HR case that is assigned to you.

3.  Select **Generate plan**.

    **Note:** This option appears only for the HR service of Fulfillment type: **Manual**. It does not appear for the Employee Relations and Life Cycle Events cases.

    The AI agent creates a fulfillment plan for a given HR case by fetching HR case details, relevant KB articles, and fulfillment instructions.

4.  Choose one of the following options:

    -   Type **Approve** to publish the AI-generated fulfillment plan to the work notes of the case.
    -   Type **Modify** to add prompts for refining the AI-generated fulfillment plan.
    -   Type **Reject** to discard the AI-generated fulfillment plan.
    ![Fulfillment plan for an HR case on Core UI](../image/generate-plan-ckm.png "Example of AI-generated fulfillment plan on Core UI")




**Parent Topic:**[Resolve HR cases agentic workflow](../concept/employee-issue-resolver-na.md)


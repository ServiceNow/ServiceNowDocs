---
title: Set up an approval engine
description: To manage the approvals for each of the Task tables in the system, set up an approval engine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/approvals/t\_SetupAnApprovalEngine.html
release: australia
product: Approvals
classification: approvals
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Approval engines, Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up an approval engine

To manage the approvals for each of the Task tables in the system, set up an approval engine.

**Important:** Classic approval rules have been replaced by the Workflow Studio . Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Approval Engines**.

    The following page appears with the **Approval Engine** option for each Task table in the system. If the **Approval Engine** option is greyed out and shows **Turn engines off**, read the **Notes** in the same row. The most common reason an approval engine is turned off is that a workflow is managing the approvals on the table. Having the approval engine turned off prevents conflicts with the workflow that could cause a range of issues. If you want to use an approval engine on the table, set the workflow to inactive.

    \[Omitted image "ApprovalEnginePage.png"\] Alt text: Approval engine page

2.  Select the [approval engine option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/approvals/c_ApprovalEngines.md) for each Task table from the choice list.

3.  Click **Save**.

    These preferences are saved as system properties that are named **glide.approval\_engine.&lt;table\_name&gt;**.


**Parent Topic:**[Approval engines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/approvals/c_ApprovalEngines.md)


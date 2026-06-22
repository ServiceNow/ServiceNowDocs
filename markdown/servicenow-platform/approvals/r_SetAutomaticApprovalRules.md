---
title: Set automatic approval rules
description: Approval rules can automatically set the approval state to something other than Not yet requested. As a result, an approval rule can create a set of approvers. You can also start the approval process by setting the approval state to Requested.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/approvals/r\_SetAutomaticApprovalRules.html
release: zurich
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Approval rules, Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set automatic approval rules

Approval rules can automatically set the approval state to something other than Not yet requested. As a result, an approval rule can create a set of approvers. You can also start the approval process by setting the approval state to **Requested**.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/ask-approval-flow-designer.md). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

## Prerequisites

Role required: admin

Approval rules have two new fields:

-   **Run rule before**: If true, the approval rule runs before the record is inserted/updated.
-   **Set State**: If this rule applies, then the task record's approval state is automatically set to this value.

    **Note:** The **Set State** field only behaves as expected if the **Run rule before** check box is enabled.

-   In the example below, this rule automatically sets the state of the task to Approved thereby auto-approving the task.

\[Omitted image "ApprovalRulesFields.png"\] Alt text:

**Parent Topic:**[Approval rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/approvals/c_ApprovalRules.md)


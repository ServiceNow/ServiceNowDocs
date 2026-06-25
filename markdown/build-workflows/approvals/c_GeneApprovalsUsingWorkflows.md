---
title: Generate approvals using Workflow flows
description: Workflow Studio flows are a powerful and flexible method of generating approvals. Use workflow flows to create group approvals and user approvals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/approvals/c\_GeneApprovalsUsingWorkflows.html
release: australia
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Build workflows]
---

# Generate approvals using Workflow flows

Workflow Studio flows are a powerful and flexible method of generating approvals. Use workflow flows to create group approvals and user approvals.

A variety of variables are available to fine-tune the approval process, including the actions that occur when approval or rejection take place. When a Workflow Studio flow generates an approval record, the system populates the **Flow** field on the approval record with a reference to the flow and the Ask for Approval action. Do not use this field when creating business logic. For more information, see [Ask for Approval action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/ask-approval-flow-designer.md).

**Note:** Conflicts can arise when the approval process for a table is managed by both the Workflow Studio engine and the approval engine. In general, if there is a Workflow Studio flow that manages the approval process for a table, the [approval engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/approvals/c_ApprovalEngines.md) should be turned off for that table.

**Related topics**  


[Classic approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/approvals/r_Approvals.md)


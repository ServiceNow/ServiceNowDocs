---
title: Working with approvers for a case in Agent Workspace for HR Case Management
description: HR cases can be set up to require approvals before it can progress to completion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/agent-workspace-for-hr-case-management/hr-agent-ws-approvers.html
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Working with approvers for a case in Agent Workspace for HR Case Management

HR cases can be set up to require approvals before it can progress to completion.

The HR service configures actions related to approvals. For more information on HR service configuration, see [Configure an HR service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/configure-hr-service.md).

When a case requires an approver, the request for approval appears in the approver's Employee Center or portal under To-dos.

In Agent Workspace for HR Case Management, the child tab **Approvers** lists all requested approvers.

## Multiple approvers

HR services can have multiple approvers. When configuring an HR service, you can select approvers from fields on the HR case. For example, the subject person's manager can be selected as an approver. Using case fields provides maximum flexibility when assigning approvers.

When an approver is assigned from a case field, the approver may not be found in the following circumstances:

-   The subject person's HR profile does not contain a manager
-   The subject person's manager recently left the company
-   The manager field is empty or invalid

When an approver is missing, a warning message appears on the Approvers tab:

\[Omitted image "agent-ws-hr-missing-approvers.png"\] Alt text: Approvers tab showing warning message that approver is missing with option to select different approver


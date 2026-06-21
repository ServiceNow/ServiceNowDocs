---
title: Adding or substituting approvers to a case in HR Service Delivery Agent Workspace
description: HR cases can be set up to require approvals before it can progress to completion.Using HR Service Delivery Agent Workspace you can add an approver or substitute missing approvers for cases that require approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/hr-service-delivery/agent-ws-hr-add-approvers.html
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Adding or substituting approvers to a case in HR Service Delivery Agent Workspace

HR cases can be set up to require approvals before it can progress to completion.

The HR service configures actions related to approvals. For more information on HR service configuration, see [Configure an HR service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/hr-service-delivery/configure-hr-service.md).

When a case requires an approver, the request for approval appears in the approver's Employee Center or portal under To-dos.

\[Omitted image "esc-hr-to-do.png"\] Alt text: Employee Center - To-dos

|Number|Description|
|------|-----------|
|\[Omitted image "1.png"\] Alt text: HR Agent Workspace Case form callout 1|Select To-dos.|
|\[Omitted image "2.png"\] Alt text: HR Agent Workspace Case form callout 2|To approve, select **Approve**. To reject, enter a reason and select **Reject**.|

In HR Service Delivery Agent Workspace, the child tab **Approvers** lists all requested approvers.

\[Omitted image "agent-ws-hr-approvers-tab.png"\] Alt text: HR Agent Workspace - Approvers tab

## Multiple approvers required

HR services has an optional configuration that requires multiple approvers. When configuring an HR service, select approvers from the fields on the HR case. For example, select Subject person manager as an approver. Using fields from a case provides maximum flexibility when assigning an approver. By assigning an approver from the case, it's possible an approver cannot be found. For example:

-   Subject person manager is the approver.
-   The Subject person's HR profile does not contain a manager.
-   Or, the Subject person's manager recently left the company.

When an approver is missing, the following message appears:

\[Omitted image "agent-ws-hr-missing-approvers.png"\] Alt text: HR Agent Workspace - Missing approvers message

## Add or substitute an approver to a case in HR Service Delivery Agent Workspace

Using HR Service Delivery Agent Workspace you can add an approver or substitute missing approvers for cases that require approval.

### Before you begin

Role required: sn\_hr\_core.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Locate and open an HR case that requires approvers.

3.  Select **Add Approvers** from the list of UI actions \(tabs at the top of the form\).

    \[Omitted image "agent-ws-hr-approver-missing.png"\] Alt text: HR Agent Workspace - Approver missing

4.  Select replacement approvers or add new ones.

    \[Omitted image "agent-ws-hr-list-approvers.png"\] Alt text: HR Agent Workspace - List of approvers

5.  Select **OK**.

6.  Select **Save**.



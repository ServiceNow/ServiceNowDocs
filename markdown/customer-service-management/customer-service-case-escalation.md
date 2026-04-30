---
title: Case and account escalation
description: Use the escalation feature to highlight specific cases or accounts and raise awareness of important customer issues.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-03-27"
reading_time_minutes: 2
breadcrumb: [Administer Customer Service Management, Customer Service Management]
---

# Case and account escalation

Use the escalation feature to highlight specific cases or accounts and raise awareness of important customer issues.

Escalating a case or an account provides the following benefits:

-   Increases attention about a customer issue.
-   Facilitates communication about that issue.
-   Provides a way to track progress toward a resolution.

Users with the escalation requester role can [escalate a case or an account](../task/escalate-csm-case.md) by selecting the **Escalate Case** related link on the case or account form.

## Case and account escalation differences

While the escalation process is similar for cases and accounts, there are some important differences to note.

-   Case escalations: A customer service agent typically manages a case escalation and works directly with the escalated case to resolve the issue.
-   Account escalations: An escalation manager typically manages an account escalation, which can include multiple associated cases, and records details in the escalation record.

For more information, see [Case and account escalation differences](../reference/case-account-escalation-differences.md).

## Configuring case and account escalation

The following table includes an overview of case and account escalation configuration tasks. Users with the system administrator role can perform these tasks.

|Task|Description|
|----|-----------|
|[Configure escalation management](../task/configure-escalation-management.md)|Configure case and account escalation using Customer Service Management guided setup.|
|[Create a case or account escalation template](../task/create-escalation-template.md)|Escalation templates determine how an escalation request is processed, including the type of escalation and an optional approval process.|
|[Create a case or account escalation severity](../task/create-escalation-severity.md)|Create definitions for different levels of escalation severity and select color indicators to highlight escalated cases and accounts in the user interface.|

## Using case and account escalation

The following table includes an overview of case and account escalation user tasks.

<table id="table_case_escalation_use"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Escalate a case or an account](../task/escalate-csm-case.md)

</td><td>

Escalate cases or accounts, either on behalf of customers or for internal purposes. Escalating a case or account creates an associated escalation record. Role required: escalation requester

</td></tr><tr><td>

[Manage an escalated case or account](../task/manage-escalated-case-account.md)

</td><td>

Manage a case or account through the escalation process using the escalation record. The system identifies cases and accounts on lists and forms with color indicators that correspond to the escalation severity: red \(high\) or orange \(medium\).Role required:

-   Customer service agent
-   Escalation manager

</td></tr><tr><td>

[De-escalate a case or an account](../task/de-escalate-csm-case.md)

</td><td>

De-escalate cases or accounts when the cause of the escalation is resolved. Role required: de-escalation requester

</td></tr><tr><td>

Use an optional escalation approval process

</td><td>

Include an optional approval step for approvers to review a request and either approve or reject an escalation. When using the optional approval step, the system creates the escalation record upon approval and associates it with the case or account.

</td></tr></tbody>
</table>
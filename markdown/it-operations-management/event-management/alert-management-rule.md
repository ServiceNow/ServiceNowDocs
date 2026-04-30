---
title: Alert management rules for resolving alerts
description: You can configure Event Management to respond to alerts automatically. An alert management rule determines the required alert response, such as to open an incident, knowledge base article, open a task, launch remediation action.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Alert management rules for resolving alerts

You can configure Event Management to respond to alerts automatically. An alert management rule determines the required alert response, such as to open an incident, knowledge base article, open a task, launch remediation action.

Alert management rules provided with the base system as a store application \(Alert Rules Management \[sn\_em\_arm\]\) to help you respond to alerts. You can create filters to specify conditions for the rule so that the remedial action specified in the rule takes effect only when the conditions are met. For example, launch the required subflow or open an incident based on an alert. The alert's execution history is automatically updated to indicate the actions that were invoked.

Users with the evt\_mgmt\_admin role can use the alert management rule designer to create and customize alert management rules to act on specified alerts. Define rules with filters to determine which alerts the rule applies to. You can create rules to launch applications, URLs, subflows, remediation actions, or take other actions, such as to open an incident. For more information, see [Create an alert management rule](../task/create-alert-management-rule.md).

Users with the evt\_mgmt\_operator role can manually run alert management rules.

## Alert management rule flow

The flow to create and run an alert management rule is:

![Alert Management workflow](../image/alert-mgmt-workflow.png)

<table id="table_bmf_1ht_zcb"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alert Info

</td><td>

Configure a name and general information for the rule.

</td></tr><tr><td>

Alert Filter

</td><td>

Specify a filter to determine to which alerts the rule applies. You can specify the related list conditions.**Note:** The fields that are not supported for alert filtering are: Overall Event Count, Priority, Priority Group, Priority Breakdown, Tags, and Impacted Services.

</td></tr><tr><td>

Actions

</td><td>

Specify the response to the alert, such as to run a subflow, perform remediation action, launch an application, or launch a URL in a browser.

</td></tr></tbody>
</table>## How rules are applied to updated alerts

Alert management rules run on all updated open alerts. Rules don’t run on closed alerts, even if they’ve been updated. The filters determine whether the rule's actions apply to the alert. For example, if a rule's condition indicates that an email message is sent when the alert severity changes to Major, the rule applies to an alert updated by a severity change from Warning to Major.

## Use of filters and other actions

Filters ensure that the rule is invoked only when the configured condition occurs, and not for every update of the alert. For example, you can configure a rule so that updates that aren’t relevant \(such as a **Work notes** field update\) don’t cause the rule to run. As another example, a filter condition can specify that the alert management rule runs only when the alert severity is critical.

You can perform the following actions:

-   Specify a filter that determines which alerts the rule applies to.
-   In the Related List Conditions section of the form, configure additional conditions, for example, with an **Alert &gt; Parent** relationship, to filter for any alerts that were received today.
-   Respond to alerts. For example, by using subflows and workflows, create incidents for primary alerts with critical severity, or open a search engine in a browser to search for data according to the description field of the alert.
-   Apply remediation. Remediation is based on Orchestration workflows that can be scripted to perform remediation tasks such as gathering system information or rebooting a server.

    **Note:** For enhanced performance of **Event Management - Evaluate Scoped Alert Rules Management** scheduled jobs, use subflows instead of workflows.


## Scheduled jobs that check alert management rules

Alert management rules are checked every 11 seconds by the default **Event Management - Evaluate Scoped Alert Rules Management0** scheduled job. The job then executes the required actions. For large-scale environments, you can add more than one job. Please contact Customer Service and Support.

**Note:** Only new users from Vancouver and up get two scheduled jobs: **Event Management - Evaluate Scoped Alert Rules Management0** and **Event Management - Evaluate Scoped Alert Rules Management1**. Users upgrading from previous family releases remain with a single scheduled job **Event Management - Evaluate Scoped Alert Rules Management0**.

Don’t modify the **sn\_em\_arm.alert\_management.num\_of\_jobs** property.

By default, the alert grouping job \(**Service Analytics group alerts using RCA/Alert Aggregation**\) and the alert management \(**Event Management - Evaluate Scoped Alert Rules Management0**\) jobs run independently of each other. For more information about coordinating the alert response and the automated alert grouping, see [Synchronizing alert response with automated alert grouping](../task/coordinating-alert-response-with-automated-alert-grouping.md).

## Migrate existing alert action rules

Existing alert action rules from an earlier release can be migrated to become alert management rules. You can modify an alert action rule only after migrating it to an alert management rule. For more information, see [Migrate an alert action rule to an alert management rule](../task/t_EMCreateAlertRule.md).

-   **[Create an alert management rule](../task/create-alert-management-rule.md)**  
Create an alert management rule to track alerts and resolve them by determining the required response, for example, to open an incident or launch remediation action.
-   **[Event Management subflows in the base system](../reference/subflows-provided.md)**  
The subflows provided with the base system appear in the Remediation Subflows area of alert management rules.
-   **[Create a custom subflow](../task/create-custom-create-incident-subflow.md)**  
You can create a subflow according to your requirements. You can then use the custom subflow to resolve alerts.
-   **[Alert executions information](alert-rule-execution.md)**  
Alert executions information provides a reference to the alert management rule actions that are performed. This information appears in the Alert Management Rule record only if an alert matches the filter in the rule and an action was performed. You can click any link in the Alert Executions list to open the referenced item.
-   **[Migrate an alert action rule to an alert management rule](../task/t_EMCreateAlertRule.md)**  
Existing alert action rules from an earlier release can be executed, but cannot be modified. Alert action rules that have been migrated become alert management rules and all the definitions of the alert action rules are migrated to the alert management rule format. Migrated rules can be modified.
-   **[Synchronizing alert response with automated alert grouping](../task/coordinating-alert-response-with-automated-alert-grouping.md)**  
Synchronize alert response with grouping by ensuring alert management jobs runs after alert grouping jobs—this prevents duplicate actions like incident creation on secondary alerts.
-   **[Configure alert remediation actions](../task/configure-alert-remediation-subflows.md)**  
Run commands to perform alert remediation on remote Linux and Windows CIs.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)


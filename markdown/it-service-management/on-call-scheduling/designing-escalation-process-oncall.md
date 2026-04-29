---
title: Designing an escalation process
description: To design an escalation process for a task, you define a trigger rule and configure one or more escalation policies.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Escalations in On-Call Scheduling, Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Designing an escalation process

To design an escalation process for a task, you define a trigger rule and configure one or more escalation policies.

A trigger rule specifies both the conditions under which an escalation process should begin and the escalation actions \(workflow or script\) to perform. An escalation policy describes the order in which escalation notifications are sent, the escalation audience, and other aspects of the escalation.

## How a trigger rule works

When a task is created or updated, the instance compares the assignment rules with the rule's conditions to determine whether a condition is met. If there is a match, then the instance activates the workflow or script that is specified by the rule's action. Trigger rules are an extension of assignment rules and they have the same behavior as assignment rules.

For example, a trigger rule might specify:

-   If \(rule condition\): An incident with level **Critical** or **High** is raised and is assigned to the **Network** group.
-   Then \(rule action\): Run the **Assign and Notify** workflow. \(The workflow sends an email notification to the current on-call roster member.\)

![Network high priority trigger rule](../image/trigger-rule-when-to-activate-tab.png "Rule condition on the When to activate tab")

![example trigger action](../image/trigger-rule-action-to-take-tab.png "Rule action on the What action to take tab")

**Note:** An on-call escalation is canceled when the assignment group of the associated task record, for example, an incident, changes to a different group without a matching trigger rule. It ensures that an existing irrelevant escalation workflow is no longer associated with that task record.

See [Create an escalation trigger rule](../task/create-trigger-rule-oncall.md).

## About escalation policies

An escalation policy includes the following configurations:

-   The escalation audience \(roster members and managers\).
-   A policy type that defines the order in which rosters and roster members receive escalation notifications.
-   Other aspects of the escalation process like the contact methods to use and the number of reminders to send for each notification.

You can create a custom escalation policy for a shift by overriding settings in a default escalation type, for example, by configuring custom delays between escalation steps.

-   **[Configure a table for escalation trigger rules](../task/configure-tables-for-escalation-trigger-rule.md)**  
Configure escalation trigger rules for the tables that do not extend tasks.
-   **[Create an escalation trigger rule](../task/create-trigger-rule-oncall.md)**  
Create a trigger rule to specify both the conditions under which an escalation process should begin and the actions \(workflow or script\) to perform for the escalation.
-   **[Create an escalation policy](../task/create-custom-esc-policy-oncall.md)**  
An escalation policy includes the policy type that defines the order in which rosters and roster members receive escalation notifications. You can create a custom escalation policy for a shift by overriding settings in a default escalation type, for example, by configuring custom delays between escalation steps.
-   **[Escalation and reminder settings for rosters](../reference/escalation-remind-settings-oncall.md)**  
Use the escalation settings to specify how and when escalations occur and when reminder notifications are sent.
-   **[Example escalation reports](example-escalation-reports-oncall.md)**  
Because escalation reports depend on the escalation type, report content can vary greatly.

**Parent Topic:**[Escalations in On-Call Scheduling](escalations-oncall.md)

**Related topics**  


[Track the progress of an escalation](../task/track-escalation-progress-oncall.md)

[View details in an escalation log](../task/view-escalation-logs-oncall.md)


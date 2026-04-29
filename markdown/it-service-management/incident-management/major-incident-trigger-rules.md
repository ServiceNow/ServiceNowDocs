---
title: Create trigger rules for major incidents
description: Create trigger rules to define the conditions under which a trigger action is executed. You can create major incident trigger rules to define the conditions under which an incident is automatically considered as a major incident candidate.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing major incidents, Incident Management, IT Service Management]
---

# Create trigger rules for major incidents

Create trigger rules to define the conditions under which a trigger action is executed. You can create major incident trigger rules to define the conditions under which an incident is automatically considered as a major incident candidate.

## Before you begin

Role required: incident\_manager or admin

## About this task

Major incident trigger rules are evaluated asynchronously each time an incident is created or updated provided the following conditions are met:

-   The incident record doesn't have the Parent Incident populated, which means that the current incident isn't a child incident.
-   The major incident isn't proposed or accepted.
-   The incident is active.

**Note:** The base system major incident trigger rules are inactive by default.

## Procedure

1.  Navigate to **All** &gt; **Major Incidents** &gt; **Administration** &gt; **Major Incident Trigger Rules**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_wpx_bfq_kbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the trigger rule.

</td></tr><tr><td>

Table

</td><td>

Table on which the trigger rule executes.

</td></tr><tr><td>

Application

</td><td>

Application scope of the trigger rule. The trigger rule is available for all applications or for scoped applications.

</td></tr><tr><td>

Execution Order

</td><td>

The rule with lowest execution order is triggered first. In the following example, the rule with order = 100 is executed first.Example:

-   If business criticality of business service is 1-most critical or 2-somewhat critical, Order = 100.
-   If the number of child incidents is greater than 20, then Order = 200.
-   For a P1 incident, Order = 300.
 **Note:** If any of the existing trigger rule conditions are met, the incident is considered to be a major incident candidate. Verification of the remaining rules isn’t required. Otherwise, all the rules are verified based on the execution order.

</td></tr><tr><td>

Action to take

</td><td>

Action taken on the incident when the trigger rule is executed. The possible values are the following:-   **Propose Major Incident**: Incident is proposed as a major incident candidate when the trigger rule is executed. After it’s approved, the incident is promoted to a major incident.
-   **Promote Major Incident**: Incident is promoted directly to a major incident when the trigger rule is executed.
-   **Note:** The **Create major incident from candidate** \(**sn\_major\_inc\_mgmt.com.snc.incident .min.major\_incident\_creation**\) system property creates different behaviors depending on which options are selected.

When the system property is set to **Create new**, the following behaviors occur in relation to the **Action to take** values:

-   **Propose Major Incident**: The incident is proposed as a major incident candidate. After it’s approved, a new major incident is created and the incident is marked as its child.
-   **Promote Major Incident**: A new incident is created and promoted to a major incident. The existing incident is marked as its child.
When the system property is set to **Promote**, the following behaviors occur in relation to the **Action to take** values:

-   **Propose Major Incident**: The incident is proposed as a major incident candidate. After it’s approved, a new major incident is created and the incident is marked as its child.
-   **Promote Major Incident**: The existing incident is promoted to a major incident.


</td></tr><tr><td>

Active

</td><td>

Option to activate the trigger rule.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that must be met to execute the trigger rule.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Managing major incidents](../concept/major-incident-management.md)


---
title: Configure major incident trigger rules
description: Create and configure the trigger rules for a major incident to define the conditions for when a trigger action is executed. You can create major incident trigger rules to define the conditions under which an incident is automatically considered as a major incident candidate.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Major Incident Management in Service Operations Workspace, Setting up Major Incident Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure major incident trigger rules

Create and configure the trigger rules for a major incident to define the conditions for when a trigger action is executed. You can create major incident trigger rules to define the conditions under which an incident is automatically considered as a major incident candidate.

## About this task

Major incident trigger rules are evaluated asynchronously each time a major incident is created or promoted from an incident, provided the following conditions are met:

-   The incident record doesn't have the Parent Incident populated, which means that the current incident isn't a child incident.
-   The major incident isn't proposed or accepted.
-   The incident is active.

You can also configure major incident trigger rules to directly create a major incident, bypassing the candidate step.

**Note:** Base system trigger rules are available.

## Before you begin

The Major Incident Management plugin must be activated in Service Operations Workspace. For more information, see [Activate Major Incident Management in Service Operations Workspace](install-mim-sow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the Admin Center page, navigate to the configuration page for Major Incident Management through either the **Overview** tab or the **Configurations** tab.

    -   In the **Overview** tab, select the **Configure** button in the Major Incident Management section.
    -   In the **Configurations** tab, select **Major Incident Management**.
    The configuration page displays all configurable features in Major Incident Management. In the Trigger rules section, you can view the number of trigger rules that are configured and are currently active.

3.  On the Trigger rule section, select **Configure**.

    The Trigger rules page displays a list of available trigger rules. You can select any available trigger rule and select the following actions:

    -   Activate: Activates the selected trigger rule. The base system major incident trigger rules are inactive by default.
    -   Delete: Deletes the selected trigger rule.
    -   Deactivate: Deactivates the selected active trigger rule.
    -   Copy: Copies the trigger rule along with the information. This option helps in creating a trigger rule using the data of an existing trigger rule.
4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_rfz_kcw_y1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the trigger rule.

</td></tr><tr><td>

Table name

</td><td>

Table where the trigger rule is executed.

</td></tr><tr><td>

Action to take

</td><td>

Action taken on the incident when the trigger rule is executed. Possible values:

 -   **Propose Major Incident**: Incident is proposed as a major incident candidate when the trigger rule is executed. After it’s approved, the incident is promoted to a major incident.
-   **Promote Major Incident**: Incident is promoted directly to a major incident when the trigger rule is executed.
 **Note:** The **Create major incident from candidate** \(**sn\_major\_inc\_mgmt.com.snc.incident .min.major\_incident\_creation**\) system property creates different behaviors depending on which options are selected.

 When the system property is set to **Create new**, the following behaviors occur in relation to the **Action to take values**:

 -   **Propose Major Incident**: The incident is proposed as a major incident candidate. After it’s approved, a new major incident is created and the existing incident is marked as its child.
-   **Promote Major Incident**: A new incident is created and promoted to a major incident. The existing incident is marked as its child.
 When the system property is set to **Promote**, the following behaviors occur in relation to the **Action to take** values:

 -   **Propose Major Incident**: The incident is proposed as a major incident candidate. After it’s approved, it's promoted to a major incident.
-   **Promote Major Incident**: The existing incident is promoted to a major incident.


</td></tr><tr><td>

Application

</td><td>

Application scope of the trigger rule. The trigger rule is available for all applications or for scoped applications.

</td></tr><tr><td>

Execution order

</td><td>

The sequence that the rules are triggered. The rule with lowest execution order is triggered first. For example, a rule with order = 100 is executed first then a rule with order = 200.

 **Note:** If any of the existing trigger rule conditions are met, the incident is considered to be a major incident candidate. Verification of the remaining rules isn’t required. Otherwise, all the rules are verified based on the execution order.

</td></tr><tr><td>

Active

</td><td>

Option to activate the trigger rule.

</td></tr><tr><td>

Conditions

</td><td>

Condition builder to set conditions that must be met to execute the trigger rule.

</td></tr></tbody>
</table>6.  Select **Save**.

    The trigger rule is created and added to the list of available trigger rules.



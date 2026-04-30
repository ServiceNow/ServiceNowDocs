---
title: Create a time sheet policy
description: As a time card administrator, you can create a time sheet policy to define the requirements for time card users to record their time worked. The time card approvers must review and process time sheets under the applicable time sheet policy.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Time sheet policies, Time Card management, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a time sheet policy

As a time card administrator, you can create a time sheet policy to define the requirements for time card users to record their time worked. The time card approvers must review and process time sheets under the applicable time sheet policy.

## Before you begin

Role required: timecard\_admin

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Administration** &gt; **Time Sheet Policies**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="time_sheet_policy_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the policy.

</td></tr><tr><td>

Allow blank time cards

</td><td>

Option to enable submission of blank time cards for approval.

 By default, this option is not selected.

</td></tr><tr><td>

Auto create time card on planned task update

</td><td>

Option to create a time card automatically when you update a planned task, if the following conditions are true:

 -   You are a time card user
-   You are assigned to the task through **Assigned to** or **Additional assignee list** field
-   The task is not in a pending state.
 By default, this option is not selected.

</td></tr><tr><td>

Auto fill time card with time worked entries

</td><td>

Option to fill in time cards automatically when you enter time in the **Time worked** field on the Task form.

 If a time card does not exist for the task, one is created when the time worked is updated if the following conditions are true:

 -   You are a time card user.
-   You are assigned to the task through the **Assigned to** or **Additional assignee list** field.
 By default, this option is not selected.

</td></tr><tr><td>

Auto create time cards every week

</td><td>

Option to [generate time cards automatically](auto-generate-time-cards.md) every week through a scheduled job for all users assigned to the time sheet policy. The time cards are generated based on the planned task assignments and hard-allocated resource plans of the users.

 By default, this option is selected.

</td></tr><tr><td>

Update actual hours and cost in resource plan/reports

</td><td>

Option to update actual hours and actual cost of the associated resource plan based on the hours entered in the approved time card.

 When selected, you can associate a resource plan related to the selected task with the time card in the following ways:

-   If the task has multiple resource plans, you can select the appropriate plan.
-   If the task has one resource plan, that plan is selected by default.
 The hours from the time card entry and the hourly resource rate are used to update the **Actual hours** and **Actual cost** values of the associated resource plan.

**Note:** If the task has no resource plan, the associated records update the corresponding project.

 By default, this option is not selected.

</td></tr><tr><td>

Allow recall

</td><td>

Option to enable the recall action on a time sheet or time card after it is approved and processed.

 By default, this option is selected.

</td></tr><tr><td>

Recall period allowed \(days\)

</td><td>

Number of days within which you can recall a time sheet or time card.

 This field appears when the **Allow recall** option is selected.

 The default value is 30.

</td></tr><tr><td>

Week starts on

</td><td>

Start day of the week for the time sheet.

 The default value is Sunday.

**Note:** For more information on filtering Time Sheets using this field, see [KB0852458](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0852458) article in Now Support Knowledge Base.

</td></tr><tr><td>

Maximum hours per day

</td><td>

Maximum number of hours that can be entered each day in a time sheet.

 The default value is 24.

 Setting this field to -1 enables the resource to enter:

-   A value from 0 through 24 for the hours worked each day
-   A negative value, to correct the previously entered timecards.


</td></tr><tr><td>

Maximum hours per week

</td><td>

Maximum number of hours allowed in a week in a time sheet.

 The value for total hours for a week in a time sheet is the sum of hours entered per day of that week. If set to -1, the total hours per week allowed is up to 168 \(24 x 7\) hours.

 The default value is 40.

</td></tr><tr><td>

Non-project time approver

</td><td>

Type of approval required when you submit a time card that has a non-project task assigned.

 -   **Auto**: Time card is auto-approved when submitted.
-   **User Manager**: Time card is routed to the user manager for approval when submitted.

The user manager has the time card approver role and is also selected as the manager of the time card user on the User form.

-   **None**: A user with the timecard\_admin role can approve time cards when submitted.


</td></tr><tr><td>

Project time approver

</td><td>

Type of approval required when you submit a time card that has the project task.

 -   **Auto**: Time card is auto-approved when submitted.
-   **Project Manager**: Time cards for a project task are routed to the respective project manager for approval when submitted. The project manager is picked from the task against which you are submitting time.
-   **User Manager**: Time cards are routed to the user manager for approval when submitted.
-   **Both**: Time cards are routed to both the user manager and project manager for approval when submitted.

A time card remains in the Submitted state when only one of the approvers approves the time card.

-   **None**: A user with the time\_card admin role can approve time cards.
 **Note:**

-   The project manager and the user manager can view only those time cards that are routed to them for approval.
-   If the user manager or the project manager changes while the time card is still not approved, the system automatically updates the approver of the time card.
-   If the name of the project manager or the user manager is not populated on the respective form, a user with the time\_card admin role can approve time cards.


</td></tr><tr><td>

Allow multiple rate types

</td><td>

Option to provide a rate type in a time card to be used during expense line generation.When this option is selected, the **Rate type** field displays on the Time Card form to enable the selection of a rate type.

 For more information, see [Rate type in labor rate card](https://www.servicenow.com/docs/access?context=RateType&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

</td></tr><tr><td>

Default rate type

</td><td>

Rate type used by default for the time card.If you select none, the Standard rate type option is used.

 This field appears when the **Allow multiple rate types** check box is selected.

</td></tr><tr><td>

Default Policy

</td><td>

Option to set the time sheet policy as the default. The default policy is a global time sheet policy that applies to all users who are not assigned to any other time sheet policy.

 Only one time sheet policy can be set as the default.

 A time sheet policy set as the default policy cannot be deleted. You must first set another policy as the default policy.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

-   [Set the time sheet policy as the default policy](set-default-time-sheet-policy.md), if required.
-   [Assign the time sheet policy to users](assign-time-sheet-policy-to-user.md).

**Parent Topic:**[Time sheet policies](../concept/time-sheet-policies.md)


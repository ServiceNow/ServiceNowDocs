---
title: Create delegation rules
description: Specify which records are available for service delegation. Specify records by table name, by a condition, and by whether they are an approval or an assignment.
locale: en-US
release: yokohama
product: Granular Delegation
classification: granular-delegation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting up Granular Delegation, Granular Delegation, Employee Service Management]
---

# Create delegation rules

Specify which records are available for service delegation. Specify records by table name, by a condition, and by whether they are an approval or an assignment.

## Before you begin

Role required: delegation\_admin

If you have not done so already, create a delegation rule table. See [Add delegation rule tables](add-delegation-rules-tables.md).

## About this task

Administrators create delegation rules to allow the delegation of specific records. Access Control Rules \(ACLs\) determine if a delegate can access the records that match the delegation rules assigned to them. Creating delegation rules requires an administrator to be familiar with the data model of the delegated services.

**Important:** Granular delegation does not change a delegate's access to records. To access records, a delegate must already have the necessary roles. For example, to delegate task records, a delegate must have a role such as itil to access the Task table and its extensions.

## Procedure

1.  Navigate to **All** &gt; **Granular Delegation** &gt; **Delegation Rules**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_dcf_rpq_3nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Label for the delegation rule.

</td></tr><tr><td>

Application

</td><td>

Application associated with the delegation rule. This field is not editable and shows the application of your correct scope.

</td></tr><tr><td>

Short Description

</td><td>

Summary of the delegation rule. Provide enough detail that users can determine when to select the rule.

</td></tr><tr><td>

Active

</td><td>

Option for activating or deactivating a delegation rule.

</td></tr><tr><td>

Table

</td><td>

Type of records you want your delegate to access. Each delegation rule only applies to one table and does not apply to table extensions. Create a delegation rule for each table you want to grant a delegate access to.

</td></tr><tr><td>

Conditions

</td><td>

Filter applied to records in the table. Delegates can only access records that match these conditions.**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Approvals

</td><td>

Option to delegate approvals. Approval authority allows a delegate to approve or reject approval requests.

</td></tr><tr><td>

Assignments

</td><td>

Option to delegate assignments.

</td></tr></tbody>
</table>4.  Select **Save** or **Submit**.

    The **Delegation Rule** list returns with the **Delegates**, **Delegator User Criteria**, and **Delegate User Criteria** tabs.

    **Note:** If there are delegates using the rule, you cannot delete it and can only edit the **Name** and **Short description** fields.

    The **My Delegates** widget on the Employee Center does not appear unless there is an active delegation rule.

5.  Select the **Delegates** tab.

    Admins see a list of all delegates. You can select a delegate from the list and edit the start and end dates, notifications, and current delegation rules.

6.  Select the **Delegator User Criteria** tab to further define who can be a delegator.

7.  Select **Edit**.

8.  Use condition filters and you can select types of users that can be delegators for the delegation rule.

    For example, you can select **Active is true** and move **Managers** from the **Collection** column to the list on the right. This condition determines only active managers are eligible to be a delegator.

9.  Select **Save**.

10. Select the **Delegate User Criteria** tab to further define who can be a delegate.

11. Select **Edit**.

12. Use condition filters to select types of users that can be delegates for the delegation rule.

    For example, you can select **Active is true** and move **Users with 'sn\_hr\_core.case\_writer' role** from the **Collection** column to the list on the right. This condition determines only users with the HR case writer role can be a delegate.

13. Select Save.

    The **Delegation Rule** form returns.

14. Select **Update**.


## What to do next

Organize the delegation rules into categories to make delegating large batches of tasks easy and efficient for your employees. See [Create delegation rule categories](create-delegation-rule-categories.md).

Delegate assigned tasks for a specific period of time. See [Create a delegate](create-delegation-admin.md).

Employees can now delegate their assigned tasks to other employees. See [Delegate on-demand tasks](../concept/granular-delegation-use.md#).


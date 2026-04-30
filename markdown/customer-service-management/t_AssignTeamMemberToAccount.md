---
title: Assign a team member to an account
description: Assign a team member to an account by selecting an employee and their role or responsibility in the Customer Service Management \(CSM\) application. When you assign a team member to an account with account manager responsibility, they can view the information and perform actions on behalf of the accounts, such as creating or updating cases from the customer portal.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Creating an account team, Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Assign a team member to an account

Assign a team member to an account by selecting an employee and their role or responsibility in the Customer Service Management \(CSM\) application. When you assign a team member to an account with account manager responsibility, they can view the information and perform actions on behalf of the accounts, such as creating or updating cases from the customer portal.

## Before you begin

Role required: sn\_customerservice\_manager or admin

**Note:** CSM Contributor User \(com.snc.csm\_contributor\_user\) plugin must be installed.

## About this task

If you're the system administrator, you can assign a team member to an account from the Account Team Members related list on the Responsibility Definition form.

If you're the customer service manager, you can assign a team member to an account from the Account Team Members related list on the account or partner record.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Accounts** or **Partners**.

2.  Select an account.

3.  From the Account Team Members related list, select **New**.

    The account team member must have sn\_customerservice.relationship\_contributor role.

4.  On the form, fill in the fields.

<table id="table_jb3_qpg_q5"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Account

</td><td>

Account that the user is assigned to. If you're assigning a user from an account or partner record, this field is automatically filled in. If not, you can select an account from the Accounts list.

</td></tr><tr><td>

User

</td><td>

Employee selected to fulfill the role or responsibility.**Note:** Starting with the Vancouver release, the Service Organization External Staff \[sn\_csm\_service\_organization\_external\_staff\] can be added as Account Relationship Managers through Account Team Members \(Account Staff Relationships\).

</td></tr><tr><td>

Type

</td><td>

Defines the label for the relationship with the selected user. You can select the type from the list of related party configurations.**Note:** Starting with the Yokohama release, the **Type** field is added to the Account Team Member form. For more information on how to populate the **Type** field for existing data, see [Populate the Type field in relationship tables using the fix script](migration-of-account-manager-responsibility-access.md).

</td></tr><tr><td>

Responsibility

</td><td>

Role or responsibility selected for this employee.

</td></tr><tr><td>

Order

</td><td>

Specifies the sequence in which records are displayed, organized according to business preferences.

</td></tr></tbody>
</table>5.  Select **Submit**.



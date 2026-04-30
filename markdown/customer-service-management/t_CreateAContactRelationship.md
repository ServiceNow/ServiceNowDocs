---
title: Create a contact relationship for an account
description: Create a contact relationship for an account by selecting a contact and then assigning a responsibility to that contact in the Customer Service Management \(CSM\) application. Through this relationship, a contact can effectively manage the accounts and can execute actions on behalf of the associated accounts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Contact relationships, Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Create a contact relationship for an account

Create a contact relationship for an account by selecting a contact and then assigning a responsibility to that contact in the Customer Service Management \(CSM\) application. Through this relationship, a contact can effectively manage the accounts and can execute actions on behalf of the associated accounts.

## Before you begin

Role required: sn\_customerservice\_manager or admin

## About this task

Starting with the Zurich release, Customer Service Management \(CSM\) introduced the `Prevent duplicate for account-contact`business rule. By using this business rule, an administrator can assign multiple responsibilities per account for a contact.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Accounts** or **Partners**.

2.  Select an account.

3.  In the Contact Relationships related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_jb3_qpg_q5"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Account

</td><td>

The account to which the contact is assigned. This field is automatically filled in.

</td></tr><tr><td>

Contact

</td><td>

The customer contact selected to fulfill the role or responsibility.The Contacts list includes contacts from any related partner or account as well as contacts from the account hierarchy.

</td></tr><tr><td>

Type

</td><td>

Defines the label for the relationship with the selected user. You can select the type from the list of related party configurations.**Note:** Starting with the Yokohama release, the **Type** field is added to the Contact Relationship form. For more information on how to populate the **Type** field for existing data, see [Populate the Type field in relationship tables using the fix script](migration-of-account-manager-responsibility-access.md).

</td></tr><tr><td>

Responsibility

</td><td>

Role or responsibility selected for this customer contact.**Note:** As part of creating a responsibility definition, the admin can specify if the responsibility is unique. If so, the responsibility can only be assigned to one contact per account. For more information, see [Create account teams](../concept/configure-csm-account-teams.md).

</td></tr><tr><td>

Order

</td><td>

Specifies the sequence in which records are displayed, organized according to business preferences.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The contact name, account, and responsibility are added to the Contact Relationships related list.



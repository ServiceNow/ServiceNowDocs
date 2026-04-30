---
title: Create a recipients list
description: Create and save a list of users to receive targeted communications.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Targeted communications, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a recipients list

Create and save a list of users to receive targeted communications.

## Before you begin

Role required: sn\_publications.author, sn\_publications.admin, sn\_customerservice\_agent, sn\_customerservice\_manager, sn\_majorissue\_mgt.major\_issue\_manager

## About this task

A recipient list can include internal users, accounts, contacts, or consumers. Create a recipient list using any of the following methods:

-   By importing a list of users.
-   By creating a dynamic list based on selected conditions.
-   By creating a script.

Recipients lists can have both dynamically generated and manually added records of the same type.

**Note:** You must create at least one recipient list before creating a publication.

## Procedure

1.  Navigate to **All** &gt; **Targeted Communications** &gt; **Recipients Lists**.

2.  Select **New**.

3.  Fill in the fields on the Recipients List form.

<table id="table_mca_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the list.

</td></tr><tr><td>

Type

</td><td>

The type of recipients to include in the list.-   Contacts \(customer\_contacts\)
-   Internal Users \(sys\_user\)
-   Consumers \(csm\_consumer\)
-   Accounts \(customer\_account\)


</td></tr><tr><td>

State

</td><td>

The state of the recipient list. -   **New**: The list has not yet been generated. Select **Refresh Recipient List**.
-   **In Progress**: The list is generated. \(You can see only this state when generating a large list of recipients.\)
-   **Complete**: The list has been generated.


</td></tr><tr><td>

Method

</td><td>

The method used to generate the recipient list. -   **Upload File**: Create a list by uploading user information from a selected Excel .xlsx file.
-   **Dynamic Condition**: Create a list by selecting conditions in the condition builder or by adding a script.

**Note:** To exclude inactive users from receiving emails, use the condition builder to exclude inactive users from the recipients list.

</td></tr><tr><td>

Choose File

</td><td>

If the **Method** is **Upload file**, download an Excel template and then select an .xlsx file that contains the user information. The templates vary based on the entity selected in the **Type** field. For accounts, the template includes columns for sys\_id and account number values. For contacts, consumers, and internal users, the template includes columns for sys\_id and email values.

</td></tr><tr><td>

Show Script

</td><td>

If the **Method** is **Dynamic Condition**, enable this check box to create a recipients list using a script. Enabling this check box displays the **Script** field.

</td></tr><tr><td>

Script

</td><td>

The script used to create a recipients list.

</td></tr><tr><td>

Table

</td><td>

The table that stores the user information. Depending on the selection in the **Type** field, this field displays:-   Contact \[customer\_contact\]
-   User \[sys\_user\]
-   Consumer \[csm\_consumer\]
-   Account \[customer\_account\]


</td></tr><tr><td>

User Field

</td><td>

The field that references the user record in the User \(sys\_user\) table. For the following types of recipient lists, this is the sys\_id:

-   Contacts \(customer\_contacts\)
-   Internal Users \(sys\_user\)
-   Consumers \(csm\_consumer\)


</td></tr><tr><td>

Account Field

</td><td>

The field in the selected table that stores the account information.This field is displayed for the following types of recipients lists: **Accounts**.

</td></tr><tr><td>

Conditions

</td><td>

Use the buttons in this field to build one or more conditions on the selected table. A condition is made up of a selected field, an operator, and a value. Add conditions using the AND and OR buttons. Delete conditions by selecting the **Delete**button on the right side of a condition.

</td></tr></tbody>
</table>4.  Select **Submit**.

    For recipients list created by file upload, selecting **Submit** validates the records in the Excel file. Following validation, the system displays a pop-up window with the upload results, including valid and invalid user records.



---
title: Recipients List form
description: Description of the field values for the Recipients List form.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Recipients List form

Description of the field values for the Recipients List form.

<table id="table_uc3_hx2_5fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the recipients list.

</td></tr><tr><td>

Type

</td><td>

Type of users to include in the list. Possible values are:-   Contacts
-   Internal Users

 The selection of each type changes the dynamic conditions. For example, if you select **Internal Users**, the **Table** field displays the value as **User \[sys\_user\]**.

</td></tr><tr><td>

State

</td><td>

State of the recipients list.-   **New**: List has not yet been generated.
-   **In Progress**: List is currently being generated. \(You can see this state only when generating a very large list of recipients.\)
-   **Complete**: List is generated.

</td></tr><tr><td class="sub-head" colspan="2">

Setup

</td></tr><tr><td>

Method

</td><td>

Method used to generate the recipients list. Possible values are:-   `Upload File`: Upload an Excel file with the recipients list using the specified template.
-   `Dynamic Condition`: Run a script or condition builder to create the recipients list.

 **Note:** When the **Method** is `Dynamic Condition`, you can either use a script or a condition builder to create the recipients list.

</td></tr><tr><td>

Choose File

</td><td>

Allows you to download an Excel template, and then upload the Excel file with user information using the specified template.**Note:**

-   This field is available only if the **Method** is `Upload File`.
-   The templates vary based on the entity selected in the **Type** field. For accounts, the template includes columns for sys\_id and account number values. For contacts, consumers, and internal users, the template includes columns for sys\_id and email values.

</td></tr><tr><td>

Show Script

</td><td>

If selected, displays the script to create the recipients list.**Note:** This field is available only if the **Method** is `Dynamic Condition`.

</td></tr><tr><td>

Script

</td><td>

Script to create the recipients list.**Note:** This field is available only if the **Method** is `Dynamic Condition` and the **Show Script** check box is selected.

</td></tr><tr><td>

Table

</td><td>

Table that stores the user information. The table is selected based on the **Type** field.**Note:** This field is available only if the **Method** is `Dynamic Condition`.

</td></tr><tr><td>

User Field

</td><td>

Table field that refers to users. **Note:** This field is available only if the **Method** is `Dynamic Condition`.

</td></tr><tr><td>

Conditions

</td><td>

Condition builder to create the recipients list based on the specified table and user field. A condition is made up of a selected field, an operator, and a value. Add conditions using the AND and OR buttons. Delete conditions by clicking the Delete button to the right of a condition.**Note:** This field is available only if the **Method** is `Dynamic Condition`.

</td></tr></tbody>
</table>**Parent Topic:**[Surveys reference](survey-reference.md)

**Related topics**  


[Define a recipients list for surveys](../task/define-recipient-list.md)

[Create a recipients list](https://www.servicenow.com/docs/access?context=t_TargetCommCreateRecipientList&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)


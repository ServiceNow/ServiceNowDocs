---
title: Create field level restrictions
description: Set field level restrictions in DLP incidents to protect sensitive information from being exposed. You can use field level restrictions to control the users or groups who can access specific fields in the DLP incidents.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [DLP Incident Access Restrictions, Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create field level restrictions

Set field level restrictions in DLP incidents to protect sensitive information from being exposed. You can use field level restrictions to control the users or groups who can access specific fields in the DLP incidents.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

Field level restrictions enable you to display only certain fields for specific users or groups, providing a more granular way to control the data a user can access. You can create a Field level restriction by defining the DLP incident matching conditions, selecting the users or groups to which these conditions apply, and then choosing the DLP fields that these users or groups can view.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Incident Access Restrictions** &gt; **Field level restrictions**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_sjp_4fl_jtc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the field level restriction.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the field level restriction is active.

</td></tr><tr><td>

Execution order

</td><td>

Priority of the field level restrictions. This field indicates the order in which the field level restrictions are executed when two or more field level restrictions share the triggering conditions.The field level restriction with the lowest number has the highest priority.

 To set the order of operation, enter a value. For example, 100, 200, or any other number. The default value is 100.

</td></tr><tr><td>

Short description

</td><td>

Unique description for this field level restriction.

</td></tr><tr><td>

Incident matching condition

</td><td>

Options in the incident that matches the defined conditions. You can select any of the incident fields for defining the trigger condition for the field level restrictions.Use the lists and fields of the conditions builder to set the filters for the first row. To add more conditions, click **AND** or **OR**:

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
 To set a second filter condition, click **New Criteria**.

 For example, you can select the field as `Policy name`and set the condition as `in`, and `Name of the policy`.

**Note:** The conditions in the condition builder are case sensitive.

</td></tr><tr><td>

Applies to

</td><td>

Option to apply the incident matching conditions to specific users or groups. You can apply the conditions to the following:-   **All end users**: Option to select all end users to whom the DLP incident conditions are applicable.
-   **All reviewers of escalated incidents**: Option to select all reviewers of escalated incidents to whom the DLP incident conditions are applicable. This refers to all DLP incidents escalated to the Manager.
-   **Users**: Click the ![Lock icon](../image/dlp-lock-icon.png) icon to add a particular user from the list to whom the DLP incident conditions are applicable. You can also add a user by using their email address or search option. For example, Legal Manager.

To add yourself as the user to whom the DLP conditions are applicable, click the ![Add me icon](../image/dlp-addme-icon.png)

-   **Groups**: Click the ![Lock ic](../image/dlp-lock-icon.png) icon to add a particular group from the list to whom the DLP incident conditions are applicable. You can also add a group by using the search option. For example, Survey creators.


</td></tr><tr><td>

Allow access to following fields only

</td><td>

-   **DLP Fields**: Option to define the DLP fields that you want allow access to the selected users or groups. Select the DLP fields that you want to allow access to from the Available column and move them to the Selected column.

**Note:** The selected users or groups will be able to access only the selected DLP fields.

For example, you can select the**Assigned to** and **Opened** fields from the Available column and move them to the Selected column. Then, the selected users or groups have access only to the Assigned to and Opened fields.

-   **Upload attachments**: Option to indicate whether you want to allow the selected users or groups to upload attachments.
-   **Custom Fields**: Option to define the custom fields that you want allow access to the selected users or groups. You can view the custom fields that you have created under the Available column.

Select the custom fields that you want to allow access to from the Available column and move them to the Selected column.

**Important:**

    -   Custom fields for DLP incidents are supported only on the San Diego version or later.
    -   The selected users or groups will be able to access only the selected Custom fields.


</td></tr></tbody>
</table>    ![Set up field level restrictions for your DLP incidents](../image/dlp-field-restrictions.gif "DLP Field Level Restriction")

4.  Click **Submit**.


**Parent Topic:**[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)


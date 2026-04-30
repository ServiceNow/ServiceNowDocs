---
title: Create record level restrictions
description: Set record level restrictions in DLP incidents to protect sensitive records from being exposed. You can use record level restrictions to control the users or groups who can access specific records in the DLP incidents.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [DLP Incident Access Restrictions, Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create record level restrictions

Set record level restrictions in DLP incidents to protect sensitive records from being exposed. You can use record level restrictions to control the users or groups who can access specific records in the DLP incidents.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

Record level restrictions enable you to provide access to records only for specific users or groups, providing a more granular way to control the records a user can access. You can create a record level restriction by defining the DLP incident matching conditions, selecting the users or groups to which these conditions apply, and then choosing the DLP records that these users or groups can view.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Incident Access Restrictions** &gt; **Record level restrictions**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_sjp_4fl_jtc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record level restriction.

</td></tr><tr><td>

Short description

</td><td>

Unique description for this record level restriction.

</td></tr><tr><td>

Execution order

</td><td>

Priority of the record level restrictions. This field indicates the order in which the record level restrictions are executed when two or more record level restrictions share the triggering conditions.The record level restriction with the lowest number has the highest priority.

 To set the order of operation, enter a value. For example, 100, 200, or any other number. The default value is 100.

</td></tr><tr><td>

Allow access to incidents matching the condition

</td><td>

Options enable access to the incidents that matches the defined conditions. You can select any of the incident fields for defining the trigger condition for the record level restrictions.Use the lists and fields of the conditions builder to set the filters for the first row. To add more conditions, click **AND** or **OR**:

-   If **AND** is selected, all conditions must be matched.
-   If **OR** is selected, either condition can be matched.
 To set a second filter condition, click **New Criteria**.

**Note:** The conditions in the condition builder are case sensitive.

For example, you can select the field as `Active`and set the condition as `is`, and `true`.

</td></tr><tr><td>

Applies to

</td><td>

Option to apply record level restrictions to specific users or groups. You can apply the conditions as follows:-   **Users**: Click the ![Lock icon](../image/dlp-lock-icon.png) icon to add a particular user from the list to whom the selected record is applicable. You can also add a user by using their email address or search option. For example, Legal Manager.

To add yourself as the user to whom the record is applicable, click the ![Add me icon](../image/dlp-addme-icon.png). For example, System Administrator.

-   **Groups**: Click the ![Lock icon](../image/dlp-lock-icon.png) icon to add a particular group from the list to whom the selected record is applicable. You can also add a group by using the search option. For example, Survey creators.


</td></tr></tbody>
</table>    ![Set up record level restrictions for your DLP incidents](../image/dlp-record-restrictions.gif "DLP Record Level Restriction")

4.  Click **Submit**.


**Parent Topic:**[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)


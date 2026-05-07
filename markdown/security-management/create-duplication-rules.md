---
title: Create duplication rules in Security Operations
description: You can use Duplication Rules to identify new email, enrichment data, or field maps with active duplicate records and process them appropriately.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Shared data transformation, Security Operations common functionality, Security Operations]
---

# Create duplication rules in Security Operations

You can use Duplication Rules to identify new email, enrichment data, or field maps with active duplicate records and process them appropriately.

## Before you begin

Role required: sn\_sec\_cmn.write

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Duplication Rules**.

2.  Select **New**.

3.  Fill in the fields on the form, as appropriate:

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the duplication rule.

</td></tr><tr><td>

Table

</td><td>

Table where records are created and used to determine duplication.

</td></tr><tr><td>

Identifying fields

</td><td>

Select a set of fields that indicate a duplicate security incident, observable, vulnerability, and so on, when the values in these fields are identical.

</td></tr><tr><td>

Duplicate action

</td><td>

Governs how to handle duplicate emails. Choices are: -   **Create as child**

Creates a record as a child of the original. The field linking the child to the parent is the **Parent** field.

-   **Do not create nor update records**

\(default\) Does nothing. Ignores duplicates.

-   **Update duplicate record**

Updates the fields in the existing record as specified in **Duplication Actions.**

**Note:** If you choose **Update duplicate record**, the **Duplication Actions** related list appears.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the rule.

</td></tr><tr><td>

Description

</td><td>

Describes the purpose and application of this duplication rule; when it should be used, for example a rule designed for IP-based observable, or security incidents from the firewall.

</td></tr></tbody>
</table>4.  Select and hold \(or right-click\) in the record header and select **Save** or select **Update**.

5.  To set duplication actions, if you have chosen **Update duplicate record**, select **New** to create duplication actions for each field you want to update in the incident.

6.  Fill in or edit the fields on the form, to describe how to update the field:

<table id="table_dhf_nzm_jw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field

</td><td>

The name of the field to use for the duplication action.

</td></tr><tr><td>

Action

</td><td>

The actions supported vary by field type. Choices are:

-   **Update this field with the new value**

Replaces the previous value in the existing record with this value.

-   **Append the new value to a comma separated list, if unique**

Treats the value as an entry in a comma-separated list and adds the new data \(if any\) as a new entry in that list. If the data is already in the list, it is not added twice.

-   **Append the new value to this field**

Appends the new value to the end of the existing text in the field.

-   **Add one to a counter field**

Adds one to the numeric field.

-   **Set the field to today**

Sets the field to the current date and time.

-   **Append to related list**

Adds the related record with this value to the related list of the current record. Appears when there is a many-to-many table, with a column of the same type, linked to the table being updated.

For example, **Affected CI** or **Affected User**.

</td></tr><tr><td>

Relationship

</td><td>

\[Optional\] This field appears only when the **Append to related list** action is chosen. It is the name of the related list you want to associate with this rule.

</td></tr><tr><td>

Duplication rule

</td><td>

Rule that this action is part of.

</td></tr><tr><td>

Table

</td><td>

Table where records are created. Displays as information only.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the action.

</td></tr></tbody>
</table>7.  Select **Submit**.


**Parent Topic:**[Shared data transformation](../concept/shared-data-transformation.md)


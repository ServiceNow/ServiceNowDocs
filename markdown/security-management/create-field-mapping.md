---
title: Map tables to tables with Security Operations field mapping
description: Security Operations provides you with finer field-mapping granularity so you can map a Security Operations table to any other table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Security Operations field mapping, Security Operations common functionality, Security Operations]
---

# Map tables to tables with Security Operations field mapping

Security Operations provides you with finer field-mapping granularity so you can map a Security Operations table to any other table.

## Before you begin

Role required: sec\_cmn.write

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **Field Mapping**.

2.  Select **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the field map.

</td></tr><tr><td>

Source table

</td><td>

The table that provides the data to use to create a record in the destination table.

</td></tr><tr><td>

Duplication rule

</td><td>

Governs how to handle source records that would generate a duplicate record. For more information, see [Shared data transformation](../concept/shared-data-transformation.md).

</td></tr><tr><td>

Destination table

</td><td>

The table where new records are created.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the mapping. **Note:** Only one mapping between tables can be active at a time. If two maps contain the same tables, then the older version is automatically deactivated.

</td></tr><tr><td>

Description

</td><td>

Description for the field map.

</td></tr></tbody>
</table>4.  When you have completed your entries, select and hold \(or right-click\) in the form header and select **Save**.

    **Field Mapping Fields** tab appears. This record defines what data is placed in the target field, in records created by this field transform.

    ![Field Mapping form](../image/FieldMapping.png)

5.  Select **New**.

6.  Fill in the fields on the form, as appropriate.

<table id="choicetable_w4v_gmy_tz"><tbody><tr><td id="d148427e244">

**Field**

</td><td class="bold">

Description

</td></tr><tr><td id="d148427e253">

**Store value in a field or a related list**

</td><td>

Select where to find the value. Choices include:-   Add new value into a field in the record
-   Link to this value in a related list
-   Link to this value, creating a record if a matching record does not exist

**Note:** If the destination table does not have any related lists, this field is not displayed.

</td></tr><tr><td id="d148427e276">

**Field**

</td><td>

When **Store value in a field or related list** is set to **Add new value into a field in the record** this field specifies the field to fill in.**Note:**

For choice fields, matches are made to existing choices using the underlying choice label or value. If no match is found, the field is set, but no new entry is added to the choice list. For more information, see Choice lists.

For reference fields, an entry is set only when a value matching the display name of the record, or valid`sys_id` is found. For more information, see Reference fields.

</td></tr><tr><td id="d148427e315">

**Related list**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list** or **Link to this value, creating a new record if a matching record does not exist**, this field specifies the related list to add information to.

</td></tr><tr><td id="d148427e336">

**Value field**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list** or **Link to this value, creating a new record if a matching record does not exist**, this field specifies the field within the table displayed in the related list, that is used to look up and find an existing record. For example, if your related list is **Affected CIs**, this field may contain **Name** or **Fully Qualified Domain Name**, or any other field in the CI record that should be used to look up the CI is added to the **Affected CIs** list.

</td></tr><tr><td id="d148427e371">

**Relationship data**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list**, a new record is created to link that record \(such as a security incident\) to the value \(a CI, an observable, and so on\). This field specifies any additional information \(field and value pairs\) that should be added to that linking record. For example, adding an observable for a source IP, you can specify that this IP is the source, rather than destination IP. For multiple values, use a ^ separator, for example, type= Source IP^active=true.

</td></tr><tr><td id="d148427e389">

**New record data**

</td><td>

**When Store value in a field or related list** is set to **Link to this value, creating a new record if a matching record does not exist**, if a related record matching the parsed value is not found, a new record is created. This field specifies the static data to add to that record. For example, for **Affected CIs**, if we cannot find the CI, this setting indicates that a new CI is created\). The value found in the source record is set to the **Value** field in the CI record. You can set additional data – a note indicating why this CI was created, some information about what type of CIs you are working with. A sample would be: `description=Created by malware Incident report^type=autodetect`

</td></tr><tr><td id="d148427e413">

**Value separator**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list** or **Link to this value, creating a new record if a matching record does not exist**, this field specifies the separator to use for lists of items, commonly a comma or semicolon.

</td></tr><tr><td id="d148427e434">

**Value type**

</td><td>

When **Store value in a field or related list** is set to **Add new value into a field in the record** this field specifies the type of value. Choices include: -   **Source field record**
-   **Append to the field as a new line**
-   **Static value**
-   **Static value plus source record field value**


</td></tr><tr><td id="d148427e468">

**Source field**

</td><td>

Choose the source field that contains the value to be placed within the destination field or the selected related list.

</td></tr><tr><td id="d148427e477">

**Static field**

</td><td>

Static value for the field.

</td></tr><tr><td id="d148427e487">

**Value transform**

</td><td>

Choose the field value transformation entry to apply. It is used to map choice fields between records, for example, converting the set of **Category** choices for a security incident into the appropriate **Type** field for a Change Request.

</td></tr><tr><td id="d148427e502">

**Destination table**

</td><td>

Auto-populated with the destination table.

</td></tr><tr><td id="d148427e511">

**Field Mapping**

</td><td>

Auto-populated with the parent field map.

</td></tr><tr><td id="d148427e520">

**Source table**

</td><td>

Auto-populated with the source table.

</td></tr></tbody>
</table>7.  Click **Submit.**


**Parent Topic:**[Security Operations field mapping](../concept/field-mapping.md)


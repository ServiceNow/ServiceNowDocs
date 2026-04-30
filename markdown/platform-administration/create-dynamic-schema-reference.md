---
title: Create a dynamic schema reference
description: Add a reference field that points to the dynamic schema metadata that you've created.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Storing dynamic attributes on a record, Dynamic Schema, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a dynamic schema reference

Add a reference field that points to the dynamic schema metadata that you've created.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the table that you want use for storing dynamic attributes.

3.  In the Table Columns related list, select **New**.

4.  Create a reference to your dynamic schema for a group, multiple groups, category, or multiple categories.

<table id="choicetable_dx5_4lv_gbc"><thead><tr><th align="left" id="d277615e87">

Reference Type

</th><th align="left" id="d277615e90">

Steps

</th></tr></thead><tbody><tr><td id="d277615e96">

**Dynamic attribute group reference**

</td><td>

1.  In the Type field, select **Reference**.
2.  Enter a name for the dynamic attribute group that you're referring to in the Column label field.


</td></tr><tr><td id="d277615e117">

**Dynamic attribute groups reference**

</td><td>

1.  In the Type field, select **List**.
2.  Enter a name for the dynamic attribute groups that you're referring to in the Column label field.


</td></tr><tr><td id="d277615e138">

**Dynamic category reference**

</td><td>

1.  In the Type field, select **Reference**.
2.  Enter a name for the dynamic category that you're referring to in the Column label field.


</td></tr><tr><td id="d277615e159">

**Dynamic categories**

</td><td>

1.  In the Type field, select **List**.
2.  Enter a name for the dynamic categories that you're referring to in the Column label field.


</td></tr></tbody>
</table>5.  In the Reference Specification tab, select the dynamic schema element that contains the attributes you want to store on a record.

    -   Reference attributes in one or more dynamic attribute groups by selecting **Dynamic Attribute Group** in the Reference field.
    -   Reference attributes in one or more dynamic categories by selecting **Dynamic Category** in the Reference field.

## Add a reference to a dynamic attribute group

![Add a List field that references a dynamic attribute group.](../image/dynamic-schema-reference-example.png)

## What to do next

[Create a dynamic attribute store field](create-dynamic-attribute-store-field.md)

**Parent Topic:**[Storing dynamic attributes on a record](../concept/storing-dynamic-attributes.md)


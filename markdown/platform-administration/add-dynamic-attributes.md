---
title: Add dynamic attributes to a dynamic group
description: Define the dynamic attributes that describe a record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/add-dynamic-attributes.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Dynamic Schema, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add dynamic attributes to a dynamic group

Define the dynamic attributes that describe a record.

## Before you begin

Role required: admin

## About this task

After creating a dynamic attribute group, build out your taxonomy by specifying each dynamic attribute within the group.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Attributes** &gt; **Dynamic Attribute Groups**.

2.  Select the dynamic attribute group that you want to update.

3.  In the Dynamic Attributes related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_szt_vrp_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group

</td><td>

Dynamic attribute group that contains this attribute.

</td></tr><tr><td>

Label

</td><td>

Label used for displaying the dynamic attribute.

</td></tr><tr><td>

Name

</td><td>

Internal name for the dynamic attribute.

</td></tr><tr><td>

Type

</td><td>

Data type of the attribute.To optionally define the attribute using a choice set, select String.

</td></tr><tr><td>

Choice Set

</td><td>

Fixed set of values defined in a choice set. For example, if you created a choice set for Colors with choices for red, green, and blue, you can select the Colors choice set to limit the attribute's values to the color choices defined in the choice set. See [Create a dynamic choice set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/create-choice-set.md).

 This option only appears when you select String in the **Type** field.

</td></tr><tr><td>

Order

</td><td>

Value that determines the attribute's order in a list.

</td></tr><tr><td>

Description

</td><td>

A brief summary of what the attribute stores.

</td></tr><tr><td>

Active

</td><td>

Option to activate the dynamic attribute.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Add a dynamic attribute for product height

\[Omitted image "dynamic-attribute-example.png"\] Alt text: Add a dynamic attribute that captures the height of products.

## What to do next

Add more dynamic attributes to the dynamic attribute group as needed. For example, when defining metadata for products in the electronics category, you might add dynamic attributes for height, width, and depth.

**Parent Topic:**[Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/dynamic-schema.md)


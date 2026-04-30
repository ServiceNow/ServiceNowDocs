---
title: Create Data relationships
description: Create the data relationships in the Template Configurations module, which helps you to navigate from a record in the template configuration to any table. When you create these paths, you can fetch the necessary data from each of these records in the Operational Resilience report template.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-16"
reading_time_minutes: 1
breadcrumb: [Generating Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create Data relationships

Create the data relationships in the Template Configurations module, which helps you to navigate from a record in the template configuration to any table. When you create these paths, you can fetch the necessary data from each of these records in the Operational Resilience report template.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Digital resilience incident reporting** &gt; **Template Configurations**.

2.  In the Template Configurations module, open the template configuration that you created.

3.  Select **New** in the Data relationships related list.

    The Data relationship new record is displayed.

4.  Add the source and target relationships.

    A sample record is shown for reference.

    ![Data relationships.](../image/d17-dri-temp-config-data-rela-rel-list.png)

5.  On the form, fill in the fields.

<table id="table_zb5_hgc_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Level that you want to go to. For example, you can specify `Plan to Documentation`.

</td></tr><tr><td class="sub-head" colspan="2">

Source

</td></tr><tr><td>

Parent relationship

</td><td>

Parent of the data relationship.

</td></tr><tr><td>

Source table

</td><td>

Source table used for the data relationship created. This field is automatically set.

</td></tr><tr><td class="sub-head" colspan="2">

Target

</td></tr><tr><td>

Target relationship

</td><td>

Target relationship. You can select an existing relationship or create a relationship. For example, you can select `Plan to Asset dependencies`. **Note:** For more information, refer to Setting up the 360º views. You can register only existing relationships between the types of data you want to view.

</td></tr><tr><td>

Relationship type

</td><td>

Type of the relationship such as many to many or one to many. This field is automatically populated based on the selection made in the **Target relationship** field.

</td></tr><tr><td>

Target table

</td><td>

Table from which the data is obtained. This field is automatically populated.

</td></tr></tbody>
</table>6.  Select **Submit**.

    Based on the selections, the data is shown in the template.


## What to do next

Create content configurations to specify the type of data you want to fetch on the report. For more information, see [Set up the content configurations](../../grc-business-continuity-management/task/create-content-config-for-temp-config.md).


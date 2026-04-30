---
title: Create data relationships
description: Create a path to go from a record in the template configuration to any table that you require. When you create these paths, you can get the necessary data from each of these paths in your audit report template.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure document templates using Document Designer, Microsoft Word based audit report templates using Document designer, Common GRC features, Governance, Risk, and Compliance]
---

# Create data relationships

Create a path to go from a record in the template configuration to any table that you require. When you create these paths, you can get the necessary data from each of these paths in your audit report template.

## Before you begin

Role required: sn\_grc\_doc\_design.admin and sn\_audit.admin

## About this task

When you create data relationships, for example, for an audit engagement, you can specify how the issues, remediation tasks, test plans, and so on, are related to the record in the template relationship registry and you create a path to navigate to these respective records. You can create as many relationships as you require.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Report** &gt; **Template configurations**.

2.  Open the template configuration that you created.

3.  In the Data relationships related list, select **New**.

4.  On the form, fill in the field.

<table id="table_zb5_hgc_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Level that you want to go to. For example, you can specify `Engagement to issues`.

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

Select an existing relationship or create a target relationship. For example, you can select **Issues to engagement**. **Note:** For more information, refer to Setting up the 360º views. You can register only existing relationships between the types of data you want to view.

</td></tr><tr><td>

Relationship type

</td><td>

Type of the relationship such as many to many or one to many. This field is automatically populated based on the selection made in the **Target relationship** field.

</td></tr><tr><td>

Target table

</td><td>

Table from which the data is obtained. This field is automatically populated.

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

Create content configurations to specify the type of data you want to fetch on the report. For more information, see [Create content configurations](create-content-configurations.md).


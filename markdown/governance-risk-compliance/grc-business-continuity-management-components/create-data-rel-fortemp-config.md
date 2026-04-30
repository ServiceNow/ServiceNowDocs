---
title: Configure the data relationships
description: Configure the data relationships in the Template Configurations module, which helps you to navigate from a record in the template configuration to any table. When you create these paths, you can fetch necessary data from each of these records in the BCM report template.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up the template configurations, Generating reports using Document designer, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure the data relationships

Configure the data relationships in the Template Configurations module, which helps you to navigate from a record in the template configuration to any table. When you create these paths, you can fetch necessary data from each of these records in the BCM report template.

## Before you begin

Role required: sn\_grc\_doc\_design.admin and sn\_bcm.admin

## About this task

When you create data relationships, you can specify how selected records, such as plans to recovery teams or plans to related assets, are connected to the table \(for example, \[sn\_bcp\_plan\]\) in the template relationship registry. You can then establish a path to navigate to these respective records. You can create as many relationships as needed.

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **General Administration** &gt; **Template Configurations**.

2.  In the Template Configurations module, open the template configuration that you created.

3.  In the Data relationships related list, select **New**.

    The Data relationship new record is displayed.

    ![Data relationship new record.](../image/data-rela-new-record.png)

    You can add the source and target relationships.

    ![Source relationships.](../image/data-rel-record-source-rel-list.png)![Target relationships.](../image/data-rel-record-target-rel-list.png)

4.  On the form, fill in the fields.

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

Select an existing relationship or create a target relationship. For example, you can select `Plan to Asset dependencies`. **Note:** For more information, refer to Setting up the 360º views. You can register only existing relationships between the types of data you want to view.

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

    The Data relationships related list is shown in the example.

    ![Data relationships related list.](../image/data-rela-template-config.png)


## What to do next

Create content configurations to specify the type of data you want to fetch on the report. For more information, see [Set up the content configurations](create-content-config-for-temp-config.md).

**Parent Topic:**[Set up the template configurations](set-up-document-designer-templates.md)


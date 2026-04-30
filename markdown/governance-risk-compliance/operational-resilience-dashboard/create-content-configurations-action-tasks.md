---
title: Create Content configurations
description: Set up the content configurations in the Template Configurations module to define the data you want to view or fetch when creating a report template. You can configure it to display a list of records or aggregated data, such as a list of remediation tasks or top priority issues. You can fetch up to 200 records from any table.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-16"
reading_time_minutes: 2
breadcrumb: [Generating Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create Content configurations

Set up the content configurations in the Template Configurations module to define the data you want to view or fetch when creating a report template. You can configure it to display a list of records or aggregated data, such as a list of remediation tasks or top priority issues. You can fetch up to 200 records from any table.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Digital resilience incident reporting** &gt; **Template Configurations**.

2.  Open the template for which you want to create content configurations.

3.  On the Content configurations related list, select **New**.

    The Content configurations related list is shown in the example.

    ![Content configurations related list.](../image/content-config.png)

4.  On the form, fill in the fields.

<table id="table_zb5_hgc_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the content configuration. For example, List of remediation tasks.

</td></tr><tr><td>

Template configuration

</td><td>

Template configuration for which you're defining the content configuration. This field is automatically set based on the configuration that you selected in step 2.

</td></tr><tr><td>

Target table

</td><td>

Table from which data must be fetched.

</td></tr><tr><td>

Data relationship

</td><td>

Data relationship for which you want to create content configurations. Only the data relationships that you have previously created are available for selection.

</td></tr><tr><td>

Filter criteria

</td><td>

Filter criteria and the Aggregation criteria to be built as required.

</td></tr><tr><td>

Aggregation criteria

</td><td>

Aggregation query to be used for the content configuration record. Use Data columns and Intermediate filters related lists for the content configuration record.

</td></tr><tr><td>

Content block criteria

</td><td>

To specify table or data that you want to insert in the content block as a table, select the Content block criteria tab. In the Parent block configuration field, select the required content configuration.

 In the Data columns related list, specify the columns you want on the report from the table that you have selected. You can either specify the standard columns available or you can write a custom script for the column.

</td></tr></tbody>
</table>5.  Build the Filter criteria and the Aggregation criteria as required.

6.  To specify a table or data that you want to insert in the content block as a table, select the **Content block criteria** tab.

    1.  In the **Parent block configuration** field, select the required content configuration.

    2.  Select **Submit**.

7.  Choose which columns from the Data columns list to include in the report.

    You can either specify the standard columns available or you can write a custom script for the column.

    **Note:** You can add up to 20 columns in a table and in a content block. Similarly, certain content blocks can be repeated 200 times in Xanadu and 500 times in Zurich.

8.  Specify the order of the columns as they must appear on the report template.

9.  Select **Update**.

    The Content configurations related list is displayed.



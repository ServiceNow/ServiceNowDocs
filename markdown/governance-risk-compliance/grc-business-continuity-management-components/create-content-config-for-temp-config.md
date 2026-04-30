---
title: Set up the content configurations
description: Set up the content configurations in the Template Configurations module to define the data you want to view or fetch when creating a report template. You can configure it to display a list of records or aggregated data, such as a list of remediation tasks or top priority issues. You can fetch up to 200 records from any table.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up the template configurations, Generating reports using Document designer, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up the content configurations

Set up the content configurations in the Template Configurations module to define the data you want to view or fetch when creating a report template. You can configure it to display a list of records or aggregated data, such as a list of remediation tasks or top priority issues. You can fetch up to 200 records from any table.

## Before you begin

Role required: sn\_grc\_doc\_design.admin and sn\_bcm.admin

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **General Administration** &gt; **Template Configurations**.

2.  Open the template for which you want to create content configurations.

3.  On the Content configurations related list, select **New**.

    The Content configurations new record and its related lists are displayed.

    ![Content configurations new record.](../image/content-conf-new-record-filter-criteria.png)![Filter criteria.](../image/content-conf-new-record-filter-criteria.png)![Aggregation criteria.](../image/content-conf-sample-record-aggr-criteria.png)![Content block criteria.](../image/content-conf-sample-record-content-block-criteria.png)

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the content configuration. For example, `Asset dependencies`.|
    |Template configuration|Template configuration for which you're defining the content configuration. This field is automatically set based on the configuration that you selected in step 2.|
    |Target table|Table from which data must be fetched.|
    |Data relationship|Data relationship for which you want to create content configurations. Only the data relationships that you have previously created are available for selection.|
    |Filter criteria|Filter condition and the number of records that can be displayed.|
    |Aggregation criteria|Aggregation query to be used for the content configuration record. Use Data columns and Intermediate filters related lists for the content configuration record.|
    |Content block criteria|Parent block configuration to specify a table or data that you want to insert in the content block as a table|

5.  Build the Filter criteria and the Aggregation criteria as required.

6.  To specify a table or data that you want to insert in the content block as a table, select the **Content block criteria** tab.

    1.  In the **Parent block configuration** field, select the required content configuration.

    2.  Select **Submit**.

7.  In the Data columns related list, specify the columns you want on the report from the table that you have selected.

    You can either specify the standard columns available or you can write a custom script for the column.

    **Note:** You can add up to 20 columns in a table and in a content block. Similarly, certain content blocks can be repeated 200 times in Xanadu and 500 times in Zurich.

8.  Specify the order of the columns as they must appear on the report template.

9.  Select **Update**.

    The Content configurations related list is shown in the example.

    ![Content configurations related list.](../image/content-config-rel-list-template-config.png)


## What to do next

Create a scripted variable for the report. For more information, see [Define the scripted variables](create-scripted-vari-for-temp-config.md).

**Parent Topic:**[Set up the template configurations](set-up-document-designer-templates.md)


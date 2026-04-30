---
title: Create content configurations
description: Define the data that you want to view or fetch, whether it's a list of records or an aggregation when creating an audit report. For example, specify if you want to see a list of remediation tasks or the list of the top five high priority issues. A maximum of 200 records can be fetched from any table.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure document templates using Document Designer, Microsoft Word based audit report templates using Document designer, Common GRC features, Governance, Risk, and Compliance]
---

# Create content configurations

Define the data that you want to view or fetch, whether it's a list of records or an aggregation when creating an audit report. For example, specify if you want to see a list of remediation tasks or the list of the top five high priority issues. A maximum of 200 records can be fetched from any table.

## Before you begin

Role required: sn\_grc\_doc\_design.admin and sn\_audit.admin

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Report** &gt; **Template configurations**.

2.  Open the template for which you want to create content configurations.

3.  On the Content configurations related list, select **New**.

    ![](../image/template-configuration.png)

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the content configuration. For example, `List of remediation tasks`.|
    |Template configuration|Template configuration for which you're defining the content configuration. This field is automatically set based on the configuration that you selected in step 2.|
    |Target table|Table from which data must be fetched.|
    |Data relationship|Data relationship for which you want to create content configurations. Only the data relationships that you have previously created are available for selection.|
    |Filter criteria|Filter condition and the number of records that can be displayed.|
    |Aggregation criteria|Aggregation query to be used for the content configuration record. Use Data columns and Intermediate filters related lists for the content configuration record.|
    |Content block criteria|Parent block configuration to specify a table or data that you want to insert in the content block as a table.|

5.  Build the Filter criteria and the Aggregation criteria as required.

6.  To specify a table or data that you want to insert in the content block as a table, select the **Content block criteria** tab.

    1.  In the **Parent block configuration** field, select the required content configuration.

    2.  Select **Submit**.

7.  In the Data columns related list, specify the columns you want on the report from the table that you have selected.

    For more information, see [Configure Data columns](configure-data-columns.md).

8.  In the Intermediate filters related list, define the filters that should apply to the dataset to refine the results displayed in the report.

    For more information, see [Configure Intermediate filters](configure-intermediate-filters.md).

9.  Select **Update**.



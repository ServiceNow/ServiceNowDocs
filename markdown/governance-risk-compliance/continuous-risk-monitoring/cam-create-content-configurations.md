---
title: Create content configurations for CAM
description: Define the data that you want to view or fetch, whether it's a list of records or an aggregation when creating an ATO artifacts. For example, specify if you want to see a list of closed POA&amp;M or the list of system elements. A maximum of 200 records can be fetched from any table.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring ATO artifacts report templates using the Document Designer with Word add-in, CAM reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create content configurations for CAM

Define the data that you want to view or fetch, whether it's a list of records or an aggregation when creating an ATO artifacts. For example, specify if you want to see a list of closed POA&amp;M or the list of system elements. A maximum of 200 records can be fetched from any table.

## Before you begin

Role required: sn\_grc\_doc\_design.admin and sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **Template configuration**.

2.  Open the template for which you want to create content configurations.

3.  On the Content configurations related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the content configuration. For example, `List of remediation tasks`.|
    |Template configuration|Template configuration for which you're defining the content configuration. This field is automatically set based on the configuration you selected in step 2.|
    |Target table|Table from which data must be fetched.|
    |Data relationship|Data relationship for which you want to create content configurations. Only the data relationships that you have previously created are available for selection.|

5.  Build the Filter criteria and the Aggregation criteria as required.

6.  To specify table or data that you want to insert in the content block as a table, select the **Content block criteria** tab.

    1.  In the **Parent block configuration** field, select the required content configuration.

    2.  Select **Submit**.

7.  In the Data columns related list, specify the columns you want on the report from the table that you have selected.

    You can either specify the standard columns available or you can write a custom script for the column.

8.  Specify the order of the columns as they must appear on the ATO artifact report template.

9.  Select **Update**.


**Parent Topic:**[Configuring ATO artifacts report templates using the Document Designer with Word add-in](cam-configure-word-based-template.md)


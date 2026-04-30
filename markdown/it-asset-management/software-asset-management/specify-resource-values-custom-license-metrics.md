---
title: Specify resource values for your custom license metrics
description: If you create a custom license metric based on resource values, specify the resource value for each software product that you want to calculate licensing requirements for.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add a custom license metric, Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Specify resource values for your custom license metrics

If you create a custom license metric based on resource values, specify the resource value for each software product that you want to calculate licensing requirements for.

## Before you begin

Role required: sam\_user

## Procedure

1.  Open the Resource Value \[samp\_sw\_resource\_value\] table.

    -   If you're using the Software Asset Workspace, open the License operations view. From the License operations view, navigate to **Resource value** &gt; **Resource value**.
    -   If you're using the Software Asset Management classic application, navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Resource Value**.
2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the resource value.|
    |Software model|Software model of the software product that the resource value is associated with.|
    |Company|Company of the associated software product.|
    |Location|Physical location of the associated software product.|
    |Units consumed|Total number of resource value units that you are currently consuming of the associated software product. For example, if you are protecting 50 terabytes of data using a data protection software product, set the **Units consumed** field to `50`.|
    |Department|Department that the associated software product is assigned to.|
    |Cost Center|Cost center that is financially responsible for the associated software product.|

4.  Save the resource value.

    -   If you're using the Software Asset Workspace, select **Save**.
    -   If you're using the Software Asset Management classic application, select **Submit**.

## Result

When subsequent reconciliations run, the Software Asset Management application determines the license compliance position of the associated software product by comparing the value of the **Units consumed** field against the value of the corresponding **Licenses required** field in the License Metric Results \[samp\_license\_metric\_result\] table.

**Parent Topic:**[Add a custom license metric](add-custom-license-metric.md)


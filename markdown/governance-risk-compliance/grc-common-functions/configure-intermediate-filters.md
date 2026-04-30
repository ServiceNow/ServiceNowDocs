---
title: Configure Intermediate filters
description: Set up filters for intermediate data relationship nodes based on the selected data relationship in the content configuration. This ensures only relevant information is displayed, making reports clear and actionable.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [Create content configurations, Configure document templates using Document Designer, Microsoft Word based audit report templates using Document designer, Common GRC features, Governance, Risk, and Compliance]
---

# Configure Intermediate filters

Set up filters for intermediate data relationship nodes based on the selected data relationship in the content configuration. This ensures only relevant information is displayed, making reports clear and actionable.

## Before you begin

Role required: sn\_grc\_doc\_design.admin and sn\_audit.admin

## Procedure

1.  Navigate to the **Intermediate filters** related list.

2.  Select **New**.

3.  On the Data column new record form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Provide a unique name for the intermediate filter.|
    |**Content configuration**|Displays the name of the selected entity. This field is pre-populated and read-only. Select the info icon to preview the record.|
    |**Data relationship node**|Select the node that defines the relationship for filtering data.|
    |**Active**|Indicates whether the filter is active. Selected by default. If you want the filter to be inactive, you can deselect this check box.|
    |**Target table**|Displays the table associated with the selected node.|
    |**Condition**|Add filter conditions, OR clauses, or sorting options to define which records are included. Setting up conditions is optional.|
    |**Set record limit**|Enable this option to restrict the number of records returned.|

4.  Select **Submit**.



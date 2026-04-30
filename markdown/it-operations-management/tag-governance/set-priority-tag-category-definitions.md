---
title: Set the priority for tag category definitions for Tag Categorization
description: Set the priority for tag category definitions to ensure that tag keys belonging to multiple categories are properly categorized.
locale: en-US
release: yokohama
product: Tag Governance
classification: tag-governance
topic_type: task
last_updated: "2025-07-06"
reading_time_minutes: 1
breadcrumb: [Using Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Set the priority for tag category definitions for Tag Categorization

Set the priority for tag category definitions to ensure that tag keys belonging to multiple categories are properly categorized.

## Before you begin

Verify that you have installed version 1.16.3 of Service Mapping Plus to access to the CI tag category and CI tag key tables. For more information, see [Install Service Mapping Plus](../../service-mapping/task/install-service-mapping-plus.md).

Role required: admin

## About this task

A tag key can belong to multiple categories. Setting the priority ensures that Tag Categorization maps Configuration Items \(CIs\) and cloud resources to the correct category.

For example, the tag key Application might belong to both the Application and Cost Center tag categories. Set the priorities for the Cost Center and Application tag categories to 100 and 101, respectively, to prioritize mapping to the Application category. If a conflict occurs, this setting ensures that the Application category has higher priority and automatically maps the tag key to it.

## Procedure

1.  Navigate to **All** &gt; **Tag Governance** &gt; **Tag Categories**.

2.  Verify that you are in the leaf domain.

    1.  In the page header, select the globe icon ![](../../../reuse/icons/product-icons/globe-outline-24.svg).

    2.  Select **Domain scope**, and choose the appropriate leaf domain.

3.  Select the category definition for the tag category whose priority you want to set.

4.  In the Priority field, set the value.

5.  Select **Update** to save the change.

6.  If you want to apply your changes immediately rather than waiting for the automatic update within 24 hours, select the **Re-Categorize Tags** button.



---
title: Modify tag category information for Tag Categorization
description: Modify tag category definitions to support Tag Categorization and ensure that tag categories align with your requirements for data management and classification.
locale: en-US
release: yokohama
product: Tag Governance
classification: tag-governance
topic_type: task
last_updated: "2025-06-26"
reading_time_minutes: 1
breadcrumb: [Using Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Modify tag category information for Tag Categorization

Modify tag category definitions to support Tag Categorization and ensure that tag categories align with your requirements for data management and classification.

## Before you begin

Verify that you have installed version 1.16.3 of Service Mapping Plus to access to the CI tag category and CI tag key tables. For more information, see [Install Service Mapping Plus](../../service-mapping/task/install-service-mapping-plus.md).

Role required: tag\_governance\_admin

## Procedure

1.  Navigate to **All** &gt; **Tag Governance** &gt; **Tag Categories**.

2.  Verify that you are in the leaf domain.

    1.  In the page header, select the globe icon ![](../../../reuse/icons/product-icons/globe-outline-24.svg).

    2.  Select **Domain scope**, and choose the appropriate leaf domain.

3.  Select the category definition for the tag category you want to modify.

4.  In the **Regex** field, modify the definition.

    You can delete an existing value \(regex\) or add a new value \(regex\) in this field.

5.  Enter a value in the **Priority** field to set a priority for this tag category.

    Because a tag key can belong to multiple categories. setting the priority ensures that Tag Categorization maps CIs to the correct category.

6.  Select **Update** to save the changes.

7.  If you want to apply your changes immediately rather than waiting for the automatic update within 24 hours, select the **Re-Categorize Tags** button.



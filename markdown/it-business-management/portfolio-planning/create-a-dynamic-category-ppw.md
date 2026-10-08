---
title: Create a dynamic category
description: Create a dynamic category to define the custom fields that appear on demand records of a specific demand experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/portfolio-planning/create-a-dynamic-category-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [dynamic category, custom fields, demand experience, SPM]
breadcrumb: [Demand experiences, Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Create a dynamic category

Create a dynamic category to define the custom fields that appear on demand records of a specific demand experience.

## Before you begin

Identify the custom fields that demands of the demand experience need, and the data type of each field.

Role required: admin

## About this task

A dynamic category groups the dynamic attributes that appear as custom fields on demand records. When you assign the dynamic category to a demand experience, demand managers can view and update those fields in Next Experience for Demand Management. A category can have a parent category, and it inherits the attributes of its parent.

## Procedure

1.  Navigate to **All** &gt; **Enterprise-Wide Deployment** &gt; **SPM Dynamic Categories**.

    The Default SPM Dynamic Namespace record opens.

2.  Select the **Dynamic Categories** related list.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Namespace|Namespace that the dynamic category belongs to. This field is automatically set to Default SPM Dynamic Namespace.|
    |Label|Display name of the dynamic category. Use a name that identifies the demand experience that the category supports.|
    |Parent|Optional. Parent category whose attributes this category inherits. Leave this field empty to create a top-level category.|
    |Name|Unique system name of the dynamic category.|
    |Description|Brief description of the custom fields that the dynamic category provides.|

5.  Select **Submit**.

6.  Open the dynamic category and add the dynamic attributes that define its custom fields.

    Supported data types are String, Boolean, Date, Date/Time, Integer, Decimal, Floating point, Choice, and Reference. For a Choice attribute, select the choice set that provides its values. To create a dynamic attribute, see [Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-schema.md).


## Result

The dynamic category is available for demand experience configurations. Demands assigned to a demand experience that uses this category show its custom fields in Next Experience for Demand Management.

## What to do next

Associate the dynamic category with a demand experience. For more information, see [Create a demand experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-a-demand-experience-ppw.md).

**Related topics**  


[Enterprise-Wide Deployment for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/ewd-for-demands-ppw.md)

[Demand experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-experiences-ppw.md)


---
title: Create a category
description: Administrators and catalog administrators can create or edit a category.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service catalog categories, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a category

Administrators and catalog administrators can create or edit a category.

## Before you begin

Role required: admin

## About this task

To create or edit a category:

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Categories**.

    A list of existing categories appears. If the **Parent** field is blank, the category does not have a parent category.

2.  Click **New** or select the category to edit.

    **Note:** The visibility of a category is controlled by user criteria. See [Apply user criteria to items and categories](t_AppUserCritItemsCat.md#).

    ![Screenshot for the Service Catalog categories](../image/MaintainCategories.png "Service Catalog categories")

3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Title|Descriptive name for the category.|
    |Application|The application scope in which the category is applicable.|
    |Catalog|The catalog this category belongs to.|
    |Active|Check box to indicate that the category is available to add to the service catalog homepage.|
    |Location|Any location information relevant for the category.|
    |Parent|Any parent category for which this category is a subcategory.|
    |Description|Information about the category. The description appears when the category is collapsed on the service catalog homepage. The description also appears in the **Related Categories** list when a user clicks the parent category title.|
    |Icon|The small icon displayed beside the category name, when the category is listed as a subcategory.|
    |Header icon|The icon displayed beside the category header, when the category is a top-level category.|
    |Desktop image|A larger image to display with the category on the Service Catalog homepage. This image is visible only if the relevant renderer defines it to be used \(the default renderer does not display this field\).|
    |Classic Mobile image|A picture to use on Classic Mobile devices for this category. If a mobile image is not selected, the **Desktop image** appears if the **Classic Mobile Subcategory Render Type** is set to **Cards**.|
    |Classic Mobile Subcategory Render Type|The rendering option to control how subcategories are displayed. Select **List** for a single-column list, or **Cards** for a multi-column display.|
    |Hide description \(classic mobile browsing\)|Option for displaying the description at the top of the list on Classic Mobile devices.|


**Parent Topic:**[Service catalog categories](../concept/c_ServiceCatalogCategories.md)

**Related topics**  


[Configure dynamic categories](t_ConfigureDynamicCategories.md)


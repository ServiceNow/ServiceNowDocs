---
title: Create a safety control measure category
description: Create or modify a control measure category to group your safety controls into logical categories.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure settings, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Create a safety control measure category

Create or modify a control measure category to group your safety controls into logical categories.

## Before you begin

Role required: sn\_hs\_rm.hierarchy\_of\_controls\_manager or sn\_hs\_rm.hierarchy\_of\_controls\_writer

## Procedure

1.  Select **All**.

2.  In the navigation filter of the application navigator, enter the following command:

    `sn_hs_rm_hierarchy_of_controls.list`

    The Hierarchy of controls list appears.

3.  Create a control measure category or update an existing one.

    -   To create a category, select **New**.
    -   To modify an existing one, open it from the list.
4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|System-generated unique number for the control measure category.|
    |Name|Name of the category.|
    |Short description|Brief description of the category.|
    |Order|Order at which this category is listed on the Select control measures form when submitting a Job safety analysis \(JSA\).|
    |Active|Option to mark the category available for use. A control measure category must be active to be used.|

5.  Select **Submit**.


## Result

-   The control measure category is created and saved in the Hierarchy of controls \[sn\_hs\_rm\_hierarchy\_of\_controls\] table.
-   The category is listed in the **Control measure category** field on the Control measure form.
-   It is also displayed on the Select control measures form when submitting a Job safety analysis \(JSA\). However, a category with no control measures associated with it doesn't appear on the Select control measures form.

## What to do next

Associate related control measures with the category. For more information, see [Safety control measures](hs-define-controls.md).

**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)


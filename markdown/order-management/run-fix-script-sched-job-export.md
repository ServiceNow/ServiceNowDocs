---
title: Add Code field values to catalog entities
description: Add the Code field values for the main product catalog entities. The system uses this field as a way to identify catalog entities uniquely and to determine whether the Code field values for an export catalog entity are to be inserted or updated in the target instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exporting and importing product catalog entities, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Add Code field values to catalog entities

Add the **Code** field values for the main product catalog entities. The system uses this field as a way to identify catalog entities uniquely and to determine whether the **Code** field values for an export catalog entity are to be inserted or updated in the target instance.

## Before you begin

Role required: admin

## About this task

The **Code** values for product catalog entities are system-assigned alphanumeric values based on the catalog entity name, such as the name of a product offering. If the **Code** field values for the main catalog entities are empty, run certain on-demand scheduled jobs and fix scripts to add the **Code** field values for the main product catalog entities.

Both the scheduled jobs and fix scripts add the **Code** field values for the catalog entities.

## Procedure

1.  On the source instance, navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and do the following:

    1.  In the filter, enter `Application is Product Catalog Management Core`, then select **Run**.

        A list of jobs for Product Catalog Management Core is displayed.

    2.  Run each of the following jobs in the order listed below \(select the job, then select **Execute Now**\).

        -   **Migrate prod chars values to char options**
        -   **Schedule job to modify code field on characteristic records that contain special characters**
        -   **Schedule job to populate code field on master entities**
        -   **Schedule job to populate name field on product offering characteristics**
        -   **Schedule Job with upgrade script to populate code**
2.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

    1.  In the filter, enter `*code` to view the list of applicable fix scripts.

    2.  Run each of the following fix scripts \(select the script, then select **Run Fix Script**\).

        -   **Populate Code Field** - For Product Catalog Management Core application
        -   **Populate Code Field** - For Compatibility Management application
        -   **Populate Code Field** - For Attribute Propagation
        -   **Populate Code Field Decomposition Rule** - For Order Management application
        These scripts can be run in any order.

3.  Repeat Steps 1 through 2 on the target instance.


## Result

Your product catalog admin can export product catalog entities from the source instance and import them to the target instance.


---
title: Add Code field values to catalog entities after upgrading
description: Add the Code field values for the main product catalog entities. The system uses this field to determine whether the Code field values for an export catalog entity are to be inserted or updated in the target instance.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exporting and importing product catalog entities, Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Add Code field values to catalog entities after upgrading

Add the **Code** field values for the main product catalog entities. The system uses this field to determine whether the **Code** field values for an export catalog entity are to be inserted or updated in the target instance.

## Before you begin

Role required: admin

## About this task

In the Washington DC release, the **Code** field was added for the main product catalog entities. If the **Code** field values for these catalog entities are empty after upgrading to the Washington DC release, run both a fix script and an on-demand scheduled job to add the **Code** field values for the main product catalog entities.

The fix script adds the **Code** field values for characteristic options. The scheduled job adds the **Code** field values for product offerings, product offering catalog, and product, service, and resource specifications.

## Procedure

1.  On the source instance, navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Select the **Populate Code Field** and select **Run Fix Script**.

    The system runs the script, which adds the **Code** field value to characteristic options.

3.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

4.  Select the **Schedule job to populate code field on master entities** job.

5.  Verify that the **Run** field is set to On Demand and select **Execute now**.

    The system runs the job, which adds the **Code** field value for product offerings, product offering catalog, product offering categories, and product, service, and resource specifications.

6.  Select the **Schedule Job with upgrade script to populate code** job.

7.  Verify that the **Run** field is set to On Demand and select **Execute now**.

    The system runs the job, which adds the **Code** field value to the Product Catalog Management Core.

8.  Repeat Steps 1 through 7 on the target instance.


## Result

Your product catalog admin can export product catalog entities from the source instance and import them to the target instance.


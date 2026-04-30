---
title: Batch update for product specification versions
description: Use the inventory batch update job to update product specifications when changes occur from one version to another.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Updating specification versions, Specifications and product offerings, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Batch update for product specification versions

Use the inventory batch update job to update product specifications when changes occur from one version to another.

## Before you begin

Role required: product\_catalog\_admin and product\_catalog\_manager

## About this task

Batch inventory specification update lets catalog admins and product managers create an on-demand job that triggers a batch specification version update. The update doesn’t create change orders but directly updates product inventory in orders. Batch updates also create a log that including errors.

There are two steps to perform this process. The first is to update the specification version from the source version to the target version. The second step is to run an inventory upgrade job.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Product Specifications** and select the product specification you want to update.

    ![Image shows the Product Specification window that let managers update specification version.](../image/som-prod-spec-version-update.png)

2.  Select the **Create New Version** button to create a version of the specification.

3.  Select **Publish** to publish the specification version, then select **Update** to update the specifications to add the new version.

    Now there are two published versions of the specification. The initial version is considered the source version and the v2 version is considered the target version.

4.  To start the version update on existing product inventories, select **Upgrade Inventory** and select **Yes** at the prompt.

    The job is created for the source specification as v1 and the target is automatically populated as the latest published version of the source specification. The inventory upgrade job starts and runs a series of validation steps to confirm the job runs successfully. When the validation is complete, the job enters an **In progress** state. If an error occurs, the job status turns to **Error**.

5.  Navigate to **All** &gt; **Inventory upgrade job** and select the job you’re working with to view the status of the job and address any errors.

    ![Upgrade inventory job window that allows managers to view the progress of an inventory upgrade job.](../image/som-upgrade-inventory-job.png)

6.  Navigate to **All** &gt; **Inbound queue** &gt; **Inbound requests** and select the record id you’re working with to view the status.

    The number of inbound queue requests indicates the number of product inventories that matched the source specification. Once all the inbound queue records are processed, the request creates a change order for each of the inbound queue records processed successfully.


**Parent Topic:**[Updating specification versions](../concept/som-specification-version-update.md)


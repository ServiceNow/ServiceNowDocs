---
title: Request a new product or service
description: Request a new product or service to manage features and enhancements.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# Request a new product or service

Request a new product or service to manage features and enhancements.

## Before you begin

-   Identify, prioritize, and create a backlog of features and enhancements required for the product or service.
-   Define a roadmap of features and enhancements to be included across multiple releases.

Role required: sn\_dpr\_model.product\_manager

## About this task

-   The Product records are saved in the Application Models \[cmdb\_application\_product\_model\] table.

    If the application model has a corresponding business application, the **View Business Application** related link is displayed on the Product form. Select **View Business Application** to view details of the corresponding business application.

-   The Service records are saved in the Service Models \[cmdb\_service\_product\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(![Products and services icon.](../image/dpr-icon-products.png)\).

3.  Select **Request new** for a new product or service.

4.  In the dialog box, fill in the fields.

    For more information on the field descriptions, see [Request new product or service form](../reference/request-product-service-form.md).

5.  Select **Submit**.


## Result

-   A request is submitted to create a product or service.
-   The **DPR Service Catalog Request approval** flow is triggered that auto-approves the request and then triggers the **Request Product** flow that creates the product or service.

    **Note:** You can modify these flows in Workflow Studio according to your business needs.

-   The new product or service is listed in the Productsand Services list.
-   A DevOps app corresponding to the product or service is also created.

## What to do next

-   [Manage product hierarchy using Included products](dpr-manage-included-products.md).
-   Select the product or service name from the list to see details, plan releases, and manage data from external tools.

**Parent Topic:**[Using Digital Product Release](../concept/dpr-using-digital-product-release.md)


---
title: Decimal quantity support for service-based purchases in Shopping Hub
description: As a shopper, you can now specify decimal quantity values for service-based products when you create or edit a purchase requisition \(PR\) or purchase order \(PO\) in Shopping Hub.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [My purchases on Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Decimal quantity support for service-based purchases in Shopping Hub

As a shopper, you can now specify decimal quantity values for service-based products when you create or edit a purchase requisition \(PR\) or purchase order \(PO\) in Shopping Hub.

**Note:** This capability supports decimal quantities for service‑based products only. Applicable for both create and edit actions for both purchase requisitions and purchase orders in Employee Center and Shopping Hub.

## Key benefits

This functionality provides the following benefits:

-   You can specify decimal quantities for selected service-based products.
-   You can enable or disable decimal support for a service product by configuring its UOM.

**Important:** Starting with Yokohama Patch 12 and Zurich Patch 6, Shopping Hub supports decimal quantities for service-based products. If you upgraded to Yokohama Patch 12 or Zurich Patch 6 and cannot specify decimal quantities for services, you must run a script from the Scripts - Background module. For more information, see [Run the fix script to enable decimal quantities for services](../task/run-fix-script-decimal-qty.md).

## How to configure

Role required: sn\_shop.shopping\_hub\_admin

Plugin required: Shopping Hub \(sn\_spend\_uib\)

-   To enable this capability for a service product, you must configure a unit of measure \(UOM\) that supports decimal values.

    ![Supplier Products table showing Unit column with decimalSupported values for service products.](../image/sh-decimal-uom.png)

-   You control decimal quantity support at the UOM level. In the Unit of Measure Decimal Support decision table, set the decimalSupported attribute to true for the required UOM, as shown in the following image.

    ![Unit of Measure Decimal Support decision table with decimalSupported condition set to true.](../image/sh-decimal-dectable.png)

    **Note:** You can use decimal quantities only for products of type Service. You cannot specify decimal quantities for products of type Good, even if the UOM is configured to support decimal values.


## How it works

The following points describe how this capability works:

-   When you purchase a product of type Service, you can enter a decimal value in the Quantity field.

    ![Purchase form for product type Service showing decimal quantity 1.8 in the Quantity field.](../image/sh-decimal-service.png)

-   When you purchase a product of type Good, Shopping Hub prevents you from entering a decimal value in the Quantity field and displays an error message.

    ![Purchase form for product type Good showing decimal quantity 1.4 with error message "Decimal values are not supported".](../image/sh-decimal-good.png)

-   When you edit a PR or PO for a product of type Service, you can enter a decimal value in the New quantity field.

    ![Edit form for product type Service showing decimal quantity 1.7 in the New quantity field.](../image/sh-decimal-edit-service.png)

-   When you edit a PR or PO for a product of type Good, Shopping Hub prevents you from entering a decimal value in the New quantity field and displays an error message.

    ![Edit form for product type Good howing decimal quantity 1.4 with error message "Decimal values are not supported".](../image/sh-decimal-edit-good.png)


-   **[Run the fix script to enable decimal quantities for services](../task/run-fix-script-decimal-qty.md)**  
After upgrading to Yokohama Patch 12 or Zurich Patch 6, if you are unable to specify decimal quantities for services, you must run a background fix script to enable support for decimal quantities.

**Parent Topic:**[My purchases on Shopping Hub](my-purchases.md)


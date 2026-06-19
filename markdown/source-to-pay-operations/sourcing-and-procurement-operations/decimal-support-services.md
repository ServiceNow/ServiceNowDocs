---
title: Decimal quantity support for service-based purchases in Shopping Hub
description: As a shopper, you can now specify decimal quantity values for service-based products when you create or edit a purchase requisition \(PR\) or purchase order \(PO\) in Shopping Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/decimal-support-services.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 2
breadcrumb: [Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Decimal quantity support for service-based purchases in Shopping Hub

As a shopper, you can now specify decimal quantity values for service-based products when you create or edit a purchase requisition \(PR\) or purchase order \(PO\) in Shopping Hub.

## Key benefits

This functionality provides the following benefits:

-   You can specify decimal quantities for selected service-based products.
-   You can enable or disable decimal support for a service product by configuring its UOM.

**Note:** Starting with Yokohama Patch 12 and Zurich Patch 6, Shopping Hub supports decimal quantities for service-based products. If you upgraded to Yokohama Patch 12 or Zurich Patch 6 and cannot specify decimal quantities for services, you must run a script from the Scripts - Background module. For more information, see [Run the fix script to enable decimal quantities for services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/run-fix-script-decimal-qty.md).

## How to configure

Role required: sn\_shop.shopping\_hub\_admin

Plugin required: Shopping Hub \(sn\_spend\_uib\)

-   To enable this capability for a service product, you must configure a unit of measure \(UOM\) that supports decimal values.

    \[Omitted image "sh-decimal-uom.png"\] Alt text: Supplier Products table showing Unit column with decimalSupported values for service products.

-   You control decimal quantity support at the UOM level. In the Unit of Measure Decimal Support decision table, set the decimalSupported attribute to true for the required UOM, as shown in the following image.

    \[Omitted image "sh-decimal-dectable.png"\] Alt text: Unit of Measure Decimal Support decision table with decimalSupported condition set to true.

    **Note:** You can use decimal quantities only for products of type Service. You cannot specify decimal quantities for products of type Good, even if the UOM is configured to support decimal values.


## How it works

The following points describe how this capability works:

-   When you purchase a product of type Service, you can enter a decimal value in the Quantity field.

    \[Omitted image "sh-decimal-service.png"\] Alt text: Purchase form for product type Service showing decimal quantity 1.8 in the Quantity field.

-   When you purchase a product of type Good, Shopping Hub prevents you from entering a decimal value in the Quantity field and displays an error message.

    \[Omitted image "sh-decimal-good.png"\] Alt text: Purchase form for product type Good showing decimal quantity 1.4 with error message "Decimal values are not supported".

-   When you edit a PR or PO for a product of type Service, you can enter a decimal value in the New quantity field.

    \[Omitted image "sh-decimal-edit-service.png"\] Alt text: Edit form for product type Service showing decimal quantity 1.7 in the New quantity field.

-   When you edit a PR or PO for a product of type Good, Shopping Hub prevents you from entering a decimal value in the New quantity field and displays an error message.

    \[Omitted image "sh-decimal-edit-good.png"\] Alt text: Edit form for product type Good howing decimal quantity 1.4 with error message "Decimal values are not supported".


-   **[Run the fix script to enable decimal quantities for services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/run-fix-script-decimal-qty.md)**  
After upgrading to Yokohama Patch 12 or Zurich Patch 6, if you are unable to specify decimal quantities for services, you must run a background fix script to enable support for decimal quantities.

**Parent Topic:**[Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/shopping-hub-overview.md)


---
title: Activate the schedule flows
description: Activate the schedule flow that interacts with Coupa to pull information into your ServiceNow instance. You can pull information on primary data, supplier management, sourcing, invoice, and so on.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Activate the schedule flows

Activate the schedule flow that interacts with Coupa to pull information into your ServiceNow instance. You can pull information on primary data, supplier management, sourcing, invoice, and so on.

## Before you begin

Role required: sn\_coupa\_spoke.Coupa Admin

## Procedure

1.  Open **Run Trigger Coupa Integration**.

2.  Navigate to **Flow Designer** &gt; **Flow**.

3.  Select **Activate**.

4.  In the **Trigger** field, specify the time and interval at which you want to automatically run the scheduled flow.

    This flow in turn triggers the subflows to automate tasks. To customize the sample flow, copy it to the required application scope.

    The available subflows include:

    |Subflow|Description|
    |-------|-----------|
    |Look up legal entities from Coupa|Retrieves details of the legal entities in Coupa.|
    |Look up currencies from Coupa|Retrieves details of the currencies in Coupa.|
    |Look up conversion rates from Coupa|Retrieves details of the conversion rates in Coupa.|
    |Look up shipment notice using PO line id in Coupa|Retrieves details of the shipment notice using PO line ID in Coupa.|
    |Look up advance shipment notice after updated date in Coupa|Retrieves details of the advance shipment notice after updated date in Coupa.|
    |Create, update, and deactivate supplier in Coupa|Manage suppliers by creating, updating, and deactivating supplier in Coupa.|
    |Look up suppliers from Coupa|Retrieves details of the suppliers in Coupa.|
    |Create, update, and cancel purchase order in Coupa|Manage purchase orders by creating, updating, and canceling purchase order in Coupa.|
    |Look up purchase orders from Coupa|Retrieves details of the purchase orders in Coupa.|
    |Create and void goods receipt in Coupa|Manage goods receipt by creating and voiding goods receipt in Coupa.|
    |Look up receipts from Coupa|Retrieves details of the receipts in Coupa.|
    |Look up product catalogs from Coupa|Retrieves details of the product catalogs in Coupa.|
    |Create, update, and cancel invoice in Coupa|Manage invoices by creating, updating, and canceling invoice in Coupa.|
    |Look up invoices details from Coupa|Retrieves details of the invoices in Coupa.|
    |Look up Invoice payment details|Retrieves details of the Invoice payment in Coupa.|
    |Create sourcing event|Manage sourcing event by creating sourcing events in Coupa.|
    |Look up sourcing events from Coupa|Retrieves details of the sourcing events in Coupa.|
    |Award purchase|Retrieves details of the Award purchase in Coupa.|

    **Note:**

    If you want to change the configurations that are shipped along with Source-to-Pay Integration with Coupa, you can edit the subflows.

    Once data is pulled into staging tables, the transform maps move data into target tables. For more details, refer to [Source-to-Pay integration framework transform maps and subflows](../../sourcing-procurement-operations/concept/s2p-transform-maps-flows.md).


**Parent Topic:**[Configure Source-to-Pay integration with Coupa](../concept/configuring-source-to-pay-coupa-integration.md)

**Related topics**  


[ERP Source Configuration for Coupa](../concept/erp-source-configuration-coupa.md)

[Define an ERP source configuration for Coupa](define-erp-source-coupa.md)

[Configure integration services for Coupa](configure-service-maps-coupa.md)

[Looking up primary data in Coupa](../concept/look-up-primary-data-coupa.md)


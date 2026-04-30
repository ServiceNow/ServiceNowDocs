---
title: Spendint API
description: The Spendint API provides endpoints that push the catalog, price, availability, order, shipment, and invoice information from a third party to the ServiceNow instance. This API is part of the Source-to-Pay Integration Framework application.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Spendint API

The Spendint API provides endpoints that push the catalog, price, availability, order, shipment, and invoice information from a third party to the ServiceNow instance. This API is part of the Source-to-Pay Integration Framework application.

This API requires the Procurement Integration Framework \(com.glide.sn\_spend\_intg\) store application and is provided within the `sn_spend_intg` namespace. For information, see [Procurement File Transfer Framework](../../../product/sourcing-procurement-operations/concept/procurement-file-transfer-framework.md).

To access this API, you must have the sn\_spend\_intg.procurement\_integrator role.

-   **[Third-party registration for PIF and PFTF](../../../product/sourcing-procurement-operations/reference/third-party-registration-for-pif-pftf.md)**  
Onboard a supplier through the third-party registration process before you get started with Source-to-Pay Integration Framework \(PIF\) or Procurement File Transfer Framework \(PFTF\).
-   **[Spendint API - POST /sn\_spend\_intg/spendint/catalog](../reference/spendint-POST-catalog.md)**  
Allows suppliers to post multiple catalogs for creating supplier products, model products, contracts, and pricing records.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/price](../reference/spendint-POST-price.md)**  
Updates any pricing for supplier product records.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/availability](../reference/spendint-POST-availability.md)**  
Updates the availability for supplier product records.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/orderack](../reference/spendint-POST-orderack.md)**  
Updates order information for when a user shops for a product from a third-party catalog. When the user checks out, a purchase line is created so that approvals or other tasks for the purchase can be completed.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/shipment](../reference/spendint-POST-shipment.md)**  
Use this endpoint to accept updates on purchases from third parties.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/invoice](../reference/spendint-POST-invoice.md)**  
Accepts invoices from third-party providers.

**Parent Topic:**[Integrating Sourcing and Procurement Operations with other applications](../../../product/sourcing-procurement-operations/concept/integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with Employee Center](../../../product/sourcing-procurement-operations/concept/employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](../../../product/sourcing-procurement-operations/concept/psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](../../../product/sourcing-procurement-operations/concept/better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Project Management](../../../product/sourcing-procurement-operations/concept/integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Celonis](../../../product/sourcing-procurement-operations/concept/integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](../../../product/sourcing-procurement-operations/concept/integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](../../../product/sourcing-procurement-operations/concept/integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../../../product/sourcing-procurement-operations/reference/erp-source-val-spo-objects.md)

[Procurement File Transfer Framework](../../../product/sourcing-procurement-operations/concept/procurement-file-transfer-framework.md)


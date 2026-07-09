---
title: Spendint API
description: The Spendint API provides endpoints that push the catalog, price, availability, order, shipment, and invoice information from a third party to the ServiceNow instance. This API is part of the Source-to-Pay Integration Framework application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/spendint-api.html
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Spendint API

The Spendint API provides endpoints that push the catalog, price, availability, order, shipment, and invoice information from a third party to the ServiceNow instance. This API is part of the Source-to-Pay Integration Framework application.

This API requires the Procurement Integration Framework \(com.glide.sn\_spend\_intg\) store application and is provided within the `sn_spend_intg` namespace. For information, see [Procurement File Transfer Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/procurement-file-transfer-framework.md).

To access this API, you must have the sn\_spend\_intg.procurement\_integrator role.

-   **[Third-party registration for PIF and PFTF](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/third-party-registration-for-pif-pftf.md)**  
Onboard a supplier through the third-party registration process before you get started with Source-to-Pay Integration Framework \(PIF\) or Procurement File Transfer Framework \(PFTF\).
-   **[Spendint API - POST /sn\_spend\_intg/spendint/catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/spendint-POST-catalog.md)**  
Allows suppliers to post multiple catalogs for creating supplier products, model products, contracts, and pricing records.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/price](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/spendint-POST-price.md)**  
Updates any pricing for supplier product records.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/spendint-POST-availability.md)**  
Updates the availability for supplier product records.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/orderack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/spendint-POST-orderack.md)**  
Updates order information for when a user shops for a product from a third-party catalog. When the user checks out, a purchase line is created so that approvals or other tasks for the purchase can be completed.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/shipment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/spendint-POST-shipment.md)**  
Use this endpoint to accept updates on purchases from third parties.
-   **[Spendint API - POST /sn\_spend\_intg/spendint/invoice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/spendint-POST-invoice.md)**  
Accepts invoices from third-party providers.

**Parent Topic:**[Integrating Sourcing and Procurement Operations with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with IT Asset Management]()

[Sourcing and Procurement Operations integration with Employee Center]()

[Sourcing and Procurement Operations integration with third-party sourcing solutions]()

[Sourcing and Procurement Operations integration with Third-party Risk Management]()

[Sourcing and Procurement Operations integration with Project Management]()

[Sourcing and Procurement Operations integration with Celonis]()

[Sourcing and Procurement Operations integration with Field Service Management]()

[Source-to-Pay Operations integration with Contract Management Pro]()

[ERP source validation on Sourcing and Procurement Operations objects]()

[Procurement File Transfer Framework]()


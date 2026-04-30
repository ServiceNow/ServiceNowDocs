---
title: Tax calculations
description: A framework to integrate tax calculations into Sourcing and Purchasing Automation is implemented such that approvals can be done on the full value of purchases.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Tax calculations

A framework to integrate tax calculations into Sourcing and Purchasing Automation is implemented such that approvals can be done on the full value of purchases.

## Tax estimates from Shopping Hub administrator

A Shopping Hub administrator can configure tax estimates to be included in purchase requests for the approval process. This is enabled through a system property sn\_shop.tax.estimate.inclusion, which is included in purchase request approvals. If this inclusion is marked as true, the tax estimate from the cart line or checkout is included as a field in the purchase line and in the total line amount. However, if this inclusion is marked as false, not only would tax be excluded in the purchase request approval process, but also not calculated at checkout. This applies even when a customer has made the effort to set up the tax calculation API, but has not marked the purchasing property to true.

**Note:** When a purchase request becomes a purchase order, the tax estimate is not included in the total amount.

## Tax calculation integration process

-   Tax integration is triggered when a shopper adds a product to the cart, and the sn\_shop.tax.estimate.inclusion property to include tax in the purchase request approval process is marked as true.
-   A flow designer tax estimate responsible for making the API call, is triggered.
-   The flow designer evaluates if the SAP integration in configured or not.
-   If the SAP integration is configured, the flow designer sends the relevant parameter information to the SAP tax engine API, and receives the retrieved tax information to the calling function.
-   The received tax estimate is updated in the cart line as well as on the final checkout page.
-   If the SAP integration is not configured or there are integration errors, the flow designer does not receive any information from the SAP API, and the estimated tax is reflected as undetermined.

    **Note:** Here, the customer is open to integrate with any other tax engine, as desired.


-   **[Tax calculation API](tax-calculations-api.md)**  
A tax calculation API is created to provide specific parameters to a tax calculator engine, SAP in this case.
-   **[Tax calculation integration with SAP](tax-calculation-integration-sap.md)**  
SAP's tax engine API consumes necessary parameters from the tax calculation generic API to provide tax estimates.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)


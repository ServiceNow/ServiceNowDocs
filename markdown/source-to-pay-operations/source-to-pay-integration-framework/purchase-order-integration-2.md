---
title: Purchase order integration
description: Purchase orders are created in Source-to-Pay \(S2P\) and synchronized to the ERP system asynchronously.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase order integration

Purchase orders are created in Source-to-Pay \(S2P\) and synchronized to the ERP system asynchronously.

As there are several key concepts that are specific to the ERP system but are not captured in S2P, the following configurations in S2P are prerequisites to ensure successful execution of the integration:

-   ERP Address Mapping: This table stores the mapping between a delivery location in S2P and a plant in the ERP system. Additional address identifier columns are available in this table to allow customers map an address in S2P to other entities in the ERP system.
-   ERP Asset Category Mapping: This table stores the mapping between a capitalization policy in S2P and an asset class in the ERP system. The asset class is populated based on the value that was mapped to the corresponding capitalization policy that triggered the creation of the fixed asset in S2P.
-   ERP Material Group Mapping: This table stores the mapping between a model category in S2P and a material group in the ERP system. Depending on the model category associated to the supplier product in a purchase order line within S2P, the appropriate model category is populated in the ERP system.
-   Account assignment category configuration: To accommodate prepayments and the ability to store multiple general ledger accounts on a purchase order line in the ERP system, configuration has to be done to either introduce a net new Account Assignment Category in the ERP system that has this feature enabled, or update an existing one.

**Note:** The ERP integration mapping tables can be accessed through the primary data by a procurement administrator alone.

## Process flow

-   On final review of a purchase requisition, a purchase order and fixed assets, if applicable, are created in S2P, triggering the integration with the ERP system.
-   Attachments, if any, with valid sys-ids, are copied from the Inbound Purchase Order staging table record to the Purchase Order primary table record. This is done through a transform script, which is part of the Order stage transform map, triggered onAfter.
-   If there is an integration error, an integration error purchasing task is created on the purchase requisition. This contains the error message from the ERP system to inform the procurement specialist what must be updated.
-   If a purchase order line is being inserted by the ERP system with no corresponding purchase order in S2P, your administrator gets an error message. They can run the 'Retrigger failed order line import set records' scheduled job to re-trigger the error purchase order line records that have not been imported due to the absence of the purchase order. For more information on integration error handling, see [Integration errors in staging tables](../../accounts-payable-operations/concept/integration-errors-in-staging-tables.md).
-   Purchase orders are not created in the ERP system until the integration error is resolved in S2P. At this juncture, the status of the purchase order and purchase requisition in S2P is set to Pending Submission.
-   Additional form sections, fields, and mapping tables are created in S2P for integration purposes.
-   On successful purchase order creation in the ERP system, a purchase order ERP number and purchase order line ERP number are returned and synchronized back to the appropriate record in S2P.
-   If a capitalization policy is satisfied, fixed assets are created in the ERP system and the ERP number is synchronized back to S2P.
-   Purchase order revisions in S2P do not result in a new purchase order creation in the ERP system. The existing purchase order is updated to reflect the revised information. The buttons to update a purchase order are turned off when the integration status in the Outbound Order \[sn\_spend\_intg\_outbound\_purchase\_order\] staging table is New or In Process.
-   Cancellation of a purchase order in S2P moves the status of the purchase order to Pending Submission. When the integration is successful in the ERP system, the purchase order is canceled.
-   Blanket purchase orders are not created in the ERP system as it is a pre-approved list of users who do not have to go through the approval process when they purchase against the blanket purchase. Also, there are no financial documents associated with blanket purchase orders in S2P.
-   Purchase order releases are created in the ERP system.
-   Invoices and receipts are created against the standard purchase order releases in S2P, and as such, created as standard purchase orders in the ERP system as well.

## Purchase order line split scenario

Multiple purchase order lines are created from a single purchase line if the following conditions are met:

-   Purchase is integrated with the ERP system
-   Purchased quantity is 100 or more
-   Purchase is capitalized, for example, fixed assets created for the purchase

If multiple purchase order lines must be created, the first purchase order line can have a maximum purchased quantity of 99, and the remainder should go into the next purchase order line\(s\), none exceeding 99. You can create as many purchase order lines as required to cover the quantity of products purchased.

For example, if a purchase line purchased quantity is 250, which is capitalized and integrated with the ERP system, the purchase order lines are split as follows:

-   POL1001: Purchased quantity = 99
-   POL1002: Purchased quantity = 99
-   POL1003: Purchased quantity = 52

**Note:** Each purchase order line created here must reference the same purchase line, and the fixed assets created must reference the appropriate purchase order line.


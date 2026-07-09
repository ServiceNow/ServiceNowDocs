---
title: Considerations for implementing the Asset Management and SPO better together flow
description: This section provides information on considerations for implementing the Asset Management and SPO better together solution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-key-consideration.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sourcing and Procurement Operations and Asset Management integration, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Considerations for implementing the Asset Management and SPO better together flow

This section provides information on considerations for implementing the Asset Management and SPO better together solution.

<table id="table_id2_tj3_tfc"><thead><tr><th>

Functional detail

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PO and PR transaction behavior

</td><td>

To enable seamless integration:

 -   The **Cancel** and **Order** options are disabled for POs in Asset Management.
-   Edit and return flows for Purchase Requisitions \(PR\) and Purchase Orders \(PO\) in SPO are not supported in this integration. Therefore, the **Confirm Revision** option is disabled when the PR is in the Pending Review state.

</td></tr><tr><td>

Acknowledging asset receipt in Asset Management

</td><td>

-   After asset delivery, the purchaser acknowledges receipt via the PO in Asset Management. Assets are then created and can be viewed under the **Assets** tab of the Asset Management PO.
-   In this workflow, no assets or receipts are created from the SPO PO.
-   A read-only receipt is generated on the SPO POL only after the Asset Management receipt slip is created.

</td></tr><tr><td>

Shopping Hub and Asset Management

</td><td>

As part of this flow, all asset, consumable, and enterprise purchases should go through the service catalog. Services purchases should continue to flow through Shopping Hub.

Shopping Hub controls should prevent asset purchases directly from the Shopping Hub catalog.

</td></tr><tr><td>

Supplier Product and Vendor Catalog Item table usage

</td><td>

When a purchase is initiated using the Asset Management and SPO flow, the system doesn't use the Vendor Catalog Item \(pc\_vendor\_cat\_item\) table. Instead, it uses SPO's Supplier Product \(sn\_shop\_supplier\_product\) table to process the purchase.

</td></tr><tr><td>

How Asset Management and SPO better together flow affects SAM-Coupa integration

</td><td>

The Asset Management and SPO integration flow does not support the Software Asset Management \(SAM\) and Coupa integration. If you are currently using the SAM-Coupa integration and wish to continue doing so, do not install the Asset Management Integration for Sourcing and Procurement Operations \(sn\_spend\_asset\) plugin.If you choose to install the better together application, complete the following steps to successfully implement the SPO-Coupa integration:

-   Stop the "Create a Requisition" business rule from triggering on the Asset Management Purchase Order table \(proc\_po\) when the status changes to Ordered.

-   Restrict the creation of new itam\_procurement\_integration\_job scheduled jobs. Retire any existing daily jobs to avoid potential conflicts.

-   Delete all business rules associated with the app-itam-procurement-integration application to prevent integration conflicts.
-   Ensure that Purchase Requests \(PRs\), Purchase Orders \(POs\), and Receipts in SPO are properly mapped to corresponding entities in Coupa for seamless integration.

</td></tr><tr><td>

Creation of assets for services

</td><td>

The creation of inventory assets for services in the alm\_asset table is disabled in the Sourcing and Purchasing Automation and Asset Management Integration for Sourcing and Procurement Operations plugins. The previously created inventory assets for services are not affected. For fixed assets, Asset Management continues to create corresponding records in the alm\_asset table for services. Inventory asset creation for goods continues to function as before.

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing and Procurement Operations integration with Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-itam-better-together.md)


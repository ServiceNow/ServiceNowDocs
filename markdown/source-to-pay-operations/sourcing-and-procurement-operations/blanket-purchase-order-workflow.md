---
title: Blanket purchase order workflow
description: During checkout, when a shopper selects I am not sure in the delivery date option, it creates a purchase requisition with a blanket order type, which results in the creation of a blanket purchase order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/sourcing-and-procurement-operations/blanket-purchase-order-workflow.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 4
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Blanket purchase order workflow

During checkout, when a shopper selects **I am not sure** in the delivery date option, it creates a purchase requisition with a blanket order type, which results in the creation of a blanket purchase order.

Purchasing permissions define the list of users, groups, cost centers, or departments that are allowed to purchase against the blanket purchase order without requiring any approvals. As receipts and invoices are not applicable for blanket purchase orders, these related lists are not displayed on the purchase order form view.

For details on the various fields and related lists that are populated for a blanket purchase order, see [Purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/purchase-order.md).

## Standard purchases against a blanket purchase order

A standard purchase order release is created when the following conditions are satisfied:A standard purchase order release is created automatically, as part of the purchasing flow, when a user purchases a supplier product that is on a blanket purchase order and the following conditions are satisfied:

-   The blanket purchase order is in the **Ordered** or **Pending Revision** state, and the blanket purchase order line for the supplier product is active and is not in the **Pending Cancellation** state.
-   User who requested the purchase is defined under the associated purchasing permission of the blanket purchase order.

    The business owner who requested the original blanket purchase order can always release against the blanket purchase order even if they are not explicitly defined under the purchasing permission.

-   Creation date of the standard purchase line falls within the range of the blanket line’s start and end date.
-   The date of the purchase falls within the start and end date of the corresponding line on the blanket purchase order. For goods, the date of the purchase request is used. For services, the start and end date of the request are used.
-   Supplier product purchased is defined as a supplier product on the blanket purchase order.
-   Funds must be available on the blanket purchase order. The value of the **Released amount** field on the blanket purchase order must be less than the value in the **Total amount** field.

The standard purchase order release has a reference to the blanket purchase order and will be displayed under the Purchase Order Releases related list on the blanket purchase order.

On the blanket purchase order, the sum of the total amount of all released purchase orders is updated in the **Released amount** field of the Summary Details section.On the blanket purchase order, the **Released amount** field of the Summary Details section shows the total amount of the standard purchase order releases that reference the blanket purchase order, excluding handling fees and canceled lines. The value is recalculated when a purchase order line of a release reaches the **Ordered**, **Partially Delivered**, **Delivered**, or **Closed Canceled** state. When the value of the **Released amount** field matches with the value of the **Total amount** field, the status of the blanket purchase order changes to **Closed Released**.

**Note:** The **Released amount** field is updated only for standard purchase order releases that are created through the purchasing flow. If you add a release to the blanket purchase order manually, the **Released amount** field does not update.

Available funds are not a condition for creating a release. If a purchase order release amount results in the blanket purchase order amount being exceeded, an approval is triggered for the delta amount to the business owner of the applicable standard purchase order release.

For example, if a blanket purchase order exists with an associated purchasing agreement contract with validity from January 1, 2019 to December 31, 2019. The amount limit on the blanket purchase order is $1000, and the current released amount is $800. The next standard purchase order release against the blanket is for $500. So, an approval for the delta of $300 is required.

To check if a request should be considered as a release against an existing blanket purchase order:

-   For goods, check the creation date of the purchase request against the start and end date of the corresponding line on the blanket purchase order.
-   For services, check the start and end date of the request against the start and end date of the corresponding line on the blanket purchase order.

**Parent Topic:**[Sourcing and Purchasing Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/purchase-experience-workflow.md)


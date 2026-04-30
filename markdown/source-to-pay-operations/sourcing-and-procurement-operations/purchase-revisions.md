---
title: Purchase revisions
description: Revisions for the quantity of the product, budget, or delivery location can be made to orders placed from ShoppingHub.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase revisions

Revisions for the quantity of the product, budget, or delivery location can be made to orders placed from ShoppingHub.

The shopper can revise an order from ShoppingHub or the procurement specialist can submit revision from the Sourcing and Purchasing Automation module.

When a shopper updates the **Pricing** reference field on the purchase requisition line, a revision is triggered for both standard and blanket purchase requests.

-   For standard purchase requests, the quantity is left as-is. The total line amount is updated, which in turn updates the total amount of the purchase request and triggers reassessment of approvals, if applicable. Budget, even if populated, is not considered as a revision attribute.
-   For blanket purchase requests, the quantity is left as-is. The total line amount is updated, which in turn updates the total amount of the purchase request and triggers reassessment of approvals, if applicable. In this scenario, the revision line captures the change in the pricing reference as well as the budget.

When a purchase order is created, the pricing reference on the purchase requisition line cannot be revised.

## Revisions with no purchase order

If no purchase order is created, and state of the purchase requisition is not **Closed Rejected**, **Closed Complete**, or **Closed Canceled**, you can manually revise the purchase requisition. In this case, neither a revision request nor a new purchase requisition is created. You can view the updates in the Revision Lines related list of the purchase requisition line.

The addition of a new purchase requisition or purchase order line is restricted to the same supplier and business owner for a revision process.

## Purchase order revisions

-   Shopper-initiated purchase order revision:
    -   When the status of a purchase order is not **Closed Complete** or **Closed Canceled**, a shopper can revise the lines from ShoppingHub. A revision request is created and assigned to the procurement specialist, and the state is updated to **Closed Complete**. A procurement specialist does not have to confirm the revision request prior to creation of the revised purchase requisition.
    -   A new purchase requisition of type **Revision** is created and the revision request is attached to the revised purchase requisition.
-   Procurement specialist-initiated purchase order revision:
    -   To initiate a revision of the purchase order, select **Revise** in the Sourcing and Purchasing Automation module.
    -   On confirmation of the revision, a new purchase requisition of type **Revision** is created and the revision request is attached to the revised purchase requisition.
-   Shopper-initiated blanket purchase order revision:
    -   When the status of a blanket purchase order is not **Closed Released**, a shopper can initiate a revision from ShoppingHub. Only the quantity and budget can be revised on a blanket purchase order.
    -   When a budget revision is made, the quantity and total line amount of the corresponding blanket line is calculated to the nearest value using the negotiated unit cost of the supplier product. Revisions cannot be below the current released amount against the blanket purchase order. Revising either quantity or budget results in the other being back-calculated accordingly.
    -   On confirmation of the revision, a new purchase requisition of type **Revision** is created and the revision request is attached to the revised purchase requisition.

For both the shopper-initiated and procurement specialist-initiated purchase order and blanket purchase order revisions, the status of the purchase requisition is updated to **Pending Revision** and delegation of authority is reassessed.

The state of the purchase order and the purchase order lines that were revised are updated to **Pending Revision**. The state of the purchase order lines which are not revised does not change.

When the state of the purchase requisition is **Final Review** and the purchase requisition is of the type **Revision**, you can select **Update Purchase Order** to update the existing purchase order and purchase order lines with the revised information.

State of the purchase requisition is then updated to **Closed Complete**.

**Note:**

Revision requests must be in a closed state for a purchase order to be created. For more information on purchase orders, see [Purchase order](purchase-order.md).

Revisions are not allowed in ShoppingHub for lines that have been fully received. Revisions can only be triggered for an amount that exceeds the received amount.

## Impact of rejecting an increase in funds revision

If a purchase requisition or purchase order is revised, and the re-approval is rejected, the behavior is as follows:

-   If a purchase order doesn't exist, the purchase requisition is reverted to the pre-revision state and value, for both single and multiple lines.
-   If a purchase order exists, and the good or service has either been partially delivered or not delivered at all:
    -   For a single line, the original purchase order remains as-is. The purchase order reverts to its state prior to revision. The resulting purchase requisition of type Revision will be in the Closed Rejected state, with no option to update the purchase order.
    -   For multiple lines, if every line within the revision purchase requisition is rejected, the impact is the same as above.
    -   For multiple lines, if some of the lines within the revision purchase requisition are rejected, only those rejected lines revert to their state prior to revision, upon updating the purchase order.

## Purchase revision impact on cost allocations and milestones

-   **Cost allocation behavior**

    -   Cost allocations from the original purchase requisition are updated in the revised purchase requisition.
    -   If an increase or decrease in funds happens, a new cost allocation is created for the primary cost center \(cost center of the business owner on the purchase requisition\) on the revised purchase requisition.

        This amount reflects either as an increase \(positive amount\) or decrease \(negative amount\) in funds.

    -   Once the purchase order is updated, the revised purchase order contains separate entries for the primary cost center, that is, the one from the original purchase requisition and another as a result of the revision, along with any additional user-defined allocations from the original purchase requisition.
    -   Cost allocations cannot be updated after the creation of a purchase order.
    For more details on cost allocations, see [Cost allocations](cost-allocations.md).

-   **Milestone behavior**

    -   Milestone details are copied from the original purchase requisition to the revised purchase requisition.
    -   User can create any additional milestones, as needed, on completion of the revision.
    -   Once the purchase order is updated, the original milestone on the purchase order is updated to the **Closed Canceled** state, as a copy is already created during the revision process.
    For more details on milestones, see [Milestones](milestones.md).


**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

**Related topics**  


[Purchase revision flows](../concept/purchase-revision-flows.md)


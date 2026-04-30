---
title: Purchase requisition merging
description: Purchase requisitions can be merged if certain criteria are met. This avoids multiple purchase orders from being created unnecessarily and also helps enforce approval rule limits.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase requisition merging

Purchase requisitions can be merged if certain criteria are met. This avoids multiple purchase orders from being created unnecessarily and also helps enforce approval rule limits.

Consider these various scenarios for purchase requisition grouping.

## Scenarios for merging purchase requisitions

A procurement buyer can group new products by the same supplier into an existing requisition so that multiple orders are not sent to the supplier. Consider the following scenarios:

Scenario 1: A Purchase Requisition \(PR1\) for Supplier A exists, in state Pending Approval. Purchase Order \(PO\) has not been created.

-   Sourcing not required:

    If the shopper adds a supplier product from the same Supplier A in ShoppingHub, and it has the same submitted by, supplier, cost center, and business owner as PR1, then the lines are automatically grouped with PR1 with the state Pending Approval. PR1 remains in Pending Approval state. Approvals are re-assessed similar to revisions. If the line was created more than 24 hours after PR1, it is not grouped automatically and is created under a new purchase requisition.

-   Sourcing required:

    If the shopper adds a supplier product from the same Supplier A in ShoppingHub that does not have an active contractual price, a sourcing request is created. In the sourcing request, assuming that the line was awarded to the same Supplier A, and there is an existing purchase requisition with the same submitted by, supplier, cost center, and business owner, and the newly sourced line was created not more than 24 hours after PR1, the purchase line references PR1 when the supplier is awarded, and a purchase requisition is created. The line is added into PR1 with the state Pending Approval. PR1 remains in Pending Approval state. Approvals are re-assessed similar to revisions.


Scenario 2: PR1 for Supplier A exists, in state Awaiting Task Completion. PO does not exist yet.

-   A procurement specialist has to manually merge the purchase requisitions.
-   Sourcing not required:
    -   An annotation is displayed on the header of PR2 indicating that this purchase requisition can be merged with another existing requisition &lt;purchase requisition number&gt;, where &lt;purchase requisition number&gt; is a link to PR1 that has the same submitted by, supplier, cost center, and business owner as PR2. This annotation is cleared once an order is created against PR1.
    -   The user can select **Merge** on the PR2 header to move the lines from PR2 to PR1. If there are no other requisitions or sourcing requests belonging to the purchase request that PR2 belongs to, then the purchase request and PR2 are deleted. The merged lines are in the state Pending Approval, and the purchase requisition is also reverted to Pending Approval. However, the original lines remain in their original state. Approvals are re-assessed similar to revisions.
    -   If there were other requisitions or sourcing requests under purchase request 2, then the purchase request is not deleted. Only purchase requisition 2 is deleted.
    -   The **Merge** UI action is only available if PR2 and the corresponding lines were created not more than 24 hours after PR1.
-   Sourcing required: Upon awarding the sourcing request, a similar annotation is displayed on the header of the sourcing request indicating that this line can be merged with another existing requisition &lt;Purchase requisition number&gt;. The user can select **Merge with Existing Requisition** or **Create Requisition**. If merged, PR1's state reverts to Pending Approval.

Scenario 3: PR1 for Supplier A exists, in state Final Review. PO does not exist yet. Same as Scenario 2.

Scenario 4: PR1 in state Awaiting Task Completion, PR2 not merged with PR1 and in state Pending Approval. Another purchase is created. If the procurement specialist decides not to merge PR2 with PR1, and PR2’s state is still Pending Approval, then the new purchase lines automatically merge with PR2 according to the criteria in Scenario 1.

Scenario 5: Multiple PRs in state Awaiting Task Completion or Final Review. New PR created within 24 hours with the same requested by, supplier, cost center, and business owner.

-   When the user selects **Merge** on the new purchase requisition, display a list of all the purchase requisitions in the state Awaiting Task Completion or Final Review, and allow the user to select which one to merge with.
-   In this scenario, an annotation is displayed on the most recent purchase requisition indicating that this purchase requisition can be merged with several other requisitions.

Scenario 6: Revisions

-   Purchase requisitions of type Revision, created as a result of PO revision, are not eligible for merging.
-   Purchase requisition revisions, where no PO is created, can be considered for merging using similar criteria documented in the previous scenarios.

**Note:** For all merge scenarios, **Merge** is only displayed on the UI on the most recently created purchase requisition.

Scenario 7: PR1 for Supplier A exists, in state Closed Canceled, Closed Rejected, or Closed Complete. A line is not grouped into a PR that has the state Closed Canceled, Closed Rejected, or Closed Complete. Instead, a new PR is created.

Scenario 8: PO already created, and supplier product\(s\) from the same supplier is added. Create a new purchase request and purchase requisition \(PR2\).

## Purchase line merge

Purchase lines within a purchase requisition can also be merged under the following conditions:

-   If the supplier product, business owner, cost center, submitted by, delivery date or start date/end date, delivery location, payment method, and purchase reason are identical, except the quantity, the purchase lines can be grouped into a single line instead of separate lines.
-   If the delivery date, start date/end date, or delivery location is different, a new line must be created.
-   If only the payment method is different, the cost allocation entries should be updated accordingly, based on the combined ratio.
-   If only the purchase reason is different, append the purchasing reasons as follows:
    -   Purchasing reason 1 - qty 1 \(example: New hire orientation - qty 10\)
    -   Purchasing reason 2 - qty 2 \(example: IT hardware refresh - qty 2\)

**Note:** Purchase requisition merging and purchase line merging are not applicable for bundled products.

**Parent Topic:**[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)


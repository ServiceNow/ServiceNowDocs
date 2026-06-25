---
title: Editing purchase requisitions and orders with cost allocation adjustments
description: As a shopper, you can modify purchase requisitions \(PRs\) and purchase orders \(POs\) while maintaining cost allocation across multiple cost centers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/edit-purchase-cost-allocation.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Purchase revision flows, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Editing purchase requisitions and orders with cost allocation adjustments

As a shopper, you can modify purchase requisitions \(PRs\) and purchase orders \(POs\) while maintaining cost allocation across multiple cost centers.

## Example use case for editing a purchase with multiple cost centers

In this example, a shopper creates a PR with cost allocation distributed between two cost centers, Customer Success and Engineering. The costs are assigned based on predefined percentages.

Suppose 20% is allocated to Customer Success and 80% to Engineering.

\[Omitted image "cost-dist.png"\] Alt text: Cost allocation across multiple cost centers

If you purchase 6 quantities of the energy monitoring device priced at $230 each. The total cost amounts to $1380.

\[Omitted image "cost-purchase-qty.png"\] Alt text: Purchase products in Shopping Hub

The cost for this purchase is allocated as follows:

-   Customer Success Cost Center: $276 \(20% of $1380\)
-   Engineering Cost Center: $1104 \(80% of $1380\)

\[Omitted image "cost-initial-amt.png"\] Alt text: Initial amount with cost allocation adjustments

Now suppose you edit the PR or PO to increase the quantity from 6 to 10 pencils. The total cost amounts to $2300.

\[Omitted image "cost-qty-increase.png"\] Alt text: Increase purchase quantity by editing a purchase.

In this case, the total cost is proportionally distributed between both the cost centers based on the original allocation:

-   Customer Success Cost Center: $460 \(20% of $2300\)
-   Engineering Cost Center: $1840 \(80% of $2300\)

\[Omitted image "cost-final-amt.png"\] Alt text: Final amount with cost allocation adjustments

The cost allocation remains consistent when modifying purchase quantities in a PR or PO.

For more information, see [Cost allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/cost-allocations.md).

**Parent Topic:**[Purchase revision flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-revision-flows.md)

**Related topics**  


[Edit a purchase line from a purchase requisition or order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/edit-pur-req-line.md)

[Edit a purchase line from a purchase requisition or order from Employee Center \(EC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/edit-pur-req-emp-central.md)


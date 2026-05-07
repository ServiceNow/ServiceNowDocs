---
title: Order life cycle states
description: Learn about the order states from initial capture through enrichment, decomposition, fulfillment, and completion.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-09-09"
reading_time_minutes: 1
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Order life cycle states

Learn about the order states from initial capture through enrichment, decomposition, fulfillment, and completion.

1.  A new order gets created in the Draft state.
2.  After you review and submit the order, either of the two things happen:
    -   If post-capture order enrichment is configured, enrichment tasks are created, and the order state changes to Enrichment in progress.

        If you're blocked on order enrichment tasks, change the order state to Enrichment on hold. When you're unblocked, change the order state back to Enrichment in progress.

    -   If the details captured while creating the order are sufficient to process the order and no enrichment is required, then the order state changes to New.
3.  When the order is in the New state, you can either approve or reject the order. Accordingly, the state changes to either Acknowledged or Rejected.
4.  The order in the Acknowledged state then undergoes decomposition. Domain orders are created and fulfillment flows are triggered and the order state changes to In progress.
5.  If the order is successfully fulfilled, the order state changes to Completed. If there are issues during order processing, then the outcome depends on how the issue was handled. The scenarios and their outcomes are listed in the following table.

<table id="table_g3l_lbd_pgc"><thead><tr><th>

Scenario

</th><th>

State

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

More information needed to process the order

</td><td>

Awaiting information

</td><td>

-   If additional information is received, the order state changes to In progress.
-   Or else, the order state changes to Accessing cancellation.


</td></tr><tr><td>

Inflight order change

</td><td>

Revision in progress

</td><td>

-   If compensation plan is triggered, then the order state changes back to In progress.
-   Or else, the order state changes to Accessing cancellation.


</td></tr><tr><td>

Issues during order processing

</td><td>

On hold

</td><td>

-   If the issue blocking the order processing is resolved, then the order state changes back to In progress.
-   Or else, the order state changes to Accessing cancellation.


</td></tr></tbody>
</table>6.  After the cancellation request is reviewed and processed, orders in the Accessing cancellation state change to Canceled.


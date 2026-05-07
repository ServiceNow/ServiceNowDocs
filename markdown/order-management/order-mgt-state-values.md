---
title: Customer order states
description: Use the State fields on the customer order management forms to determine the current processing state for the customer order and to perform certain types of customer order actions, such as canceling a customer order.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-10-10"
reading_time_minutes: 11
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Customer order states

Use the State fields on the customer order management forms to determine the current processing state for the customer order and to perform certain types of customer order actions, such as canceling a customer order.

## Customer Order form states

Use the **State** field on the customer order form to determine the current processing state for the order, including all of its associated line items. You can also use it to perform certain types of order actions, such as canceling an order. To learn more, see [Managing post-fulfillment order changes](../concept/managing-orders.md).

<table id="table_xzp_3fn_v4b"><thead><tr><th>

Customer order state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Customer order that is still in the capture stage or the manual entry of the customer order is not complete. The data capture phase is when an agent is capturing an order or your instance is capturing the full customer order details from an API or through Service Bridge.

</td></tr><tr><td>

New

</td><td>

Customer order capture process is complete and the entire order is awaiting approval by the fulfillment manager. After the customer order data capture completes, it automatically moves to the New state.

</td></tr><tr><td>

Submitted

</td><td>

Customer order that the order agent has submitted.

</td></tr><tr><td>

Enrichment in progress

</td><td>

Customer order for which the order enrichment process is in progress.

</td></tr><tr><td>

Enrichment on hold

</td><td>

Customer order for which the order enrichment process in on hold.

</td></tr><tr><td>

Acknowledged

</td><td>

Customer order that the fulfillment manager approved for fulfillment processing.

</td></tr><tr><td>

Rejected

</td><td>

Customer order that the fulfillment manager rejected for fulfillment processing.

</td></tr><tr><td>

In progress

</td><td>

Customer order that has been approved and is being actively worked on.

</td></tr><tr><td>

Revision in progress

</td><td>

Customer order revision that is in process but has not been approved.As part of the Inflight Order Change functions, when you are currently in the process of updating the customer order, it moves to this state.

</td></tr><tr><td>

Awaiting information

</td><td>

Customer order that is in process but awaiting receipt of information from the customer before any further fulfillment processing takes place.

</td></tr><tr><td>

On hold

</td><td>

Customer order that is on hold. No further fulfillment processing can take place until the hold is removed.

</td></tr><tr><td>

Canceled

</td><td>

Customer order that the fulfillment manager canceled. No further fulfillment processing can take place.

</td></tr><tr><td>

Assessing cancellation

</td><td>

As part of the Inflight Order Change functions, when a cancellation request is submitted for the customer order, it moves to this state. A cancellation request has been submitted for the customer order.

</td></tr><tr><td>

Cancellation in progress

</td><td>

When the cancellation request is approved, the customer order moves to this state.

</td></tr><tr><td>

Canceled

</td><td>

Customer order that the fulfillment manager canceled. No further fulfillment processing can take place.

</td></tr><tr><td>

Completed

</td><td>

All associated customer order line items are complete.**Note:** After your agents complete all fulfillment tasks for the entire customer order, the following actions occur:

-   The **State** field for the customer order is automatically set to Completed.
-   The **State** field for each of the individual customer order line items is set to Completed.

</td></tr></tbody>
</table>**Note:** To learn more about Inflight Order Change functions and how they affect the Revision in Process, Assessing Cancellation, Cancellation in Progress, and Canceled customer order states, see the following:

-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)
-   [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#)

## Order line item form states

Use the **State** field on the order line item form to determine the current processing state for an individual customer order line item. You can also use it to perform certain types of customer order actions, such as canceling a line item.

<table id="table_dfq_zp4_v4b"><thead><tr><th>

Customer order line item state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Parent customer order that is still in the data capture stage or the manual entry of the customer order is not completed. The data capture phase is when an agent is creating and configuring order line items or your instance is capturing full customer order details from an API or through Service Exchange. In this case, Draft is a system-assigned state. This state is assigned by the system.

</td></tr><tr><td>

Submitted

</td><td>

Order line item of the customer order that the order agent has submitted.

</td></tr><tr><td>

Enrichment in progress

</td><td>

Order line item of the customer order for which the order enrichment process is in progress.

</td></tr><tr><td>

Enrichment on hold

</td><td>

Order line item of the customer order for which the order enrichment process in on hold.

</td></tr><tr><td>

New

</td><td>

Data capture process for the parent customer order that is complete and the customer order line item is awaiting fulfillment approval by the fulfillment manager. After the customer order capture is complete, it automatically moves to the New state. **Note:** When you manually enter a customer order and its order line items, you can assign a **Draft** or **New** state, based on your organization's published procedures.

</td></tr><tr><td>

Acknowledged

</td><td>

Customer order line item that the fulfillment manager approved for fulfillment processing.

</td></tr><tr><td>

Scheduled

</td><td>

Order line item that has successfully passed all validations and approvals and is queued for fulfillment. At this stage, orchestration workflows can begin, ensuring that resources are allocated and tasks are sequenced correctly before actual provisioning starts. This state acts as a control point to prevent premature execution and provides visibility that the item is ready for processing.

</td></tr><tr><td>

Rejected

</td><td>

Customer order line item that the fulfillment manager rejected for fulfillment processing. No further fulfillment processing can take place.

</td></tr><tr><td>

In progress

</td><td>

Customer order line item that is still in process but not ready for fulfillment approval.

</td></tr><tr><td>

Revision in progress

</td><td>

Customer order line item revision that is in process but has not been approved. To learn more, see the following:-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)
-   [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#)

</td></tr><tr><td>

Awaiting information

</td><td>

Customer order line item that is in process but awaiting receipt of information from the customer before any further fulfillment processing takes place.

</td></tr><tr><td>

On hold

</td><td>

Customer order line item that is on hold. No further fulfillment processing can take place until the hold is removed.

</td></tr><tr><td>

Assessing cancellation

</td><td>

As part of the Inflight Order Change functions, when a cancellation request is submitted for the customer order line item, it moves to this state. To learn more, see the following:-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)
-   [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#)

</td></tr><tr><td>

Cancellation in progress

</td><td>

When the cancellation request is approved, the customer order line item moves to this state. To learn more, see the following:-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)
-   [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#)

</td></tr><tr><td>

Canceled

</td><td>

Customer order line item that the fulfillment manager canceled. No further fulfillment processing can take place.

</td></tr><tr><td>

Completed

</td><td>

Customer order line item and all associated domain orders and order tasks that are complete.**Note:** After your agents complete all fulfillment tasks for the entire customer order, the following actions occur:

-   The **State** field for the customer order is automatically set to Completed.
-   The **State** field for each of the individual customer order line items is set to Completed.

</td></tr></tbody>
</table>**Note:** To learn more about Inflight Order Change functions and how they affect the Revision in Process, Assessing Cancellation, Cancellation in Progress, and Canceled customer order line item states, see the following:

-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)
-   [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#)

## Product Order, Service Order, and Resource Order form states

Use the **State** fields on the Product Order, Service Order, and Resource Order forms to determine the current processing state for a product order, service order, or resource order.

<table id="table_kps_2v4_v4b"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

New or waiting-to-start tasks that are assigned to the product, service, or resource order.

</td></tr><tr><td>

Qualified

</td><td>

All required prerequisite tasks that are complete. Processing for the product, service, resource order, or its associated tasks can start.

</td></tr><tr><td>

In progress

</td><td>

Product, service, or resource order processing that is still in progress.

</td></tr><tr><td>

On hold

</td><td>

Product, service, or resource order processing is on hold due to issues or inadequate information required for processing the order.

</td></tr><tr><td>

Scheduled

</td><td>

Product, service, or resource order that has successfully passed all validations and is queued for fulfillment

</td></tr><tr><td>

Closed complete

</td><td>

Product, service, or resource order processing that is completed.**Note:** after your agents complete all fulfillment tasks for the product, service, or resource order, the state is automatically set to Closed Complete.

</td></tr><tr><td>

Canceled

</td><td>

Product, service, or resource order processing that was canceled.

</td></tr><tr><td>

Cancellation in progress

</td><td>

Product, service, or resource order that is in the process of being cancelled.

</td></tr></tbody>
</table>## Order Task form states

Use the **State** field on the Order Task form to determine the processing state for an order task. To learn more, see [Review and close fulfillment tasks](../task/order-mgt-customer-order-tasks.md).

<table id="table_c4f_154_v4b"><thead><tr><th>

Order task state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open

</td><td>

Processing for the order task that is open and no processing is currently taking place.

</td></tr><tr><td>

In progress

</td><td>

Processing for the order task that is still in progress or in fulfillment.

</td></tr><tr><td>

On hold

</td><td>

Order task that is on hold. No further fulfillment processing can take place until the hold is removed. If you created a fallout record for it, the state of the order task changes to On Hold until the person or group that is assigned to the fallout record resolves the issue.

</td></tr><tr><td>

Scheduled

</td><td>

 

</td></tr><tr><td>

Awaiting information

</td><td>

Order task that is in process but awaiting receipt of required information before any further processing takes place.

</td></tr><tr><td>

Resolved

</td><td>

An order task that was previously on hold due to an issue, which has now been resolved.

</td></tr><tr><td>

Closed Complete

</td><td>

Processing for the order task that is complete. It is a system-assigned state.**Note:** After your agents complete all fulfillment tasks for the order task, the state is automatically set to Closed complete.

</td></tr><tr><td>

Canceled

</td><td>

Processing for the order task that was canceled.

</td></tr><tr><td>

Draft

</td><td>

Order task that is still in the capture stage or the manual entry of the order task is not complete.

</td></tr></tbody>
</table>**Parent Topic:**[Order Management reference](order-mgt-reference.md)


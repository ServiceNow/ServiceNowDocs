---
title: Service order states
description: Use the State fields on the Order Management forms to determine the current processing state for the service order and to perform certain types of order actions, such as canceling an external service order.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Service order states

Use the State fields on the Order Management forms to determine the current processing state for the service order and to perform certain types of order actions, such as canceling an external service order.

The following flowchart illustrates how customer and service order state processing works.

![Infographic showing the customer order and service order processing workflow. For the text description, refer to the Service Order form states section.](../image/add-order-states.svg "Customer and service order state processing")

## Service Order form states

Use the **State** field on the Service Order form to determine the current processing state for the service order, including all of its associated line items. You can also use it to perform certain types of order actions, such as canceling a service order.

<table id="table_xzp_3fn_v4b"><thead><tr><th>

Service order state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Service order that is still in the capture stage or the manual entry of the service order is not complete. The data capture phase is when your instance is capturing full service order details from the TMF641. **Note:** The Service Order Open API is a ServiceNow implementation of the TMForum TMF641 Service Ordering Open API specification. To learn more, see Service Order Open API.

 In this case, Draft is a system-assigned state.

 **Note:** The Draft state also applies to domain orders that are created by the decomposition process. These orders are awaiting additional information or for their turn in the initiate order fulfillment process.

</td></tr><tr><td>

New

</td><td>

Service order capture process that is complete and the entire order is awaiting approval by the service order manager. After the service order data capture completes, it automatically moves to the New state.

</td></tr><tr><td>

Submitted

</td><td>

Service order that the order agent has submitted.

</td></tr><tr><td>

Enrichment in progress

</td><td>

Service order for which the order enrichment process is in progress.

</td></tr><tr><td>

Enrichment on hold

</td><td>

Service order for which the order enrichment process in on hold.

</td></tr><tr><td>

Acknowledged

</td><td>

Service order that the service order manager approved for fulfillment processing.

</td></tr><tr><td>

Rejected

</td><td>

Service order that the service order manager rejected for fulfillment processing.

</td></tr><tr><td>

In progress

</td><td>

Service order that has been approved and is being actively worked on. To learn more, see [Review and close fulfillment tasks](../task/order-mgt-customer-order-tasks.md).

</td></tr><tr><td>

Revision in progress

</td><td>

As part of the Inflight Order Change functions, when you are currently in the process of updating the service order, it moves to this state.

</td></tr><tr><td>

Awaiting information

</td><td>

Service order that is in process but awaiting receipt of information from the customer before any further fulfillment processing takes place.

</td></tr><tr><td>

On hold

</td><td>

Service order that is on hold. No further fulfillment processing can take place until the removal of the hold.

</td></tr><tr><td>

Assessing cancellation

</td><td>

Cancellation request that has been submitted for the service order. As part of the Inflight Order Change functions, when a cancellation request is submitted for the service order, it moves to this state.

</td></tr><tr><td>

Cancellation in progress

</td><td>

When the cancellation request is approved, the service order moves to this state.

</td></tr><tr><td>

Canceled

</td><td>

Service order that the service order manager canceled. No further fulfillment processing can take place.

</td></tr><tr><td>

Completed

</td><td>

All associated service order line items are complete. **Note:** After your agents complete all fulfillment tasks for the entire captured service order, the following actions occur:

-   The **State** field for the captured service order is automatically set to Completed.
-   The **State** field for each of the individual captured service order line items is set to Completed.

</td></tr></tbody>
</table>**Note:** To learn more about Inflight Order Change functions and how they affect the Revision in Process, Assessing Cancellation, Cancellation in Progress, and Canceled service order states, see

-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)
-   [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#)

## Order Line Item form states

Use the **State** field on the Order Line Item form to determine the current processing state for an individual service order line item. You can also use it to perform certain types of order actions, such as canceling a line item.

<table id="table_dfq_zp4_v4b"><thead><tr><th>

Service order line item state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Parent service order that is still in the data capture stage or the manual entry of the order is not complete. The data capture phase is when your instance is capturing full service order details from the TMF641.

 In this case, Draft is a system-assigned state.

</td></tr><tr><td>

Submitted

</td><td>

Order line item of the service order that the order agent has submitted.

</td></tr><tr><td>

Enrichment in progress

</td><td>

Order line item of the service order for which the order enrichment process is in progress.

</td></tr><tr><td>

Enrichment on hold

</td><td>

Order line item of the service order for which the order enrichment process in on hold.

</td></tr><tr><td>

New

</td><td>

Data capture process for the parent service order that is complete, and the service order line item is awaiting fulfillment approval by the service order manager. After the service order capture is complete, it automatically moves to the **New** state. **Note:** When you manually enter a service order and its order line items, you can assign a Draft or New state, based on your organization's published procedures.

</td></tr><tr><td>

Acknowledged

</td><td>

Service order line item that the service order manager approved for fulfillment processing.

</td></tr><tr><td>

Scheduled

</td><td>

Order line item that has successfully passed all validations and approvals and is queued for fulfillment. At this stage, orchestration workflows can begin, ensuring that resources are allocated and tasks are sequenced correctly before actual provisioning starts. This state acts as a control point to prevent premature execution and provides visibility that the item is ready for processing.

</td></tr><tr><td>

Rejected

</td><td>

Service order line item that the service order manager rejected for fulfillment processing. No further fulfillment processing can take place.

</td></tr><tr><td>

In progress

</td><td>

Service order line item that is still in process but not ready for fulfillment approval.

</td></tr><tr><td>

Revision in progress

</td><td>

Service order line item revision that is in process but has not been approved. As part of the Inflight Order Change functions, when you are currently in the process of updating the parent service order or this service order line item, it moves to this state.

</td></tr><tr><td>

Awaiting information

</td><td>

Service order line item that is in process but awaiting receipt of information from the customer before any further fulfillment processing takes place.

</td></tr><tr><td>

On hold

</td><td>

Service order line item that is on hold. No further fulfillment processing can take place until the hold is removed.

</td></tr><tr><td>

Assessing cancellation

</td><td>

Cancellation request that has been submitted for the service order line item. As part of the Inflight Order Change functions, when a cancellation request is submitted for the service order line item, it moves to this state.

</td></tr><tr><td>

Cancellation in progress

</td><td>

When the cancellation request is approved, the service order line item moves to this state.

</td></tr><tr><td>

Canceled

</td><td>

Service order line item that the service order manager canceled. No further fulfillment processing can take place.

</td></tr><tr><td>

Completed

</td><td>

Service order line item and all associated and external service order tasks that are complete. It is a system-assigned state.**Note:** After your agents complete all fulfillment tasks for the entire product, service, or resource order, the state is automatically set to Closed Complete.

</td></tr></tbody>
</table>**Note:** To learn more about Inflight Order Change functions and how they affect the Revision in Process, Assessing Cancellation, Cancellation in Progress, and Canceled service order line item states, see

-   [Managing inflight order changes and cancellation requests](../concept/inflight-order-change-mgt-overview.md)
-   [Key inflight order change and cancellation request fields](../concept/key-inflight-order-change-cancellation-request-fields.md#)

## Order task form states

Use the **State** field on the Order Task form to determine the processing state for an order task.

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


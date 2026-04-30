---
title: Order Tasks form
description: The Order Task form enables you to review and update the fulfillment tasks that are associated with the selected order.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-10-28"
reading_time_minutes: 2
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Order Tasks form

The Order Task form enables you to review and update the fulfillment tasks that are associated with the selected order.

<table id="id_l13_l5n_pqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-assigned ID for the task, starting with a prefix of TASK.

</td></tr><tr><td>

Account

</td><td>

Name of the customer account.

</td></tr><tr><td>

Primary contact

</td><td>

Primary contact for the customer account.

</td></tr><tr><td>

Order line item

</td><td>

Order line item associated with the order task.

</td></tr><tr><td>

Parent

</td><td>

Parent product, service, or resource order associated with the order task.

</td></tr><tr><td>

Short Description

</td><td>

Short description of the order task.

</td></tr><tr><td>

State

</td><td>

Current state for the order task. To view a listing of selections, select the down arrow ![](../image/field-selection-list.png) icon:

-   **Open**

Processing for the order task is open, and no processing is taking place.

-   **In Progress**

Processing for the order task is still in progress, or in fulfillment.

-   **On hold**

Order tasks that are on hold due to issues or errors.

-   **Scheduled**

Order task scheduled for processing.

-   **Awaiting information**

Order task that is stalled due to the lack of information.

-   **Resolved**

Issues blocking the processing of stalled order tasks have been resolved.

-   **Closed Complete**

Processing for the order task is complete. It is a system-assigned state.

**Note:** After your agents complete all fulfillment tasks for the order task, the state is automatically set to **Closed Complete**.

-   **Canceled**

Processing for the order task was canceled.

-   **Draft**

Order task that is still being created by the system or manually.


</td></tr><tr><td>

Priority

</td><td>

The priority of the order task. Options include:-   None
-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

</td></tr><tr><td>

Assignment group

</td><td>

The group of agents to which you want to assign the order task.

</td></tr><tr><td>

Assigned to

</td><td>

Name of the agent who should be assigned to the order task.

</td></tr><tr><td>

Short description

</td><td>

Optional description for the order task.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Free-form work order text that your customers can view.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Free-form private work note text for the product order. This work note text is for internal purposes only, and the customer can't see it. Enter the work note text, and then select **Post Work notes**.

</td></tr><tr><td>

Activity

</td><td>

Activity stream section for viewing all processing activities that have taken place for the selected order task. It includes a message that indicates that the order has been approved for processing and fulfillment.To expand, collapse, or filter by activity stream: -   Select the activity stream filter icon ![](../image/activity-stream-filter.png) to filter by post types, field changes, or flagged items.
-   Select the search icon ![](../image/field-search.png) to search the required information in the activity stream.
-   Select the sort descending icon ![](../../../reuse/icons/product-icons/sort-descending-outline-24.svg) to sort the activity from oldest to newest or select the sort ascending icon ![](../../../reuse/icons/product-icons/sort-ascending-fill-24.svg) for the opposite action.

</td></tr><tr><td>

Attachments

</td><td>

File attachments for the order task. Select **Select file** to add the file as an attachment.

</td></tr></tbody>
</table>**Parent Topic:**[Order Management reference](order-mgt-reference.md)


---
title: Manage Order Line Milestones
description: View order line milestones on order line items and mark milestones as reached when fulfillment events occur. Reach milestones automatically via fulfillment flows or manually through the UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/Manage-order-line-milestones.html
release: australia
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 2
keywords: [milestone, order fulfillment, user task, mark as reached]
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Manage Order Line Milestones

View order line milestones on order line items and mark milestones as reached when fulfillment events occur. Reach milestones automatically via fulfillment flows or manually through the UI.

## Before you begin

Your admin must have enabled order line milestones and configured the Milestone Flow Policy decision table. Milestones are created automatically when orders are submitted.

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

Order line milestones appear on order line items as soon as the order is submitted. You can view them, track their status, and manually mark them as reached when the business events they represent are complete.

## Procedure

1.  Open an order line item to view its milestones.

    In **Workspace**, navigate to a customer order and open an order line item.

    Click the **Order Line Milestones** tab or scroll to the **Order Line Milestones** related list.

2.  Review milestone details.

    The **Order Line Milestones** list displays:

    -   **Milestone** — The name of the milestone \(for example, "Managed Connectivity Services Supreme Bundle"\).
    -   **Status** — Either **Open** \(waiting to be reached\) or **Reached** \(completed\).
    -   **Sequence** — The order in which milestones are typically reached.
    -   **Milestone reached date** — The date and time the milestone transitioned to **Reached** status \(empty if still open\).
3.  Mark a milestone as reached \(manual\).

    Click on the milestone record to open it.

    In the form, locate the **Mark as Reached** button \(displayed when the milestone status is **Open**\).

    Click the button. The system updates:

    -   **Status** changes to **Reached**.
    -   **Milestone reached date** is populated with the current date and time.
    The milestone record updates immediately, and you're returned to the form.

4.  View milestone history in the related list.

    Return to the **Order Line Milestones** related list on the order line item. Reached milestones now show **Reached** status and display the date reached.

    This gives you a quick view of fulfillment progress for the order line.


## Result

The milestone is marked as reached. Your fulfillment flows may automatically respond—closing orders, updating tasks, sending notifications, or triggering compensation calculations—depending on how your admin configured the flows.

## Example: Marking a milestone as reached

You receive an order line for a Managed Connectivity Services bundle. When the order is submitted, an order line milestone is created with the name "Managed Connectivity Services Supreme Bundle" and status **Open**.

As fulfillment progresses, the SIM card is added to the package and the service is activated. At that point, you open the milestone record and click **Mark as Reached**. The status changes to **Reached** and the reached date is set to today's date.

The fulfillment flow detects this change and automatically closes the domain order and updates customer records.

## What to do next

Milestones can be marked as reached automatically if your admin configured fulfillment flows with the **Set Order Line Milestone to Reached** action. When business conditions are met \(for example, when a domain order closes\), the milestone updates without manual intervention.


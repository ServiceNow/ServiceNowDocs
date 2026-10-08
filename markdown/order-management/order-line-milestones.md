---
title: Order line milestones
description: Order line milestones mark key steps in fulfillment. Tie milestones to events like task completion, characteristic updates, or domain order closure to track progress and trigger downstream actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/order-line-milestones.html
release: australia
topic_type: concept
last_updated: "2026-09-17"
reading_time_minutes: 2
keywords: [milestone, order fulfillment, tracking]
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Order line milestones

Order line milestones mark key steps in fulfillment. Tie milestones to events like task completion, characteristic updates, or domain order closure to track progress and trigger downstream actions.

## Order line milestone levels

Order line milestones are checkpoints in the fulfillment lifecycle. They represent meaningful completion events—a step reached, a condition met, or a state achieved. Each milestone tracks when specific work gets done for an order line item.

Milestones live at two levels:

-   Milestone — admin-defined templates created at configuration time. These define what completion looks like for your business.
-   Order Line Milestone — runtime instances created automatically when orders are submitted. Each order line gets its own set of order line milestone records, tied to the milestone definitions you created.

## Milestone benefits

Milestones let you:

-   Track fulfillment progress at a glance—see which orders have reached which checkpoints.
-   Trigger automatic actions—set a milestone as reached, and let your fulfillment flows respond \(close domain orders, update tasks, notify contacts\).
-   Build visibility into service delivery timelines—connect milestones to specific service events customers care about, such as service activation, billing cycle milestones, or support escalation triggers.
-   Support compensation planning—use milestone dates to calculate incentives or SLA credits.

## Milestone states and dates

Every order line milestone has a status and \(optionally\) a reached date:

-   **Open** — Created when the order is submitted. The milestone is waiting to be completed.
-   **Reached** — Set when the business event happens \(manually via UI action, or automatically via a fulfillment flow\). The **Milestone reached date** field is populated with the date and time the milestone transitioned to reached.

## Milestone fulfillment workflow

Here's the typical flow:

1.  admin creates Milestone records—e.g., "SIM card added," "Domain order closed," "Service level activated."
2.  admin configures the **Milestone Flow Policy** decision table to map products, specifications, and actions to specific milestones.
3.  Customer submits an order with a product that triggers the **Create Order Line Milestones** business rule.
4.  For each order line, the decision table evaluates conditions and determines which milestone applies. An order line milestone record is created with status **Open**.
5.  During fulfillment, when the business event occurs \(characteristic updated, domain order closed, etc.\), a fulfillment flow or admin user marks the milestone as **Reached**.
6.  Downstream flows can then trigger on milestone completion—close orders, send notifications, update compensation records.

## Milestone examples

-   **SIM card added** — Mark as reached when the SIM card is physically added to the package.
-   **Domain order closed** — Mark as reached when the domain order transitions to a completed state.
-   **Service activated** — Mark as reached when the service is live for the customer.
-   **Characteristic updated** — Mark as reached when a required characteristic field is populated or modified.
-   **Task completed** — Mark as reached when fulfillment tasks linked to the order are closed.

## Key concepts

-   **Milestone**

    A configuration-time record that defines what business event you want to track. Reusable across multiple orders and created by admins.

-   **Order Line Milestone**

    A runtime instance created when an order is submitted. Tied to a specific order line and a specific milestone definition. Tracks the status \(open or reached\) and the date reached.

-   **Milestone Flow Policy**

    The decision table that maps order line details \(product, specification, action\) to milestone definitions. Admins customize this table to define milestone allocation for their business.

-   **Create Order Line Milestones**

    The business rule that runs when a customer order is submitted. It iterates through order lines and creates order line milestone records based on the Milestone Flow Policy decision table.



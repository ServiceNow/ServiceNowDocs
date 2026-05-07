---
title: Approving or rejecting orders
description: Fulfillment managers bridge the gap between order intake and execution by reviewing the order information and deciding whether an order is ready to proceed or requires further review.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Approving or rejecting orders

Fulfillment managers bridge the gap between order intake and execution by reviewing the order information and deciding whether an order is ready to proceed or requires further review.

## Approval workflow

To begin the approval process, start by reviewing the order and its line items thoroughly. Verify that all required fields such as order number, customer account details, contact information, pricing, critical dates, and product or service specifications are complete and accurate. The order must be in a New state to be eligible for approval.

As part of this review, the system validates key order details such as contract dates to ensure the order meets approval criteria before it can proceed.

Next, validate the order against your organization’s approval criteria. The approval criteria could include checks such as:

-   Accuracy of order details
-   Completeness of required fields
-   Compliance with business rules such as discount thresholds, contractual terms, or inventory availability
-   Validity of associated agreements or entitlements

Throughout the process, maintain clear documentation and communication. If any issues arise, coordinate with relevant teams to resolve them before approval, promoting a smooth transition from order intake to fulfillment, and minimizing delays or fallout.

You can make corrections or updates to order characteristics before approval. Once the order passes all checks, proceed to approve it. This action updates the order status to In progress, which triggers the fulfillment workflows such as decomposition into domain orders, tasks, assignment to teams, and scheduling. The system logs the approval action and updates revision fields to reflect the change.

## Rejection workflow

Begin by carefully reviewing the order details against your organization's rejection criteria checklist. The following is a list of common rejection triggers:

-   Missing or incorrect data
-   Policy violations such as unauthorized discounts or invalid entitlements
-   Inventory constraints
-   Fraud or risk flags

Once a rejection decision is made, update the order status to Rejected in the system. This action automatically halts any associated fulfillment workflows, stopping the order from being processed further. It’s important to document the reason for rejection clearly using work notes so that the requester or relevant teams understand what must be corrected.

## Reevaluating rejected orders

A rejected order can be corrected and resubmitted for reevaluation by the order agent. If all issues are resolved and the order meets approval criteria, you can approve the order. Approving a rejected order updates the status back to In progress, enabling fulfillment to resume.


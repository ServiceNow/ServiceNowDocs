---
title: Return Merchandise Authorization case end-to-end workflow
description: The Return Merchandise Authorization \(RMA\) end-to-end process is structured into a four-stage playbook that provides structured guidance and oversight throughout each phase. The RMA case workflow initiates when a customer logs an issue for their products.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Return Merchandise Authorization, Order operations, Explore, Sales Customer Relationship Management]
---

# Return Merchandise Authorization case end-to-end workflow

The Return Merchandise Authorization \(RMA\) end-to-end process is structured into a four-stage playbook that provides structured guidance and oversight throughout each phase. The RMA case workflow initiates when a customer logs an issue for their products.

The following are the different phase involved in RMA case end-to-end workflow.

## Initiate case

-   Agent action: Navigate to the RMA Case list and select **New** to open the RMA Case form.
-   System action:
    -   The playbook record generator renders the RMA Case form.
    -   And once the RMA Case form is rendered, Agent fills the customer details and **Request Source** fields, and select **Save**.
    -   The system creates the RMA Case in the Draft State.
-   Agent action: Add defective install base items as RMA Case Lines.
-   System action: Create RMA Case Lines for each selected item.
-   Agent action: Update each line with request reason code and customer-expected resolution, then submit.

## Review case

Agent action:

-   Assign the case to an agent, moving it to Work In Progress \(WIP\).
-   Perform warranty and entitlement checks for each case line.
-   Update proposed resolution sales return cases.

## Resolve case

Agent action:

-   Create tasks for support teams if needed.
-   Place case lines in the Awaiting Info state if more information is required.
-   Communicate with the customer as needed.
-   Update resolution codes and state for all case lines once resolved.

## Close case

Agent action:

-   Put the RMA case in Resolved state and formally close the case after all lines are resolved.
-   Send a final communication to the customer confirming the closure.

**Related topics**  


[Return Merchandise Authorization case user journey](rma-case-user-journey.md)


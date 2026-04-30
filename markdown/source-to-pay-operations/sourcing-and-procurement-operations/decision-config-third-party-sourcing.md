---
title: Decision configuration for third-party sourcing
description: The Sourcing Event Generation Rule decision table in Sourcing and Procurement Operations helps the sourcing managers and procurement teams to configure the business criteria on demand, which provides them with flexibility to decide on the types of requests that should be integrated with a third-party sourcing solution.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sourcing and Procurement Operations integration with third-party sourcing solutions, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Decision configuration for third-party sourcing

The Sourcing Event Generation Rule decision table in Sourcing and Procurement Operations helps the sourcing managers and procurement teams to configure the business criteria on demand, which provides them with flexibility to decide on the types of requests that should be integrated with a third-party sourcing solution.

If no decisions are configured, then sourcing requests aren’t sent to any external applications.

When a shopper requests pricing for an item that must be sourced in ShoppingHub, the following decision inputs are automatically evaluated in ServiceNow:

-   Sourcing request
-   Purchase line

To configure a decision:

1.  Navigate to **Sourcing and Purchasing Automation** &gt; **Administration** &gt; **Decision Tables**.
2.  Select the Sourcing Event Generation Rule decision table.
3.  On the Decisions related list, select **New**.
4.  In the **Label** field, enter a name for the label.
5.  In the **Answer** field, select an answer record for the given external application from the Third-Party Sourcing Registration table.

    **Note:** If there are no existing external application records in the Third-Party Sourcing Registration table, create one with the following:

    -   Third-Party Sourcing Registration Code: User-defined code to be associated with the third-party sourcing registration.
    -   Third-Party Sourcing Registration Name: Name of the third-party sourcing registration to be integrated with ServiceNow.
6.  In the **Condition** field, configure the conditions using the sourcing request and purchase line decision inputs.

    **Note:** To send sourcing requests successfully to the applicable external third-party application, these conditions must be evaluated to be true.


**Parent Topic:**[Sourcing and Procurement Operations integration with third-party sourcing solutions](psm-integration-third-party-sourcing.md)


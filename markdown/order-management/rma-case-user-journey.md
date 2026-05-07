---
title: Return Merchandise Authorization case user journey
description: The Return Merchandise Authorization \(RMA\) user journey describes the steps a customer and support agent take when handling a sales return cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Return Merchandise Authorization, Order operations, Explore, Sales Customer Relationship Management]
---

# Return Merchandise Authorization case user journey

The Return Merchandise Authorization \(RMA\) user journey describes the steps a customer and support agent take when handling a sales return cases.

The RMA user journey starts when a customer reports an issue. The agent then manages the request through a clear four-stage process:

1.  Initiate the case
2.  Review the details and entitlements
3.  Resolve the issue
4.  Close the case

This approach confirms that every request is handled smoothly, with clear communication and a focus on effective resolution.

|Steps|User|Action|System response|
|-----|----|------|---------------|
|1|Customer|Identifies product issue and contacts customer support.|Support request is logged. Customer is guided to provide product and issue details.|
|2|Agent|Receives request and navigates to the RMA Case list.|Agent selects New to initiate RMA Case creation.|
|3|Agent|Fills in customer or account details and request source in the RMA Case form.|System renders the form and creates the RMA Case in Draft state.|
|4|Agent|Adds defective products as RMA Case Lines by selecting from customer’s install base items.|System creates RMA Case Lines for each selected item.|
|5|Agent|Updates each case line with request reason code \(such as defective, damaged\) and customer expected resolution.|System saves details. Agent submits the case for processing.|
|6|Agent|Assigns the case to self \(or another agent\) to begin processing.|RMA Case and lines move to Work In Progress state.|
|7|Agent|Reviews warranty and entitlements for each case line.|System displays entitlement status and enables agent to add entitlements as needed.|
|8|Agent|Decision: Accept or Reject RMA Case?|If accepted, proceed to next step. If rejected, agent notifies customer and closes the case.|
|9|Agent|\(If accepted\) Proposed solution and updates repair type.|System records proposed resolution.|
|10|Customer|Reviews proposed solution and provided feedback \(accepts or requests clarification\).|System logs customer response.|
|11|Agent|If additional work is required, create task for specialist.|System assigns task and tracks progress for each case line.|
|12|Agent|Updates case line and overall case status as tasks are completed and customer feedback is received.|System transitions case through Resolved and Closed states as appropriate.|
|13|Agent|Communicates final resolution to customer and formally closes the case.|System archives the case and all related records.|

![This infographic displays the RMA case user journey for reporting a product issue.](../image/RMA-user-journey.png "RMA case user journey")

## Related links

-   [Activate the Return Merchandise Authorization plugin](activate-return-merchandise-authorization-plugin.md)
-   [Return Merchandise Authorization Case Management](../reference/return-merchandise-authorization-case-management-reference.md)

**Related topics**  


[Return Merchandise Authorization case end-to-end workflow](rma-case-end-to-end-flow.md)


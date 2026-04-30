---
title: External routing overview
description: External Routing involves routing to external queue based on the service channel and queue conditions, and then the assignment is completed by the third-party system.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# External routing overview

External Routing involves routing to external queue based on the service channel and queue conditions, and then the assignment is completed by the third-party system.

## Process flow

This is how the work items are processed when using external routing:

1.  Work items are routed to the queue in a queued state but are unassigned. Work items expire if the Max timeout is set.
2.  External solution looks for work items in queued state by the Work Item Table API.
3.  External solution looks for agent availability vi the AWA Agent API before assigning to agent.
4.  The external solution uses the AWA Assignment API to assign the work items to the agent.
5.  The agent sees an inbox card.

When Advanced Work Assignment is configured to use external routing:

-   Queues do not allow to have Assignment Eligibility Groups defined.
-   Work items remain in the queue with a "queued" status until the external system assigns the work item or the queue maximum wait time elapses.
-   Related lists do not display at the bottom of the Queues screen.

These APIs are required for external routing:

-   AWA Assignment API to support the external routing system to assign work items. For information on AWA Assignment API, see [AWA Assignment API](https://www.servicenow.com/docs/access?context=awa_manual_assign-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) .
-   Work item table API \(awa\_work\_item\) to look up the queued work items waiting for assignment. For information on table API, see [Table API](https://www.servicenow.com/docs/access?context=c_TableAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   AWA Agent API if the external solution requires validation of agent availability within Workspace before assignment. For more information on the AWA Agent API, see [AWA Agent API](https://www.servicenow.com/docs/access?context=agent-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Functionality of AWA components

When external routing is enabled, the AWA components provide these capabilities:

Agent

-   Components utilized
    -   Agent availability
    -   Accept button
    -   Agent capacity in use \(Service channel capacity\) increases but is not utilized against the max capacity of service channel
    -   Agent universal capacity in use increases but is not utilized against the max universal capacity
-   Components not utilized
    -   Reject button with rejection reasons: The Reject button is used when configured in the manual assignment API. If the reject button is enabled \(allowed\_to\_decline=**true** parameter in assignment API request\), then the rejection reasons are supported.
    -   Max agent capacity
    -   Max universal capacity

Service channel

-   Components utilized
    -   Channel advanced condition
    -   Inbox layouts
    -   Queue order
-   Components not utilized
    -   Assign to and assignment group fields

        These fields are used to:

        -   Determine if a document should qualify for routing.
        -   Determine which field to update once the work item is successfully assigned to an agent.
    -   Capacity and utilization features
    -   Agent capacity overrides
    -   Work item override

Queue

-   Components utilized
    -   Max wait time will expire work items if set on queue
    -   Work item routing conditions
    -   Queue order
-   Components not utilized
    -   Queue agents' presence checks: Agent's presence is checked during the assignment API request processing.
    -   Work items remain in the queue with a status of "queued" until the external system routes the work item
    -   Queue schedules
    -   The following related lists are hidden on the queue since they are not utilized:
        -   Assignment eligibility and rules
        -   Work item sort order
        -   Agent Affinity
        -   Agent assignments
        -   Group queue priorities
        -   Work items

## Functionality of External routing in AWA

External routing enables AWA to integrate with third-party contact-center-as-a-service \(CCaaS\) providers. When the external provider has made an assignment decision, the work item gets assigned utilizing the existing AWA Assignment API.

External Routing can

-   Send events to keep providers informed about the work item and agent status.
-   Enhance the assignment API to handle provider-initiated work items.
-   Track and offer contact center work items, while outsourcing agent selection to the contact center.

When Advanced Work Assignment is configured for external routing:

-   AWA provides additional parameters for an Inbox experience.
-   AWA provides additional logging and performance improvements.
-   The Inbox card is presented to the Agent with both the Reject and Accept buttons when Auto-accept is false.
-   The Inbox card shows the Time-out value to Agent. If auto-assign is true, this field is ignored, when the Time-out value of the Work Item is greater than 0.
-   The presence state of the agent switches to the specified presence state. If auto-assign is true OR no timeout is passed in, this field is ignored.
-   The work item is immediately assigned to Accept, when the Auto-assign value is true.
-   The auto-assigned work item is either displayed as an Inbox card, or both Inbox card and workspace tab. If the auto-assign value is false, this field is ignored.

**Parent Topic:**[Exploring Advanced Work Assignment](awa-overview.md)


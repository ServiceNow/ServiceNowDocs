---
title: Universal Request states and reasons
description: The Universal Request \(UR\) state is determined by the state of the primary ticket. The primary ticket for a UR is a child department ticket, such as an IT incident or a HR case. A Universal Request can have only one primary ticket at a time.
locale: en-US
release: zurich
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Universal Request, Employee Service Management]
---

# Universal Request states and reasons

The Universal Request \(UR\) state is determined by the state of the primary ticket. The primary ticket for a UR is a child department ticket, such as an IT incident or a HR case. A Universal Request can have only one primary ticket at a time.

Given are some examples of the impact of the primary ticket on UR:

-   If there is no primary ticket, then the Standard Ticket configuration for UR determines requester page view of the UR ticket.
-   If a child IT incident is the primary ticket of a UR, then the Incident Standard Ticket configuration determines the requester page view of the UR ticket.
-   If a child HR case is the primary ticket of a UR, then the Case Standard Ticket configuration determines the requester page view of the UR ticket.

## UR states and state reasons

The Universal Request \(UR\) state describes where in the life cycle the UR request is.

<table id="table_lds_cwg_llb"><thead><tr><th>

States

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

The UR request is created and is ready to be triaged. This is the first state in the life cycle.

</td></tr><tr><td>

In Progress

</td><td>

The state when the UR is being triaged and worked on. For example, the state can be In progress because of the following state reasons:-   **Triaging**: Is being triaged by the routing agent.
-   **Primary Ticket - In Progress**: Primary task is currently work in progress.
-   **Confirm Response**: Waiting on the routing agent's confirmation on the resolution provided by the department agent.

</td></tr><tr><td>

Awaiting Response

</td><td>

The state when there is a user action is pending. For example, the possible state reasons are one of the following:-   **Action Required**: When the agent has requested the user for some action or information.
-   **Accept Resolution**: When the agent has requested the requester for accepting the resolution.

</td></tr><tr><td>

Closed

</td><td>

The UR is closed.

</td></tr><tr><td>

Canceled

</td><td>

The UR is canceled.**Note:** Requesters can cancel a UR only if there are no active or closed primary tickets attached to it. Also, the state of UR must be either **New** or **In Progress**.

</td></tr></tbody>
</table>![Sample: State reason for In Progress state](../images/ur-state-reasons.png)

**Parent Topic:**[Exploring Universal Request](explore-universal-request.md)


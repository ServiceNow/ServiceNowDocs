---
title: Manually assign agents to active requests
description: Use this procedure to assign agents to active requests in service management \(SM\) applications.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Manually assign agents to active requests

Use this procedure to assign agents to active requests in service management \(SM\) applications.

## Procedure

1.  Navigate to one of the following modules:

    -   **\[SM application\]** &gt; **Open - Unassigned** for a list of requests that no one is assigned to.
    -   **\[SM application\]** &gt; **All \[SM application\] Requests** for a list of all open requests, regardless of their current assignment.
2.  Open the request you want to assign.

3.  In the **Assignment group** field, enter the group that handles this kind of request.

    If no groups are available, leave this field blank. To look up the assignment group, click the reference lookup icon \(![Lookup icon](../image/IconReferenceLookup.png)\) beside the **Assignment group** field.

    **Note:** You do not have to select an assignment group, but doing so limits the users you can assign the request to.

4.  In the **Assigned to** field, enter the agent to handle this request.

    To look up an agent, click the lookup icon \(![Lookup icon.](../image/IconReferenceLookup.png)\) beside the **Assigned to** field.

    **Note:** If one was selected, the users in the search results are limited to the users in the **Assignment group**.

5.  Click **Update**.

    An email notification is automatically sent to the assigned agent when email notifications are set up for the instance.


**Parent Topic:**[Agent assignment methods](../../service-management-core/concept/c_AgentAssignment.md)


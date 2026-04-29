---
title: Connect Support chat states
description: Connect Support chats move through specific states.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Connect Support chat states

Connect Support chats move through specific states.

![Connect Support states diagram showing the full cycle of states for a support conversation](../image/chat-support-states-diagram.png "Connect Support states diagram")

<table id="table_pzw_hcl_rw"><thead><tr><th>

Composite state

</th><th>

State

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Waiting

</td><td>

-   Requester/end user enters a queue by sending a message. Agent has not yet accepted it.
-   Requester/end user rejoins a session that is in a Reopenable state.

</td></tr><tr><td>

 

</td><td>

Work in Progress

</td><td>

-   Agent accepts a chat from a queue. Both requester and agent engage in a chat session.
-   Requester/end user temporarily leaves an ongoing conversation; requester or agent does not end the session; requester rejoins session.

</td></tr><tr><td>

Reopenable

</td><td>

Closed Abandoned

</td><td>

Requester/end user clicks **End Chat** button before agent accepts the request.

</td></tr><tr><td>

Permanently closed

</td><td>

Closed by Client

</td><td>

-   Requester/end user clicks **End Chat** button after agent accepts the request.
-   Requester/end user times out.

</td></tr><tr><td>

 

</td><td>

Closed Escalated

</td><td>

Agent escalates an ongoing conversation by performing the Escalate action from the menu icon.

</td></tr><tr><td>

 

</td><td>

Closed Complete

</td><td>

-   Agent ends the session.
-   During a chat, if an agent creates an incident or case and closes it, the chat session closes automatically.

</td></tr></tbody>
</table>
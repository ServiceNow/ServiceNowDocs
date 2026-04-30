---
title: Working on callback records in your workspace
description: Use Workspace to work on callback records originating from Omnichannel Callback
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working on records in your Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Working on callback records in your workspace

Use Workspace to work on callback records originating from Omnichannel Callback

## overview

Omnichannel Callback is a ServiceNow AI Platform® capability that provides an option for users to opt for a callback instead of waiting in the queue for an available agent. Advanced Work Assignment routes the callback work items to available agents and interaction records are created for each callback work request. The interaction records appear in the Workspace for agents to work on.

Agents can work on the records for the following callback scenarios.

-   Recurring callback: AWA routes a callback work item to an available agent based on the predefined callback attempt interval. The agent then receives a **Callback** work item. When the agent accepts the callback work item, auto-dial initiates a call to the user. Based on the resolution, the agent can either close the interaction or requeue the callback.
-   Click to call: The agent can directly call the end user using the phone icon in the interaction record if auto-dial is not enabled or the initial call did not succeed.
-   Scheduled voice callback: When a user requests a voice callback at their preferred date and time, an interaction record with callback details is created a minute before the scheduled call time and an agent receives the callback work item. When the agent accepts the callback work item, auto-dial initiates a call to the user. Based on the outcome, the agent can either close the interaction as **Closed Complete** or **Closed Abandoned**.
-   Scheduled video callback: When a user requests a video callback at their preferred date and time, an interaction record with callback details is created which includes a URL to initiate the video call. Based on the outcome, the agent can either close the interaction as **Closed Complete** or **Closed Abandoned**.

<table id="table_ch5_5nf_jvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reattempt callback

</td><td>

Agents can reattempt a callback by selecting the **More actions** button and then selecting **Re-attempt Callback**. The **Reason** menu displays and agents have the following options to choose from.-   Dead Air
-   VoiceMail
-   Customer is Busy
-   Other

</td></tr><tr><td>

Closing callback

</td><td>

If the issue is resolved, agents can close the callback. If closed, the system does not retry callbacks, and the callback task is closed. Agents can choose from the following options to close a callback.-   Resolved
-   Other

 When a callback is closed, agents can see the transcript and a recording of the conversation in the **Conversations** tab.

**Note:** The recording is also added to the **Activity** stream and the **Attachment** tab.

</td></tr></tbody>
</table>
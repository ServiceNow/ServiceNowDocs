---
title: Working on callback records
description: Use Workspace to work on callback records originating from Omnichannel Callback.
locale: en-US
release: xanadu
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Omnichannel Callback, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Working on callback records

Use Workspace to work on callback records originating from Omnichannel Callback.

Agents can work on the records for the following callback scenarios.

-   Recurring callback: When a user requests recurring callback, the callback request is added to the AWA queue. AWA routes the callback work item to an available agent based on the predefined callback attempt interval. The agent then receives a **Callback** work item. When the agent accepts the callback work item, auto-dial initiates a call to the user. Based on the resolution, the agent can either close the interaction or re-queue the callback.
-   Scheduled voice callback: When a user requests a voice callback at their preferred date and time, an interaction record with callback details is created a minute before the scheduled call time and an agent receives the callback work item. When the agent accepts the callback work item, auto-dial initiates a call to the user. Based on the outcome, the agent can either close the interaction as **Closed Complete** or **Closed Abandoned**.![Scheduled phone callback](../images/Callback-phone.png)
-   Scheduled video callback: When a user requests a video callback at their preferred date and time, an interaction record with callback details is created which includes a URL to initiate the video call. Based on the outcome, the agent can either close the interaction as **Closed Complete** or **Closed Abandoned**.![Scheduled video callback](../images/Callback-video.png)


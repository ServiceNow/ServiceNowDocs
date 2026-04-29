---
title: Users tab
description: Get detailed information on Virtual Agent users such as the time of the last conversation and duration of the conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# Users tab

Get detailed information on Virtual Agent users such as the time of the last conversation and duration of the conversation.

The **Users** tab provides information about users who interacted with Virtual Agent in a certain time period.

To access the **Users** tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

![Virtual Agent Analytics Users page with information about users and their conversations with VA](../images/users-tab-va-pae.png "Users page")

## Users tab benefits

The **Users** tab enables you to do the following:

-   Filter the list of users based on specific conditions using the filter editor. For more information, see [Use filters in the Users tab](users-tab-filtering-pae.md)
-   View user details. For more information, see User information section on this page.
-   Export the list of users to a file. For more information, see Export the list of users section on this page.

## Export the list of users

To export the list of users in the Users page to a file, select **Export**. In the Export pop-up window, specify the format for the file such as Excel, CSV, JSON, or PDF, and the delivery type such as email or download.

**Note:** You can export up to 1000 records only from the list on the page. This limit is not configurable.

## User information

The following table describes user details listed on the Users tab.

|Column|Description|
|------|-----------|
|User ID|User ID of the logged in user. If users don't log in, they appear in sessions as **Anonymous**.|
|Is Anonymous|If users didn't log in, they appear in the sessions as anonymous.|
|Channel|Conversation channel used by the user.|
|Last conversation|Timestamp of the user's last conversation with the Virtual Agent.|

-   **[Use filters in the Users tab](users-tab-filtering-pae.md)**  
You can use filters to get a deeper understanding of User data.

**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)


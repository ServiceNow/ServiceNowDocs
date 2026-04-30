---
title: Legacy - Users tab
description: Get detailed information on Virtual Agent users such as the time of the last chat, length of the chat, and other metrics.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Users tab

Get detailed information on Virtual Agent users such as the time of the last chat, length of the chat, and other metrics.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

The **Users** tab provides summary information about all users and detailed information about each user conversation with Virtual Agent.

To access the **Users** tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

![Virtual Agent Analytics Users page, with users filter set to All, highlighted.](../images/users-tab-va.png "Users page")

## Users tab benefits

The **Users** tab enables you to do the following:

-   Filter the list of users by using pre-built filtering options. For more information, see [Filtering the list of users](users-tab-filtering.md#section_chp_ddh_5pb).
-   Filter the list of users based on a specific condition and save conditions for filtering. For more information, see [Filter using the condition builder](users-tab-filtering.md#section_ons_xck_vpb).
-   View summarized information about users. For more information, see [User information](users-tab.md#section_vn2_kyj_b4b).
-   Export the list of users to a file. For more information, see [Export the list of users](users-tab.md#section_b4c_m3h_5pb).

## Export the list of users

To export the list of users in the Users page to a file, select **Export**. In the Export pop-up window, specify the format for the file such as Excel, CSV, JSON, or PDF, and the delivery type such as email or download.

**Note:** You can export up to 1000 records only from the list on the page. This limit is not configurable.

## User information

The following table describes the summarized Virtual Agent user information on the Users tab.

<table id="table_amh_4yj_b4b"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Index

</td><td>

Link to go to the User Details page. It is a unique number that the system creates and permanently assigns to a Virtual Agent user. This number becomes a part of conversation records.This number is not the same as the system user ID.

</td></tr><tr><td>

User ID

</td><td>

User ID of the logged in user. If users don't log in, they appear in sessions as **Anonymous**.

</td></tr><tr><td>

First conversation

</td><td>

How long ago the user first started the Virtual Agent conversation.

</td></tr><tr><td>

Last conversation

</td><td>

How long ago the user last had a Virtual Agent conversation.

</td></tr><tr><td>

Time on Chat

</td><td>

Duration of the Virtual Agent chat.

</td></tr><tr><td>

Last Used Channel

</td><td>

Client software the user last used to chat.

</td></tr><tr><td>

Last Used Language

</td><td>

Language the user last used in a Virtual Agent conversation.

</td></tr><tr><td>

Favorite

</td><td>

Indicates whether the user is tagged as favorite.

</td></tr></tbody>
</table>## Field options in the Filter Editor

|Option|Description|
|------|-----------|
|User ID|User ID of the logged in user.|
|User Index|Unique number that the system creates and permanently assigns to a Virtual Agent user. This number becomes a part of conversation records.|
|Conversation Exists|Container for subfilter properties. For example, in the previous image, the subfilter is **Duration**.|
|Channel Count|Number of channels a user used. A channel is the client app the user used, such as Slack. For example, if all users have used only one channel to chat with Virtual Agent, then setting the filter value to 2 eliminates all the users in the list.|
|Channels|Only displays users that used the specified channel to chat.|
|Conversation Count|Only displays users that have the number of conversations specified in the filter.|
|Favorite|Only displays users that you marked as favorite, or conversely, not marked as favorite in the User Details page. For more information, see [Legacy - User Details page](user-page.md).|
|First Conversation Time|Only displays users where the first conversation is within the time period specified.|
|Language|Only displays users that chat using the specified language.|
|Last Conversation Time|Only displays users where the last conversation is within the time period specified.|
|Time in Chat|Only displays users whose chat durations are within the time period specified, for example, more than 30 seconds.|

-   **[Legacy - User Details page](user-page.md)**  
Use the User Details page to see the history of a user's conversations.
-   **[Legacy - Use filters in the Users tab](users-tab-filtering.md)**  
You can use filters to get a deeper understanding of User data.

**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](use-the-dashboard-overview.md)


---
title: Legacy - Use filters in the Users tab
description: You can use filters to get a deeper understanding of User data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/conversational-interfaces/virtual-agent/users-tab-filtering.html
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Users, tab, filter, Virtual Agent, legacy, condition builder]
breadcrumb: [Legacy - Users tab, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Use filters in the Users tab

You can use filters to get a deeper understanding of User data.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

## Filter using the condition builder

The condition builder enables you to filter users based on one or more conditions. You can either select a default filter from the list or create a new filter condition. In the following example, the condition lists users whose conversations with the Virtual Agent lasted greater than 21 seconds.

\[Omitted image "users-page-filter-va.png"\] Alt text: Condition builder in the Filter Editor pop-up window, showing conditions: Conversation Exists, in which duration is greater than 21 seconds.

The condition builder consists of the following:

-   Field: A list based on relevant tables.
-   Operator: A list of operations that is contextually generated based on the selected field.
-   Value: A text entry field or a list that is contextually generated based on the selected field.

To remove a condition, select the delete icon \[Omitted image "delete-icon.png"\] Alt text: Delete icon. next to the condition. To add dependent conditions in the condition builder, either select **or** or **and**. To filter the conversations list using the condition, select **Run**.

To save a condition that you created in the condition builder, select **Save Filter**. In the Save Filter pop-up window, specify a name for the condition. Users having the Chat Analytics Viewer \(chat\_analytics\_viewer\) role can select and modify your saved filters.

\[Omitted image "condition-saved.png"\] Alt text: Filter Editor with filters dropdown open, All filter selected, and Channel Web Client shown under Saved Filters.

## Filtering the list of users

Use the list options to filter users.

|Option|Description|
|------|-----------|
|All|All Virtual Agent users.|
|New|First conversation happened within the past seven days.|
|Returning|Users who previously used Virtual Agent.|
|Never Returned|Users who used Virtual Agent once, but haven't used it again. The conversation count is 1.|

Selecting a **User Index** takes you to the [User Details page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/user-page.md) that provides detailed information about all of a user's conversations.

## Field options in the Filter Editor

|Option|Description|
|------|-----------|
|User ID|User ID of the logged in user.|
|User Index|Unique number that the system creates and permanently assigns to a Virtual Agent user. This number becomes a part of conversation records.|
|Conversation Exists|Container for subfilter properties. For example, in the previous image, the subfilter is **Duration**.|
|Channel Count|Number of channels a user used. A channel is the client app the user used, such as Slack. For example, if all users have used only one channel to chat with Virtual Agent, then setting the filter value to 2 eliminates all the users in the list.|
|Channels|Only displays users that used the specified channel to chat.|
|Conversation Count|Only displays users that have the number of conversations specified in the filter.|
|Favorite|Only displays users that you marked as favorite, or conversely, not marked as favorite in the User Details page. For more information, see [Legacy - User Details page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/user-page.md).|
|First Conversation Time|Only displays users where the first conversation is within the time period specified.|
|Language|Only displays users that chat using the specified language.|
|Last Conversation Time|Only displays users where the last conversation is within the time period specified.|
|Time in Chat|Only displays users whose chat durations are within the time period specified, for example, more than 30 seconds.|

**Parent Topic:**[Legacy - Users tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/users-tab.md)


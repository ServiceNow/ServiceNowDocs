---
title: Use filters in the Users tab
description: You can use filters to get a deeper understanding of User data.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-11-06"
reading_time_minutes: 2
keywords: [Filter, Users, Tab, Virtual Agent]
breadcrumb: [Users tab, Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Use filters in the Users tab

You can use filters to get a deeper understanding of User data.

## Filter using the filter editor

The filter editor enables you to filter users based on one or more conditions. You can either select an existing filter from the list or create a new filter using the editor.

The filter editor consists of the following:

-   Field: A list based on relevant tables.
-   Operator: A list of operations that is contextually generated based on the selected field.
-   Value: A text entry field or a list that is contextually generated based on the selected field.

To remove a condition, select the delete icon ![Delete icon](../images/delete-icon.png) next to the condition. To add dependent conditions in the condition builder, either select **or** or **and**. To filter the conversations list using the condition, select **Update**.

To save a condition that you created in the filter editor, select **Save filter**. In the Save Filter pop-up window, specify a name for the filter. You can also set permissions for the filter in the Save Filter window. Users having the Chat Analytics Viewer \(chat\_analytics\_viewer\) role can select and modify your saved filters.

![Filter Editor with filters dropdown open, All filter selected, and Channel Web Client shown under Saved Filters.](../images/condition-saved-pae.png "Saved condition")

## Field options in the Filter Editor

|Option|Description|
|------|-----------|
|User ID|User ID of the logged in user.|
|User Index|Unique number that the system creates and permanently assigns to a Virtual Agent user. This number becomes a part of conversation records.|
|Conversation Exists|Container for subfilter properties. For example, in the previous image, the subfilter is **Duration**.|
|Channel Count|Number of channels a user used. A channel is the client app the user used, such as Slack. For example, if all users have used only one channel to chat with Virtual Agent, then setting the filter value to 2 eliminates all the users in the list.|
|Channels|Only displays users that used the specified channel to chat.|
|Conversation Count|Only displays users that have the number of conversations specified in the filter.|
|First Conversation Time|Only displays users where the first conversation is within the time period specified.|
|Language|Only displays users that chat using the specified language.|
|Last Conversation Time|Only displays users where the last conversation is within the time period specified.|
|Time in Chat|Only displays users whose chat durations are within the time period specified, for example, more than 30 seconds.|

**Parent Topic:**[Users tab](users-tab-pae.md)


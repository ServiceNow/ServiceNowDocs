---
title: Mobile app prerequisites for enhanced chat
description: Now Assist in Virtual Agent provides users with a content-driven and search-driven generative AI experience. Depending on whether you have opted into standard or enhanced chat when configuring your assistant, you can integrate three different mobile app components with an assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Mobile app prerequisites for enhanced chat

Now Assist in Virtual Agent provides users with a content-driven and search-driven generative AI experience. Depending on whether you have opted into standard or enhanced chat when configuring your assistant, you can integrate three different mobile app components with an assistant.

For information on choosing how you want Now Assist in Virtual Agent to display on your mobile app, see [Mobile Now Assist display experience for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-na-display-experience-va.md). To understand the differences between Now Assist in Virtual Agent standard and enhanced chat experiences, see [Using Now Assist in Virtual Agent](using-now-assist-in-va.md).

The three different mobile app components that admins can integrate with an assistant are a mobile search widget, chat launcher, and custom app.

|Mobile app component|Description|Standard chat|Enhanced chat|
|--------------------|-----------|-------------|-------------|
|Mobile search widget|The search bar widget within the ServiceNow Mobile App|No|Full-page experience only|
|Chat launcher|The default Virtual Agent chat widget|Yes, but only offered to existing Now Assist in Virtual Agent customers|Yes|
|Custom app \(Mobile SDK\)|The tool to display native Virtual Agent interface in a customer’s own third-party app.|Yes, but only offered to existing Now Assist in Virtual Agent customers|Yes|

<table id="table_nzt_vbc_1fc"><thead><tr><th>

Mobile app component

</th><th>

Enhanced chat behavior

</th><th>

Prerequisites

</th></tr></thead><tbody><tr><td>

Mobile search widget

</td><td>

Typing an utterance in the search bar opens a full-screen chat experience. Users can launch the search results page from the chat.

</td><td>

Admins must select the mobile search conﬁguration to be used. For more information, see [Display your chat assistant on a portal, channel, or mobile app](../task/display-assistant-portal-channel.md).

</td></tr><tr><td>

Chat launcher

</td><td>

Selecting the chat function in a mobile app opens native Virtual Agent. A user can ask questions in native Virtual Agent and get Now Assist responses. Users can also launch the search results page from the chat.

</td><td>

Admins can optionally select the Mobile Search Configuration to improve the metadata quality.

</td></tr><tr><td>

Custom app \(mobile SDK\)

</td><td>

Selecting the custom chat function in a third-party mobile app opens native Virtual Agent. Users can ask questions in native Virtual Agent and get Now Assist responses.

</td><td>

You can't use the Now Assist in Virtual Agent AI Search experience in a custom app. Search is run by the customer's third-party mobile app/

</td></tr></tbody>
</table>
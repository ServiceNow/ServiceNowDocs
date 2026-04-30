---
title: Auto-complete suggestion types included with Now Assist in AI Search
description: Now Assist in AI Search includes an auto-complete suggestion type that displays suggested Now Assist in Virtual Agent queries.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-03"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist in AI Search reference, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Auto-complete suggestion types included with Now Assist in AI Search

Now Assist in AI Search includes an auto-complete suggestion type that displays suggested Now Assist in Virtual Agent queries.

To learn more about how this auto-complete suggestion type appears to search and chat users, see [Enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US). For details on configuring and using auto-complete suggestion types in your search application configurations, see [Auto-complete suggestions in AI Search applications](../concept/auto-complete-ais.md#).

<table id="table_rc4_z2y_v2c"><thead><tr><th>

Auto-complete suggestion type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Now Assist Suggested Query Reader Group for &lt;application name&gt;

</td><td>

Displays Virtual Agent conversational prompts based on previous user searches \(utterances\) that produced synthesized Genius Result responses. Selecting a suggested prompt opens a Virtual Agent conversation within the enhanced chat window or full-page experience.

 User queries from Virtual Agent conversations are stored as suggestions in the Utterance Suggestions \[sys\_suggested\_utterance\] table. The system prunes this table and automatically removes query suggestions if they meet either of these conditions:

-   The query and result combination have not been used in a search within the last 180 days.
-   The query suggestion refers to a record \(such as a Catalog Item or a knowledge article\) that has been deleted or deactivated.

 When you create a new search application configuration, this suggestion reader group isn't linked to it by default. If you enable enhanced chat in a search portal, this suggestion reader group is linked to the search application configuration record that's shared between the portal and Virtual Agent.

 Default section header: `Ask Now Assist`

 Readers: Now Assist Suggested Utterance Reader

 **Note:** This suggestion reader group is only supported in search application configurations for applications that support the enhanced chat experience, such as the Now Assist in VA search application configuration.

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist in AI Search reference](../concept/reference-now-assist-ais.md)


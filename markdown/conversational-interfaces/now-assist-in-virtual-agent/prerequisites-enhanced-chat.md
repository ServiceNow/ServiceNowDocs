---
title: Portal prerequisites for enhanced chat
description: Now Assist in Virtual Agent provides users with a content-driven and search-driven generative AI experience. To benefit from chat and search capabilities, your portal must have AI Search enabled before configuring your assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Portal prerequisites for enhanced chat

Now Assist in Virtual Agent provides users with a content-driven and search-driven generative AI experience. To benefit from chat and search capabilities, your portal must have AI Search enabled before configuring your assistant.

Standard chat or enhanced chat offers different experiences. Enhanced chat provides users with a resizable chat window and search experience. To understand the differences between standard chat, enhanced chat, and enhanced chat with an additional full-page experience option, see [Using Now Assist in Virtual Agent](using-now-assist-in-va.md). If you only want a chat experience, there's no dependency on a portal's search configuration. However, ensure that your portal has the default chat widget button.

To benefit from enhanced chat's search capabilities, your portal should have AI Search enabled. To configure AI Search for your portal, navigate to **All** &gt; **AI Search Admin Home**. For more information, see [Enable and configure AI Search in Service Portal](https://www.servicenow.com/docs/access?context=enable-ais-sp&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

**Note:** When you activate enhanced chat in a portal, that portal uses the VA Search Profile instead of the search profile specified in the portal's search application configuration. To learn more about search profiles and how they affect search behavior, see [Search profiles in AI Search](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Within the enhanced chat experience, the full-page experience is an additional option.

The prerequisites for both the enhanced chat experience and the enhanced chat with full-page experience are:

1.  Portal AI Search configuration
2.  Faceted Search widget
3.  ServiceNow default Typeahead Search widget \(required only for the enhanced chat with full-page experience\)

**Note:** If you customized the Faceted Search widget or the Typeahead Search widget, you must reconcile your customizations with the latest versions to ensure that you have all of the updates.


---
title: Web search
description: The web search mode performs an internet search to answer a query. Web search mode provides external search results from the internet and these results don't represent company content or policies.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Web search, Websearch]
breadcrumb: [Using Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Web search

The web search mode performs an internet search to answer a query. Web search mode provides external search results from the internet and these results don't represent company content or policies.

**Note:** For more information about how to configure web search and turn on web search, see [Web search custom skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/web-search-custom-skill.md) and [Manage an assistant chat experience](../task/manage-assistant-chat-experience.md).

Web search mode is applicable to Now Assist in Virtual Agent standard chat and enhanced chat conversations. Select the Start web search mode icon \(![Start web search mode icon.](../../dynamic-translation/image/Globe.png)\) to enter into the web search mode. While in this mode, all queries are answered via internet search results rather than internal company search results. When in web search mode, a divider line appears to indicate a conversational shift and the following text appears: `Searching the web (This search is external and does not represent Company content or policies.)`

For example, if you ask `What's the latest Macbook pro configuration?` in web search mode, a synthesized response appears along with inline citations and sources.

![Web search mode providing results and including in-line citations.](../image/dw-web-search-example.png "Example of enhanced chat's web search mode")

![Web search mode providing results and including in-line citations.](../image/standard-chat-web-search-example.png "Example of standard chat's web search mode")

You can also use web search as a fallback option. For example, if you ask `What's the weather in Las Vegas in the month of May?`, the LLM and AI Search are unable to find an answer through internal sources. Instead, you can be presented with the fallback option to **Search the web**.

![Search the web button is a fallback option for end users.](../image/dw-web-search-fallback-example.png "Example of enhanced chat's search the web fallback option")

**Note:** When entering web search via the Start web search icon \(![Start web search icon.](../../dynamic-translation/image/Globe.png)\), the prior conversational history is blanked out. When entering web search via the fallback **Search the web** option, only the last query prior to entering web search mode is taken into account.

To exit out of web search mode and return to internal search results, do one of the following:

-   Enter `Exit`.
-   Select the End web search icon \(![End web search icon.](../../dynamic-translation/image/Globe.png)\).
-   Select **End** in the Web Search banner.

    **Note:** The Web Search banner is only applicable to enhanced chat conversations.



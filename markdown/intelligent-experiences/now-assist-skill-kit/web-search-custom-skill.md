---
title: Web search custom skill
description: The web search custom skill performs an internet search to answer a query. Web search is used whenever the LLM and AI Search are unable to provide results or whenever web search mode is activated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/web-search-custom-skill.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2025-04-18"
reading_time_minutes: 2
keywords: [Now Assist, Virtual Agent, Web Search, custom skill, AI Search, LLM]
breadcrumb: [Now Assist Skill Kit reference, Now Assist Skill Kit, Enable AI experiences]
---

# Web search custom skill

The web search custom skill performs an internet search to answer a query. Web search is used whenever the LLM and AI Search are unable to provide results or whenever web search mode is activated.

The web search custom skill is based on a prebuilt topic block in Virtual Agent Designer, and is available when you turn on Now Assist in Virtual Agent. This feature is automatically triggered when both AI Search and the LLM can't find information to answer an end user's query. This feature can also be manually triggered whenever end users select the Web search results icon \(\[Omitted image "Globe.png"\] Alt text: Web search results icon.\) to enter into web search mode. Once web search activates, a third-party AI performs the search and returns with an answer.

\[Omitted image "web-search-custom-skill-01.png"\] Alt text: Virtual Agent Designer topics list showing the web search custom skill, setup topic, and prebuilt topic.

For more information about the web search mode end-user display and functionality, see .

Web Search AI choices are available in the OneExtend Definition Configs related list within the **AI Search answers** entry in the OneExtend Capabilities \[sys\_one\_extend\_capability\_list\] table. Select one of the AI definitions there, such as Perplexity, and set its value to `true`. Activate a matching AI credential by navigating to **ALL** &gt; **Connections &amp; credentials** &gt; **Credentials**, and setting the matching API key \(such as **Perplexity API key** active value to `true`\).

\[Omitted image "web-search-custom-skill-02.png"\] Alt text: OneExtend Capabilities table showing AI search answers property, and the OneExtend Capabilities Configs tab within. Perplexity AI answers is set as the default search AI.

\[Omitted image "web-search-custom-skill-03.png"\] Alt text: Credentials table showing the Perplexity API key entry, with Active value set to true.

For more information on how to work with the **AI Search answers** OneExtend capability, see [Configure AI search answers capability for web search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/configure-ai-search-answers-capability-for-web-search.md).

For more information on how to add web search as a tool in the Now Assist Skill Kit, see [Add a web search tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/add-web-search.md).

**Parent Topic:**[Now Assist Skill Kit reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/na-skill-kit-reference.md)


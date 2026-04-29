---
title: Now Assist Conversational Help
description: This skill uses Generative AI application capabilities to provide answers to the questions on the Now Assist panel.
locale: en-US
release: australia
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Skills in the Platform workflow, Now Assist skills, Now Assist AI assets, Enable AI experiences]
---

# Now Assist Conversational Help

This skill uses Generative AI application capabilities to provide answers to the questions on the Now Assist panel.

Now Assist Conversational Help overview

**Important:** Starting with the Australia release, Conversational Help Skills is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base.

You can install the External Content Connectors Application Suite from the [ServiceNow store](https://store.servicenow.com/store/app/dd69bc781bd9a650396216db234bcb0b)

and use NAp Synthesized Search with ServiceNow Docs.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](now-assist-skills-on-by-default.md).

The Now Assist Conversational Help skill displays as **Get Help** on the Now Assist panel.

**Note:** The Get Help feature is available as a part of Now Assist entitlements and no new subscription is required. The feature is enabled by default and you can turn it off in the Now Assist Admin **Settings**. The ServiceNow Now LLM Service \(Large Language Model\) is the default model provider for this Now Assist skill to retrieve precise answers to the users' questions.

## How Conversational Help works

You can ask your question by selecting **Get Help** skill and submit a query to use the help option in the Now Assist panel. Your query goes through the following steps to retrieve the best response.

**Note:** Conversational Help Skills is not available as auto-discoverable as a help skill within Now Assist panel.

1.  AI search

    The query is be sent to a **central ServiceNow instance**, where **AI Search** will search the knowledge table that stores content from product doc content.

    We use Instance Data Replication \(IDR\) that synchronizes product documentation content from Now Support instances.

    **Note:** Multiple central ServiceNow instances are deployed across three regions: US East or US West, EMEA, and APJC.

2.  The top matching chunks \(or records\) along with the user’s query, are sent to the Now Assist Q&amp;A Genius Result configuration to generate a meaningful, contextual answer.
3.  Re-ranking

    The Now Assist Q&amp;A, an out of box \(OOB\) capability, re-ranks the retrieved chunks to ensure better relevance.

4.  Cache lookup
    -   If the user query exists in the cache, the pre-stored answer is returned.
    -   If the query is not cached, the query and re-ranked chunks are sent to Now LLM to generate a meaningful answer.

The Now LLM retrieves the most relevant result from [https://www.servicenow.com/docs/](https://www.servicenow.com/docs/) portal and displays it in the same panel.

**Note:** Effective from this release, the query will retrieve results based exclusively on the release version of the user's current instance. This enhancement is integrated into the query process to ensure the delivery of precise results that reflect the latest updates and features.

![Now Assist Conversational Help skill](../image/na-conversational-help-skills.png)

For more information, see [Fetch end points in Now Assist Conversational Help skills](../reference/fetch-end-points-in-conversational-help-skill.md).


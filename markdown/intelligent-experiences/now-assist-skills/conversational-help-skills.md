---
title: Now Assist Conversational Help
description: This skill uses Generative AI application capabilities to provide answers to the questions on the Now Assist panel.
locale: en-US
release: yokohama
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Skills in the Platform workflow, Now Assist skills, Now Assist AI assets, Enable AI experiences]
---

# Now Assist Conversational Help

This skill uses Generative AI application capabilities to provide answers to the questions on the Now Assist panel.

Now Assist Conversational Help overview

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](now-assist-skills-on-by-default.md).

The Now Assist Conversational Help skill displays as **Get Help** on the Now Assist panel.

**Note:** The Get Help feature is available as a part of Now Assist entitlements and no new subscription is required. The feature is enabled by default and you can turn it off in the Now Assist Admin **Settings**. The ServiceNow Now LLM Service \(Large Language Model\) is the default model provider for this Now Assist skill to retrieve precise answers to the users' questions.

You can ask your question in two ways:

-   Select **Get Help** skill and submit a query to use the help option in the Now Assist panel.
-   Submit your query directly in the Now Assist panel. It will perform discovery and find the most appropriate skill among the listed, based on the keywords you entered. This discovered skill is used to retrieve answers for your queries.

    **Note:** The available skills displayed in the Now Assist panel can be customized in consultation with the integration teams.


## How Conversational Help works

Your query goes through the following steps to retrieve the best response.

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

**Parent Topic:**[Now Assist skills in the Platform workflow](now-assist-on-now-platform.md)


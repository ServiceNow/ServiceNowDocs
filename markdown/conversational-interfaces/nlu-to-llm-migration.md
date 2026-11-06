---
title: NLU to LLM topic migration
description: Migrate your Natural Language Understanding \(NLU\) and keyword Virtual Agent topics to large language model \(LLM\) topics in phases. You can improve topic discovery without disrupting conversations that already work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/nlu-to-llm-migration.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 3
keywords: [NLU to LLM, LLM migration, Virtual Agent NLU]
breadcrumb: [Explore NLU, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# NLU to LLM topic migration

Migrate your Natural Language Understanding \(NLU\) and keyword Virtual Agent topics to large language model \(LLM\) topics in phases. You can improve topic discovery without disrupting conversations that already work.

## Decide whether to migrate a topic

You don't have to migrate every topic immediately. NLU topics remain a good fit for predictable, structured conversations. LLM topics add the most value when:

-   Users describe the same request in many different ways.
-   You have many similar topics that are often misclassified.
-   Conversations depend on follow-up questions and context.
-   Topics change often, and maintaining utterances and retraining models takes significant effort.

## Plan how NLU and LLM topics coexist

NLU and keyword topics aren't available in LLM assistants, and LLM topics aren't available in Virtual Agent for NLU. An LLM assistant doesn't fall back to NLU topics. Any topic you don't migrate isn't discoverable in that assistant.

Before you migrate, decide which portals and channels should move to an LLM assistant and when. Make sure that every topic those users need is either migrated or replaced before you switch them over.

For more information, see [Configure assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/configure-now-assist-va.md).

## Review and prepare your inventory

1.  Identify topics with little or no usage, and retire them instead of migrating them.
2.  Check whether a prebuilt LLM topic already covers the use case.

    Use the prebuilt topic instead of migrating your own when it meets your needs. For more information, see [ITSM Virtual Agent pre-built LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-va-prebuilt-topics.md).

3.  Prioritize your remaining NLU topics.
    -   **Migrate first**

        High-volume topics, topics with frequent discovery failures, and topics with highly variable phrasing or multi-language usage.

    -   **Migrate later**

        Highly predictable topics that already work well, such as password resets and simple catalog requests.


## Migrate and test your topics

Before beginning, verify the following:

-   You have the virtual\_agent\_admin or admin role
-   ServiceNow Otto for Virtual Agent is installed
-   The Now Assist Topics skill is turned on
-   AI Search and ServiceNow Otto for AI Search are installed and activated for Virtual Agent
-   Your ServiceNow Otto plugins are up to date.

    When you update plugins, start with the parent plugin so that dependent plugins update correctly.


**Note:** Migrate fewer than 50 topics at a time so that you have time to review and test each one.

1.  Review this topic: [Migrating NLU/keyword Virtual Agent topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/llm-topic-migration.md).
2.  Follow the steps in [Migrate NLU topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/migrate-nlu-llm.md).
3.  Review the migration log.

    For details, see [NLU to LLM migration log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/llm-topic-migration-error-log.md). Expect some manual cleanup. Manually migrate and update dynamic topic blocks or switch topic scripts that were flagged. Process failures may require help from Now Support. Budget extra time if you have many complex topics.

4.  Rewrite topic and node descriptions.

    NLU intents don't make good LLM prompts. Ensure that you modify the description and instructions for your new LLM topics. For more information, see [LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/va-llm-instruction-guidelines.md).

5.  Follow the steps in [Testing LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/test-llm-topics.md).

    Ensure that you're testing topic discovery by typing in the chat to find the topic, not just clicking on the topic.

6.  Pilot your batch of LLM topics in one channel.

    Watch fallback rates and discovery misses, then migrate the next batch.



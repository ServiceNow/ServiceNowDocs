---
title: NLU Service updates
description: Refer to this documentation so you are up to date with changes to the NLU Service.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Natural Language Understanding, Natural Language Understanding, Enable AI experiences]
---

# NLU Service updates

Refer to this documentation so you are up to date with changes to the NLU Service.

## Service update summary

The NLU Service helps the system to understand natural language and drive intelligent actions. This service trains and predicts intents and entities for a given user utterance in your NLU model so it can understand human-expressed natural language, whether spoken or written. The source of this documentation is [KB0953693](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0953693).

This service is updated independently of your instance upgrade, and without any action required by you. These updates are done on a bi-monthly basis \(once every two months\) to improve the quality of NLU model training and predictions. Major updates are aligned with family releases such as Rome, San Diego, Tokyo, etc. Minor updates are automatically updated so you are using the latest version when you retrain an NLU model. While most of these updates don't impact your existing use of NLU, there may be some changes you need to be aware of.

## May 2023 NLU Service update

-   Introduced dialog acts to enable natural mid-conversation in Virtual Agent \(VA\) and improve conversation fluidity. Affirm, negate, and modify dialog acts are supported in English and enabled by default for all new VA topics.
-   Migrated all languages to use new language models, boosting average intent prediction quality by 10% across all languages.
-   Enabled customers to manage and edit irrelevant utterances for their models to improve irrelevance detection.
-   Removed the requirement for a model to have 2 or more intents in the model, making it easier for end-to-end topic testing in VA.

## March 2023 NLU Service update

-   Improved intent/entity detection through better handling of common words in vocabulary sources.
-   Improved latency and memory utilization for system entity \(NER\) detection.
-   Updated version support so that customers will need to use newer versions of the NLU Service and cannot point to n-2 releases older than their current glide version.

## January 2023 NLU Service update

-   Created the new DATE-TIME system entity \(English only\) for use in Virtual Agent.
-   Added vocabulary source and entity support \(simple, mapped, and open ended\) for the Dutch and Italian languages, and system entity support for Portuguese and Brazilian Portuguese.
-   Upgraded the ServiceNow Language Model for the Danish, Swedish, Finnish, and Norwegian languages, improving their average prediction quality by 17% from Tokyo.
-   Improved the handling of punctuation in entities and special characters in vocabulary sources.
-   Incorporated feedback provided on intent predictions by admin users in the NLU Workbench to improve model training data for Virtual Agent.

**Parent Topic:**[Exploring Natural Language Understanding](nlu-explore.md)


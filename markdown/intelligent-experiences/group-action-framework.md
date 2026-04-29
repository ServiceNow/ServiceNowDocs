---
title: Group Action Framework
description: Group Action Framework \(GAF\) is an intelligence feature on the ServiceNow AI Platform that groups related records and applies actions to them using LLMs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [gaf]
breadcrumb: [Explore, Now Assist AI agents, Enable AI experiences]
---

# Group Action Framework

Group Action Framework \(GAF\) is an intelligence feature on the ServiceNow AI Platform that groups related records and applies actions to them using LLMs.

## GAF overview

GAF is composed of two processes. The grouping process identifies clusters of similar records \(incident, cases, KB articles, etc.\) and selects a set of representative records for the cluster. The actioning process maps new records to clusters and executes large language model \(LLM\) instructions for those clusters to achieve certain tasks, such as summarizing the contents of a cluster or generating resolution steps based on steps that worked for records in that cluster. GAF processes together benefit your AI agents and Now Assist generative features in multiple ways.

-   Improves consistency and quality of agentic and generative AI features by using the best examples from groups of records.
-   Reduces the cost of LLM calls by only executing on the representative records.
-   Scales to accommodate large amounts of data because selected records can represent any size cluster.

## Skills used in GAF

Multiple skills are involved in GAF setup and execution. They are modular, so not all executions will use all skills, but they can be used together in tandem. These skills are used exclusively for GAF and currently cannot be included on their own in custom agentic workflows.

-   **Grouping skill**

    Clusters related records using machine learning techniques.

-   **Topic-labeling skill**

    Adds human-readable names to the clusters using an LLM to make the clusters easier to identify.

-   **Action strategy skill**

    Selects representative records from each cluster for the mapper and reducer skills to use.

-   **Action mapper skill**

    Runs LLM inference calls for the selected representative records, producing a record summary for the selected records.

-   **Action reducer skill**

    Uses the generated summaries created by the mapper skill to produce a single summary for the entire cluster.


## GAF and Now Assist in AI Search

GAF uses AI Search to improve its effectiveness and can use it as a fallback option in case GAF does not return any results. GAF can work without Now Assist in AI Search, but if it is enabled then GAF has optimized prediction. The optimized prediction feature increases clustering capacity up to 500,000 records and improves recall speed.

See [Install Now Assist in AI Search](https://www.servicenow.com/docs/access?context=install-now-assist-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Set up AI Search for Group Action Framework](../task/setup-ai-search-gaf.md) for more information on configuring AI Search for GAF.


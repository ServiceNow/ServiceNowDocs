---
title: Group Action Framework
description: Group Action Framework \(GAF\) is an intelligence feature on the ServiceNow AI Platform that groups related records and applies actions to them using LLMs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/group-action-framework.html
release: australia
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 4
keywords: [gaf]
breadcrumb: [Explore, AI Agent Studio, Enable AI experiences]
---

# Group Action Framework

Group Action Framework \(GAF\) is an intelligence feature on the ServiceNow AI Platform that groups related records and applies actions to them using LLMs.

## GAF overview

GAF is composed of two processes. The grouping process identifies clusters of similar records \(incident, cases, KB articles, and the actioning process maps\) new records to clusters and selects the representative record. Topic-labeling occurs during the setup process and labels the different clusters, which form the **Description** field of records on the GAF record groups \[sn\_gaf\_record\_group\] table. GAF processes together benefit your AI agents and generative AI features in multiple ways.

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


## GAF and AI Search

GAF uses AI Search to improve its effectiveness and uses it as a fallback option in case GAF does not return any results. When AI Search is enabled, then GAF can utilize its optimized prediction. The optimized prediction feature increases clustering capacity up to 500,000 records and improves recall speed.

See [Install AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/install-now-assist-ais.md) and [Set up AI Search for Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/setup-ai-search-gaf.md) for more information on configuring AI Search for GAF.

## Grouping inputs

When you configure GAF, the Grouping inputs record in the Now Assist Skill Config Var Set defines what records are clustered and how clustering behaves. The default values work for most configurations, but the following parameters are available if you need to adjust them.

-   **Table**

    The source table whose records are clustered. For example, the Incident \[incident\] table for ServiceNow Otto for ITSM.

-   **Fields**

    The field or fields used as the basis for clustering. GAF compares the content of these fields across records to identify similar ones.

-   **Filter**

    Conditions that determine which records from the source table are included in the grouping. You should have at least 2,000 records after filters are applied for clustering to complete successfully.

-   **Use taxonomy**

    When enabled, applies a taxonomy to improve the categorization of clusters.

-   **HTML Preprocessing**

    When enabled, strips HTML markup from field content before clustering. Enable this if your source records contain HTML-formatted text.

-   **Dimensionality reduction parameters \(UMAP\)**

    Controls how GAF compares records to each other before clustering. The **n\_neighbors** parameter \[2–100\] sets how many similar records GAF considers when deciding which cluster a record belongs to. The **n\_components** parameter \[5–100\] sets how many characteristics of each record GAF tracks during that comparison.

-   **Clustering parameters \(HDBScan\)**

    Controls how clusters are formed from the compared records. The **min\_samples** parameter \[2–10\] sets how many similar records must exist before GAF treats a pattern as a real cluster rather than noise. The **min\_cluster\_size** parameter \[2–100\] sets the minimum number of records required to form a cluster. The **cluster\_selection\_epsilon** parameter \[0.01–0.99\] controls how similar two clusters need to be before GAF merges them into one.


**Note:** The default values for UMAP and HDBScan parameters work for most configurations. Larger, denser clusters represent more common issue patterns and are surfaced more frequently. GAF's retrieval logic also handles smaller clusters, so less common patterns are still accessible.

## Diagnosing and troubleshooting GAF

To find logs where GAF is used on your instance, go to the Generative AI Log \[sys\_generative\_ai\_log\] table and filter based on the skill that used GAF. You can also filter the Log \[syslog\] table for the scope containing `sn-gaf`. Actions performed by skills, AI agents, and agentic workflows that use GAF all generate logs.

For more information about common errors and possible resolution steps, see [Troubleshooting GAF](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/troubleshooting-gaf.md).

## Additional information

GAF does not support domain separation at this time.


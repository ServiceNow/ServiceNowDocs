---
title: Configure solution definitions to find gaps in a knowledge base
description: The Knowledge Demand Insights feature finds knowledge gaps by comparing knowledge bases with existing tasks. To enable comparing knowledge bases with a task type, you must first configure similarity and clustering solution definitions.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configuration tasks for knowledge demand insights, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure solution definitions to find gaps in a knowledge base

The Knowledge Demand Insights feature finds knowledge gaps by comparing knowledge bases with existing tasks. To enable comparing knowledge bases with a task type, you must first configure similarity and clustering solution definitions.

## Before you begin

This task describes the process for configuring a solution definition.

Instead of doing the configuration through this procedure, consider using a guided setup. Navigate to **Knowledge** &gt; **Administration** &gt; **Guided Setup**, click **Get Started**, and then scroll to the Knowledge Demand Insights section.

Role required: admin

## About this task

Configure one similarity type and one clustering type solution definitions for each task type: incidents, customer service cases, or other tasks. A similarity solution definition collects and compares your existing records to new similar records. A clustering solution definition groups similar records into clusters so you can address them collectively or identify patterns.

## Procedure

1.  Navigate to **Knowledge Demand Insights** &gt; **Solution Definitions**.

2.  In the Solution Definitions \(ML view\) list, search for and select the similarity solution definition for the task type.

    -   For customer service cases, select **Demand Insights: Similar Cases and Knowledge \(ml\_sn\_global\_similar\_cases\_and\_kbs\)**.
    -   For incidents, select **Demand Insights: Similar Incidents and Knowledge \(ml\_sn\_global\_similar\_incidents\_and\_kbs\)**.
    -   For HR cases, select **Demand Insights: Similar HR Cases and Knowledge \(ml\_x\_sn\_hr\_core\_global\_demand\_insights\_similar\_hr\_cases\_and\_knowledge\)**.
    -   For tasks other than customer service cases, incidents, and HR cases, click **New** to create another similarity solution definition.
3.  On the Similarity Definition form, verify the default field values for customer service cases or incidents, or fill in the values for a custom configuration.

    **Note:** If the application scope isn't set to Knowledge Management - Machine Learning, you cannot edit the form and a warning message appears. To make the form editable, click the word **here** at the end of the message.

<table id="table_bxj_sbx_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for your similarity solution.

</td></tr><tr><td>

Word Corpus

</td><td>

Defines which knowledge articles and tasks are selected for knowledge gap analysis.If you don’t have a relevant word corpus, follow the steps in [Create a word corpus](https://www.servicenow.com/docs/access?context=create-word-corpus&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Table

</td><td>

Table that contains the knowledge article records. Set the value to Knowledge \[kb\_knowledge\] unless you use a different table for storing knowledge articles. After you assign a table value, the number of records that match the filter conditions is displayed as a link.

</td></tr><tr><td>

Fields

</td><td>

Fields from the Knowledge table selected for knowledge gap analysis.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions applied on the Knowledge table to filter knowledge article records for knowledge gap analysis.

</td></tr><tr><td>

Test Table

</td><td>

Table that contains the task records that you want to compare with knowledge article records.

</td></tr><tr><td>

Test Fields

</td><td>

Fields from the task table selected for knowledge gap analysis.

</td></tr><tr><td>

Processing Language

</td><td id="processing">

Dominant language of the dataset you're training on the solution definition. By default, English processing is applied to all datasets. For example, if you select Italian, the system processes the data in both English and Italian.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution. These steps might include tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td id="stopwords">

Common terms in the processing language that are excluded from the search, for example, prepositions.When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears. The **Default English Stopwords** list also appears in your selection as well.

</td></tr><tr><td>

Training Frequency

</td><td>

Frequency with which the model for similarity solution definition must be retrained.

</td></tr><tr><td>

Update Frequency

</td><td>

Frequency with which to include new records in the model for the similarity solution definition.

</td></tr></tbody>
</table>4.  Submit and train the solution definition.

    -   For a new solution definition record, click **Submit &amp; Train**.
    -   For an existing solution definition record, click **Update &amp; Retrain**.
5.  Include more useful related articles by reviewing the similarity examples based on the similarity score and updating the similarity score threshold value.

    For more information, see [Review solution similarity examples](https://www.servicenow.com/docs/access?context=review-similarity-examples&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) and [Update your similarity score threshold](https://www.servicenow.com/docs/access?context=update-similarity-threshold&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

6.  In the Solution Definitions \(ML view\) list, search for and select the clustering solution definition for the task type.

    -   For customer service cases, select **Demand Insights: Case Clusters Need Knowledge \(ml\_sn\_global\_cases\_need\_knowledge\_cluster\)**.
    -   For incidents, select **Demand Insights: Incident Clusters Need Knowledge \(ml\_sn\_global\_incidents\_need\_knowledge\_cluster\)**.
    -   For HR cases, select **Demand Insights: HR case clusters need knowledge \(ml\_x\_sn\_hr\_core\_global\_demand\_insights\_hr\_case\_clusters\_need\_knowledge\)**.
    -   For tasks other than customer service cases and incidents, click **New** to create another clustering solution definition.
7.  On the Clustering Definition form, verify the default field values for customer service cases or incidents, or fill in the values for a custom configuration.

    **Note:** If the application scope isn't set to Knowledge Management - Machine Learning, you cannot edit the form and a warning message appears. To make the form editable, click the word **here** at the end of the message.

<table id="table_bbr_chp_tjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for your clustering solution.

</td></tr><tr><td>

Word Corpus

</td><td>

Which tasks are selected for collections.

</td></tr><tr><td>

Table

</td><td>

Table that contains the filtered tasks that require knowledge articles. Set the value to Task knowledge coverage \[kb\_task\_knowledge\_coverage\] unless you use a different table for storing filtered tasks. After you assign a table value, the number of records that match the filter conditions is displayed as a link.

</td></tr><tr><td>

Fields

</td><td>

Fields from the Task knowledge coverage table selected for knowledge gap analysis.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions applied on the Task knowledge coverage table to filter knowledge article records for knowledge gap analysis.

</td></tr><tr><td>

Processing Language

</td><td>

Dominant language of the dataset you're training on the solution definition. By default, English processing is applied to all datasets. For example, if you select Italian, the system processes the data in both English and Italian.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution. These steps might include tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

Common terms in the processing language that are excluded from the search, for example, prepositions.When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears. The **Default English Stopwords** list also appears in your selection as well.

</td></tr><tr><td>

Update Frequency

</td><td>

Frequency with which to include new and updated records in the model for the clustering solution definition.

</td></tr><tr><td>

Training Frequency

</td><td>

Frequency with which the model for clustering solution definition must be retrained.

</td></tr></tbody>
</table>8.  Submit and train the solution definition.

    -   For a new solution definition record, click **Submit &amp; Train**.
    -   For an existing solution definition record, click **Update &amp; Retrain**.

## What to do next

Complete the KB curation configuration form to define the scheduled jobs for demand insights. For more information, see [Configure the mapping of solution definitions with task tables](select-tasks-knowledge-bases.md).

**Related topics**  


[Predictive Intelligence for Knowledge Management](../concept/predictive-intelligence-for-km.md)

[Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Analyze knowledge gaps from a demand insights dashboard and create knowledge gap feedback tasks](analyze-knowledge-gaps-demand-insights.md)


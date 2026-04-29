---
title: Quick start for Topic Recommendations
description: To get recommended topics based on your data, configure analysis reports, run the reports, and then review the results. You can either add new topics to Virtual Agent or link a recommendation to an existing topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Virtual Agent Topic Recommendations, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Quick start for Topic Recommendations

To get recommended topics based on your data, configure analysis reports, run the reports, and then review the results. You can either add new topics to Virtual Agent or link a recommendation to an existing topic.

The Topic Recommendations page appears in your instance at **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Topic Recommendations**.

## Step 1: Configure analysis reports based on ServiceNow data

Until you define analysis reports, the Topic Recommendations page is empty.

![The Topic Recommendations page with no analysis reports defined.](../images/tr-page-new-install.png "Topic Recommendations page with no reports defined")

Each analysis report is based on the following:

-   Data source: The ServiceNow data that you want to analyze. The options are: Incident \[incident\] table, Request \[sc\_request\] table, Live Agent chat transcripts, and Virtual Agent fallback utterances.
-   The field to analyze: A selected field \(with a string data type\) in the data source table to analyze. For example, the **Short description** field.
-   Taxonomy: The business application that includes the data sets. When you install ITSM Virtual Agent Conversations, the Incident and Request data sets are installed by default. As additional data sets for applications become available, the data sets are displayed as a taxonomy on the page after they’re installed on an instance.

You can also add conditions to your analysis reports and configure them to run on a schedule. When new recommendations are available, a notification appears in the Virtual Agent Designer Topics page.

Configure analysis reports for Topic Recommendations in Virtual Agent settings. For details, see [Configure analysis reports for Topic Recommendations](../task/define-tr-settings.md).

## Step 2: Run an analysis report

Run all configured analysis reports together or selectively run one at a time from the Topic Recommendations page.

During analysis, the Topic Recommendations app does the following:

-   Uses Intent Discovery to review your data source, comparing your data source against the related taxonomy for your business application. Intent Discovery matches the data field specified in your data set to intents in the taxonomy.
-   Maps the matched intents to pre-built topics in Virtual Agent. If intents don’t have associated pre-built topics, the app recommends them as new topics that you can build because they were requested frequently enough by your users.
-   Displays the analysis results as topic cards in the Topic Recommendations page.

For more information, see [Run a Topic Recommendation analysis](../task/run-tr-analysis.md).

## Step 3: Review report results and add or link topics and intents

Results are sorted into the following groups:

-   Topics that Virtual Agent can handle: Recommendations in this group can be addressed with a pre-built topic.

    When you add this type of recommendation to Virtual Agent, the matched pre-built topic is duplicated in your instance. You can then modify, test, and publish the added topic using Virtual Agent Designer.

-   User intents that need topic flows: Recommendations in this group match a ServiceNow NLU intent.

    When you add this type of recommendation to Virtual Agent, an empty topic is created and mapped to the matched intent in the model that you specify. You can then open the topic in Virtual Agent Designer and create a flow for the new topic.


The results are displayed in descending order of matches to your data source. The top 20 intent matches are displayed. If there are more than 20 intents, you can view them in NLU Workbench.

For more information about adding a recommendation to Virtual Agent, see [Add recommended topics and intents to Virtual Agent](../task/add-tr-results-va.md). You can also [link a recommendation to an existing topic](../task/link-tr-existing-va-topic.md).

![Topic Recommendations analyzes your data and combines it with an understanding of the product area to suggest pre-built topics and intents or new content for Virtual Agent.](../images/tr-flow-diagram.png "Mapping recommendations to Virtual Agent topics")


---
title: Run a Topic Recommendation analysis
description: Generate a report that analyzes a given data source and identifies the appropriate Virtual Agent pre-built topics that you can implement. For intents that do not have matching pre-built topics, the report identifies the user intents \(topics\) that you can create.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-06"
reading_time_minutes: 3
keywords: [Vitual agent, Topic Recommendation, analysis]
breadcrumb: [Using Virtual Agent Topic Recommendations, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Run a Topic Recommendation analysis

Generate a report that analyzes a given data source and identifies the appropriate Virtual Agent pre-built topics that you can implement. For intents that do not have matching pre-built topics, the report identifies the user intents \(topics\) that you can create.

## Before you begin

Verify that the appropriate Virtual Agent conversation plugins are activated so that the Topic Recommendations app can identify the appropriate pre-built topics.

You can use the **Check for updates** link on the Topic Recommendations page to check which plugins are installed.

Make sure you [configure analysis reports](define-tr-settings.md) first.

Role required: virtual\_agent\_admin or admin

## About this task

The analysis process takes about 15 minutes or less to return recommendation results. In the Xanadu release, Topic Recommendations requires a minimum of 10,000 records in the data source and will only process a maximum of 300,000 records. Use filters in the settings page to reduce the number of records in the data source, if needed.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Topic Recommendations**.

2.  In the Topic Recommendations page, go to the data source to be analyzed and trigger the analysis.

    -   If the view is set to **All**, do the following:
        1.  Select **Get new recommendations**.
        2.  In the dialog box, select the sources you want to get reports for.

            If a check box is unavailable, a report may already be running, or the amount of data to analyze might be outside of the minimum or maximum allowed.

        3.  Select **Get new recommendations**.
    -   If the view is set to **By Source**, do the following:
        1.  Select **Run analysis** or **Refresh** in the source status bar.
        2.  Modify any settings in the dialog box, and then select **Get recommendations**.
    A message indicates that the topic-finding process has started and the approximate time for recommendation results. The page or status bar displays `Analysis in progress`. You can review other items while the analysis runs.

    **Note:** Changing the settings here affects only this analysis. The default settings for the recommendation are preserved. To change the default settings, see [Configure analysis reports for Topic Recommendations](define-tr-settings.md).

3.  When the report completes, review the analysis results for the data set.

    The results display as cards in two sections: **Topics that VA can handle** for pre-built topics and **User intents that need topic flows** for intents and corresponding topics that can be created.

    **Tip:** To view details about a pre-built topic or user intent, select the card, and then select the Info icon ![Blue info icon](../images/icon-info-blue.png) to open an overlay card. For more information, see [Topic Recommendations cards](../reference/topic-recommendations-cards.md).


## What to do next

You can [add a Topic Recommendation as a new topic](add-tr-results-va.md) or [link it to an existing topic](link-tr-existing-va-topic.md). You can also [hide a recommendation](hide-tr-recommendation.md) from the list in aggregate view.


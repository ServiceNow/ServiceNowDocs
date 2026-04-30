---
title: Set up text analytics
description: Select the text fields to analyze and which indicators to analyze.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Text analytics and text widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Set up text analytics

Select the text fields to analyze and which indicators to analyze.

## Before you begin

Text analytics relies on specific steps in the [data collection jobs](../concept/performance-analytics-glossary.md#). The **Collect** parameter in the relevant jobs must be set to collect text analytics. A job is relevant if it collects data for the same indicators that are subject to text analysis. See [Create or schedule a data collection job](t_CreatASchedDataCollJob.md).

**Note:**

Regarding domain separation: To collect text analytics for specific domains, set up text analytics for each of those domains. On the collection job for each domain, specify a **Run as** user with access to that domain. Do not specify a domain configuration for the collection job. For more information, see [Approaches to Performance Analytics with domain separation](../concept/pa-domain-configurations.md). You are using a hybrid approach.

Role required: pa\_power\_user or pa\_admin

## Procedure

1.  Navigate to **All** &gt; **Text Analytics** &gt; **Setup**.

    -   To create a new text analytics configuration, select **New**.
    -   To edit an existing text analytics configuration, select the information icon in that row and select **Open record**. Select the indicator source name to open the record for that indicator source, not the text analytics configuration.
2.  Select the **Indicator source** whose input text you want to analyze.

3.  Unlock **Fields to analyze** and select the fields whose input text you want to analyze.

    You must select at least one field. Usually you want to include the **Short description** field.

    You cannot select the following fields:

    -   Dot-walked fields
    -   Translated Text fields
    -   Any other field with a type other than String
4.  Select **Use system stop words** to include the Zing stop words.

    Selected by default. The Zing global stop words apply to the indicator source. If you do not use the Zing stop words, you must select all stop words yourself.

5.  Save the text index configuration.

    The **Indicators** related list appears at the bottom of the form.

6.  In the **Indicators** list, click **Edit** and select the indicators to analyze.

7.  Run a relevant historical data collection job to collect initial data.

    You may be able to run a job from this form, or you may have to run a historical data collection job. See the next topic for details.


**Related topics**  


[Zing removes stop words from queries](https://www.servicenow.com/docs/access?context=stop-words-removed-from-queries&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)


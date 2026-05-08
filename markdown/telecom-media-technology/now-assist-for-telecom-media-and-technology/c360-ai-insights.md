---
title: Generate Telecom customer 360 insights
description: Generate customer health insights and recent customer issue insights for a customer or consumer account.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Generate Telecom customer 360 insights

Generate customer health insights and recent customer issue insights for a customer or consumer account.

**Note:** This skill is available only if Telecommunications Customer 360 is installed and requires the `sn_telecom_c360.admin` role.

The Generate Telecom Customer 360 Insights skill is enabled by default and automatically generates AI-powered insights for a customer or consumer account when you navigate to the [Telecommunications Customer 360 home page](../../tmt-telecom-customer-360/concept/c360-home-page.md). This skill triggers the following two sub-skills in parallel:

-   Telecom C360 customer health insights: This skill analyzes customer sentiment from recently closed cases and service problems to assess relationship health. It provides sentiment classification, trend analysis, and lists analyzed cases, with an extensible data provider that allows customers to incorporate custom sentiment data sources.
-   Telecom C360 top customer issue insights: This skill analyzes recent open cases, service problem cases, and customer interactions to provide insights on top customer issues. It helps agents quickly understand a customer's current issues and prioritize resolution efforts. Works at both consumer and account levels.

The skill uses the following data sources to generate insights:

-   Cases
-   Service problem cases
-   Interactions
-   Sentiment data

The insights are automatically displayed when a customer or consumer account is opened. See [Insights card](../../tmt-telecom-customer-360/concept/c360-insights-card.md) for details.

## Customize data sources

The skill uses the CustomerInsightsDataProvider scripted extension point to retrieve data. Two implementations are available with the base system:

-   CustomerHealthDataProvider: Retrieves cases, interactions, and sentiment data to generate customer health insights.
-   RecentCustomerIssuesData Provider: Retrieves cases and service problem cases to generate recent customer issue insights.

You can modify the existing implementation to retrieve data from additional sources or create your custom implementation. For more details on configuring extension points, see Using extension points to extend application functionality.

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](now-assist-spm-using.md)


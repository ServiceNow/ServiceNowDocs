---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection monitor engagement health agentic workflow
description: Use the Monitor engagement health agentic workflow to monitor the health score of engagements and their associated metric data trends, and generate risk signals when a decline is detected.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Success Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection monitor engagement health agentic workflow

Use the Monitor engagement health agentic workflow to monitor the health score of engagements and their associated metric data trends, and generate risk signals when a decline is detected.

## Monitor engagement health agentic workflow overview

Customer success managers can monitor the health score of up to 10 active engagements and summarize the health trend for the past 6 weeks. Each metric used to calculate the health score is monitored, and if a declining pattern is detected, a risk signal or a risk occurrence \(for an existing risk signal\) is generated. A summary indicating the number of risk signals created and the health score range is generated. The Monitor engagement health agentic workflow is triggered weekly based on a predefined schedule and the results are displayed in the Now Assist panel.

You can view the risk signals and occurrences that have been created by navigating to the Risk signals page. For risks created using the agentic workflow, the following field values are displayed:

-   Category: Health declined
-   Creation method: AI generated

**Note:**

-   To run the agentic workflow as a scheduled job, you must activate the Monitor engagement health flow. See Activate a flow for details.
-   The agentic workflow monitors only the engagements for which **AI Health Monitor** flag has been enabled. Each customer success manager can enable a maximum of 10 engagements. For instructions on enabling this flag, see Create an engagement.
-   By default, the health score of each individual metric is monitored. If you want to monitor only the overall health score across all engagements, update the **sn\_cust\_succ\_ai\_agent\_enable\_health\_monitor\_metrics** system property by following these steps:
    -   Navigate to **All** and enter **sys\_properties.LIST** in the search field.
    -   Select the **sn\_cust\_succ\_ai\_agent\_enable\_health\_monitor\_metrics** property.
    -   Set the Value field to **false**. When this property is inactive, the agentic workflow will monitor the overall health score instead of the individual metrics.
-   For any new or existing health definitions, you must specify the **Context** for the **Data source** to indicate how the color banding range will be applied. Based on the **Context**, you can define different color banding ranges that can be used for the health score. For example, you can configure different values for the same **Data source** as follows:

    -   **Data source 1**
        -   Data source: Daily collection of NPS
        -   Context: Health Metric Configuration: Daily collection of NPS \(Global\)
        -   Min: 80
        -   Max: 100
        -   Color: Green
        -   Category: Good
    -   **Data source 2**
        -   Data source: Daily collection of NPS
        -   Context: Daily collection of NPS for \(Customer X\)
        -   Min: 0
        -   Max: 60
        -   Color: Red
        -   Category: Poor
    For more details on configuring the color banding table, see Set up the color banding table.


## AI agents used in the Monitor engagement health agentic workflow

The Monitor engagement health agentic workflow uses specific AI agents to monitor the engagements, analyze the health trend, and generate a health score.

|AI agent|AI agent role|
|--------|-------------|
|Success trend analyst AI agent|Collects and analyzes metric data, processes large data sets, identifies patterns and anomalies. Provides clear actionable insights enabling AI agents to make informed decisions and take appropriate actions.|
|Success health monitor AI agent|Retrieves data for all active engagements, identifies trends, and creates a risk signal if a declining pattern is detected.|


---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) Monitor engagement health agentic workflow
description: Use the Monitor engagement health agentic workflow to monitor the health score of engagements and their associated metric data trends, and generate risk signals when a decline is detected.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Customer Success Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) Monitor engagement health agentic workflow

Use the Monitor engagement health agentic workflow to monitor the health score of engagements and their associated metric data trends, and generate risk signals when a decline is detected.

**Important:** Before you run this agentic workflow, you must activate the [Analyze metric data trend](../task/now-assist-tmt-analyze-metric-trend.md) skill to collect the metric data that is to be evaluated.

## Monitor engagement health agentic workflow overview

Customer success managers can monitor the health score of up to 10 active engagements and summarize the health trend for the past 6 weeks. Each metric used to calculate the health score is monitored, and if a declining pattern is detected, a risk signal or a risk occurrence \(for an existing risk signal\) is generated. A summary indicating the number of risk signals created and the health score range is generated. The Monitor engagement health agentic workflow is triggered weekly based on a predefined schedule and the results are displayed in the [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

You can view the risk signals and occurrences that have been created by navigating to the [Risk signals](https://www.servicenow.com/docs/access?context=account-lifecycle-create-risk-signal&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US) page. For risks created using the agentic workflow, the following field values are displayed:

-   Category: Health declined
-   Creation method: AI generated

## Role masking

Required role: sn\_acct\_lc.customer\_success\_agent

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Configure the monitor engagement health agentic workflow

-   To run the agentic workflow as a scheduled job, you must activate the Monitor engagement health flow. See [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for details.
-   The agentic workflow monitors only the engagements for which **AI Health Monitor** flag has been enabled. Each customer success manager can enable a maximum of 10 engagements. For instructions on enabling this flag, see [Create an engagement](https://www.servicenow.com/docs/access?context=account-lifecycle-create-engage&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US).
-   By default, the health score of each individual metric is monitored. If you want to monitor only the overall health score across all engagements, you need to update the **sn\_cust\_succ\_ai\_agent\_enable\_health\_monitor\_metrics** system property by following these steps:
    -   Navigate to **All** and enter **sys\_properties.LIST** in the search field.
    -   Select the **sn\_cust\_succ\_ai\_agent\_enable\_health\_monitor\_metrics** property.
    -   Set the Value field to **false**. When this property is disabled, the agentic workflow will monitor the overall health score instead of the individual metrics.
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
    For more details on configuring the color banding table, see [Setup the color banding table](https://www.servicenow.com/docs/access?context=account-lifecycle-setup-color-banding&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US).


## AI agents used in the Monitor engagement health agentic workflow

The Monitor engagement health agentic workflow uses specific AI agents to monitor the engagements, analyze the health trend, and generate a health score.

|AI agent|AI agent role|
|--------|-------------|
|Success health monitor AI agent|Retrieves data for all active engagements, identifies trends, and creates a risk signal if a declining pattern is detected.|

**Parent Topic:**[Customer Success Management agentic workflows](now-assist-tmt-health-risk.md)


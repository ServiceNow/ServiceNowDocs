---
title: Collect and manage a matrix of breakdowns
description: Collect a matrix of the two-breakdown combinations for an indicator. Exclude unnecessary or meaningless combinations of breakdowns from being collected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/configure-breakdown-matrix.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2023-02-02"
reading_time_minutes: 3
breadcrumb: [Automated indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Collect and manage a matrix of breakdowns

Collect a matrix of the two-breakdown combinations for an indicator. Exclude unnecessary or meaningless combinations of breakdowns from being collected.

## Before you begin

Breakdowns must be assigned to the indicator. See [Assign and map breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-breakdown-mapping.md).

**Important:** If you enable Data snapshots for an indicator, you are not limited to two-breakdown combinations and the indicator does not have a breakdown matrix. For more information, see [Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md).

Role required: pa\_data\_collector, pa\_power\_user, pa\_admin, or admin

## About this task

Sometimes, not all breakdown combinations give useful information. For example, the combination \[Country, Region\] gives the same scores as the breakdown Country. You can prevent the instance from collecting data for these invalid combinations with breakdown matrix exclusions. These exclusions are not shown in the Analytics Hub, in KPI Details, or in the scoresheet. You also cannot select excluded breakdown combinations when you create widgets or data visualizations.

To prevent performance issues, the property **com.snc.pa.dc.max\_breakdown\_elements\_level2\_limit** limits the number of elements from breakdown connections that are included in data collection. If you exceed this limit, some of the combinations in your matrix are grayed out. By excluding some breakdown combinations, you can help to avoid exceeding this limit. For more information, see [Performance Analytics properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/pa-properties.md).

**Note:**

-   The scores for individual breakdowns are still collected when the combination of those breakdowns has been excluded.
-   Scores that were collected in previous jobs for breakdown combinations are not deleted when those combinations are later excluded. New scores for those combinations are not collected.
-   These instructions are for using the graphical tool to manage breakdown matrix exclusions. However, you can also manage them in the **Breakdown matrix exclusion** tab of the indicator form.

## Procedure

1.  Navigate to **Automated Indicators**.

2.  Select the automated indicator for which you want to configure the breakdown matrix.

3.  Under **Indicator properties**, select the **Collect breakdown matrix** tab.

4.  Select the **Collect breakdown matrix** check box.

5.  Click **Manage Breakdowns**.

6.  Click **Configure Breakdown Matrix**.

    The matrix shows the number of element combinations for each breakdown pair, calculated by multiplying the number of elements for the two breakdowns. Breakdown pairs with a higher number of combinations are shown in a darker color, to help you spot possible performance bottlenecks at a glance. By default, all combinations are included in data collection. You can select combinations to exclude from data collection.

7.  In the **Breakdown Matrix** pop-up, select breakdown combinations to exclude from Analytics Hub and dashboard widgets.

    Included combinations are shaded in the breakdown matrix. Excluded combinations are white. If the number of breakdown combinations exceeds the value of **com.snc.pa.dc.max\_breakdown\_elements\_level2\_limit**, some combinations are grayed out.\[Omitted image "exclude-breakdown-combination.png"\] Alt text: Breakdown matrix with one combination excluded and another with the "Exclude breakdown combination" tool tip.

8.  On the indicator form, open the **Breakdown matrix exclusion** tab and see which breakdown combinations have been excluded.

    You can manage which breakdown combinations to exclude in this tab instead of using the graphical tool.


**Parent Topic:**[Automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/automated-indicators.md)

**Previous topic:**[Assign and map breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-breakdown-mapping.md)

**Next topic:**[Add a collection job to an indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_EditAJobForTheIndicator.md)


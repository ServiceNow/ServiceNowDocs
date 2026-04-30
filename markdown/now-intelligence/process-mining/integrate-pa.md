---
title: Integration with indicator data sources \(PA\)
description: Using Process Mining with Platform Analytics indicator data sources enables you to perform data extraction from an indicator and analyze processes associated with KPIs such as Time to resolve.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Process Mining, Activating Process Mining, Process Mining, Platform Analytics]
---

# Integration with indicator data sources \(PA\)

Using Process Mining with Platform Analytics indicator data sources enables you to perform data extraction from an indicator and analyze processes associated with KPIs such as Time to resolve.

The Process Mining plugin \(com.sn\_po\) provides an integration between Process Mining and [indicator](../../../use/performance-analytics/concept/performance-analytics-glossary.md#) data sources. Integration occurs automatically when you enable the Process Mining plugin. Afterwards, you can open the Process Mining workbench from KPI Details for an indicator.

The Process Mining plugin provides template configurations for [indicator sources](../../../use/performance-analytics/concept/performance-analytics-glossary.md#) that use the following tables:

-   Customer service case \[sn\_customerservice\_case\]
-   Incident \[incident\]
-   Problem \[problem\]
-   Change \[change\]
-   Requested Item \[sc\_req\_item\]

To support indicators based on other tables, create templates for those tables. For more information, see [Set up a table configuration](../task/po-table-configuration.md).

**Note:**

-   Process Mining supports only [automated indicators](../../../use/performance-analytics/concept/performance-analytics-glossary.md#). From KPI Details for a [formula indicator](../../../use/performance-analytics/concept/performance-analytics-glossary.md#), you can still open Process Mining, but you must choose one of the contributing automated indicators in the formula.
-   Process Mining does not support indicator sources that are based on [database views](../../../use/performance-analytics/concept/performance-analytics-glossary.md#).

## Roles

Integrating with indicators does not add any roles to Process Mining roles. To enable the integration features, you must add the PA viewer role \(pa\_viewer\) to the Process Mining users who need this capability. Similarly, add the appropriate Process Mining role to any users who manage indicators and need Process Mining capability.

## Launch and use Process Mining

Integrating with indicators adds the **Run process analysis** option to the KPI Details menu. Users can:

-   Open Process Mining for a specific indicator from KPI Details.

    ![Run process analysis from KPI Details.](../../../use/par-for-workspace/image/kpi-details-process-analysis.png)

-   Schedule data extraction from a Performance Analytics indicator.

When you initiate data extraction for an indicator, you see the extraction progress. Once it completes, you can view the project from the Process Mining Analyst Workbench. If you initiate an extraction at a later time on the same indicator settings, but on a different date, you will see a new PA project created in the **Process Mining** &gt; **Projects** &gt; **PA Projects** list.

-   **[Example of an indicator using Process Mining](performance-analytics-using-process-mining.md)**  
Understand how you can extract data from an indicator that is based on incident, problem, change, customer service case, or request process data.

**Parent Topic:**[Integrating Process Mining](integrating-process-mining.md)

**Related topics**  


[Example of an indicator using Process Mining](performance-analytics-using-process-mining.md)

[Exploring indicators with KPI Details](../../../use/par-for-workspace/reference/kpi-details-components.md)


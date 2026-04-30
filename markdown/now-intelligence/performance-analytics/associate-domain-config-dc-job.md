---
title: Associate a domain configuration with a data collection job
description: To collect Performance Analytics indicator scores from the domains specified in a domain configuration, associate that domain configuration with a collection job.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Grouping domains in Performance Analytics domain configurations, Domain separation and Performance Analytics, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Associate a domain configuration with a data collection job

To collect Performance Analytics indicator scores from the domains specified in a domain configuration, associate that domain configuration with a collection job.

## Before you begin

Role required: pa\_data\_collector or admin

The Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) must be activated.

## About this task

**Important:** Regardless of whether a domain configuration is used, the **Run as** user always determines the domain context of where the [data collection job](../concept/performance-analytics-glossary.md#) runs.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Jobs**.

2.  Select a data collection job.

3.  In the **Domain Configurations** related list, click **Edit**.

4.  Select the domain configurations you want to associate with this job.

    A separate data collection job runs for each domain included in the configuration.

5.  Click **Save**.

6.  Modify the **Order** of the domain configuration.

    If multiple domain configurations are associated with a collection job, any overlap in the included domains may cause scores to be collected incorrectly. Only the scores collected for the domain configuration with the highest **Order** value are preserved for the overlapping domains.

    **Tip:** When using multiple domain configurations with a single job, ensure each domain configuration specifies a unique set of domains.


**Parent Topic:**[Grouping domains in Performance Analytics domain configurations](../concept/pa-domain-separation-msp.md)


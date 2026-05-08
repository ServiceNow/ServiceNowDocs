---
title: Configuring scheduled jobs for SGC Central
description: You can configure scheduled jobs to automate data collection for tracking integration performance, errors, and processing status of Service Graph Connectors within the SGC Central application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring SGC Central, SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring scheduled jobs for SGC Central

You can configure scheduled jobs to automate data collection for tracking integration performance, errors, and processing status of Service Graph Connectors within the SGC Central application.

Scheduled jobs ensure that integration performance data is consistently gathered and available for reporting and analysis within SGC Central. For more information on configuring a scheduled job, see Scheduled jobs.

## Types of scheduled jobs in SGC Central

SGC Central provides different scheduled jobs to meet various data collection needs:

-   **SGC central collection**

    Collects score and metric data displayed on the SGC Central dashboard for the latest integration activity. This job runs daily automatically or as configured.

    **Note:** As a user with the admin role, you must run this scheduled job immediately after installing SGC Central and update its schedule based on your preferences to reflect the latest integration activity.

-   **SGC central collection onDemand with lookback**

    Enables on-demand collection of historical integration data for analysis. The job collects scores for a lookback period of 30 days, meaning it gathers data from 30 days ago to today \(0 days ago\), enabling historical data collection for performance analysis.

    **Note:** As a user with the admin role, you can run this scheduled job on demand, rather than on a daily schedule.



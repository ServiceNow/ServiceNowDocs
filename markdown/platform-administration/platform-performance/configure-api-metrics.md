---
title: Configure API metrics
description: Configure the API metrics feature in Application Insights to enable instance administrators to proactively monitor instance performance.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Monitoring API performance, Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Configure API metrics

Configure the API metrics feature in Application Insights to enable instance administrators to proactively monitor instance performance.

## Before you begin

The **API metrics** tab shows up under Application Insights if the following conditions are met.

-   The API metric com.glide.rest.analytics.metricbase plugin is installed.

    **Note:** By default, the API metric plugin is installed along with the Application Insights version upgrade.

-   Application Insights is installed on your instance.

Role required: admin

## Procedure

1.  Navigate to Application Manager and search for com.glide.rest.analytics.metricbase.

2.  Select your target instance from the menu where Application Insights is installed and where the API metrics plugin should be activated.

3.  Enter the following details.

    -   Plugin ID: com.glide.rest.analytics.metricbase
    -   Name: API Metrics

**Parent Topic:**[Monitoring API performance](../concept/api-metrics.md)


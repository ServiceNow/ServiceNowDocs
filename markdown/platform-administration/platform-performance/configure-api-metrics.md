---
title: Configure API metrics
description: Configure the API metrics feature in Application Insights to enable instance administrators to proactively monitor instance performance.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Monitoring API performance, Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Configure API metrics

Configure the API metrics feature in Application Insights to enable instance administrators to proactively monitor instance performance.

## Before you begin

The **API metrics** tab shows up under Application Insights if the following conditions are met.

-   The API metric com.glide.rest.analytics.metricbase plugin is installed.

    **Note:** By default, the API metric plugin is installed along with the Application Insights version upgrade.

-   Application Insights is installed on your instance.

Role required: admin

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to Application Manager and search for com.glide.rest.analytics.metricbase.

2.  Select your target instance from the menu where Application Insights is installed and where the API metrics plugin should be activated.

3.  Enter the following details.

    -   Plugin ID: com.glide.rest.analytics.metricbase
    -   Name: API Metrics

**Parent Topic:**[Monitoring API performance](../concept/api-metrics.md)


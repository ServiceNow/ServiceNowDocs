---
title: Configuring User Experience Analytics
description: An admin can configure which ServiceNow applications to track in the Usage Insights application as well as user tracking consent policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/usage-insights/configuring-user-exp-analytics.html
release: yokohama
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics, Platform Analytics]
---

# Configuring User Experience Analytics

An admin can configure which ServiceNow applications to track in the Usage Insights application as well as user tracking consent policies.

## Configuration overview

For Next Experience and Core UI, application tracking is enabled by default. On Service Portal, Usage Insights, requires enabling.

## Usage Insights plugin

The Usage Insights plugin \(com.glide.appsee\) is activated by default in the ServiceNow AI Platform in new and upgraded instances. The plugin is responsible for:

-   Checking hourly for new applications to register with the ServiceNow Usage Insights server
-   Providing access to Usage Insights functionality.

    **Note:** Usage Insights is not supported for on-prem instances.


-   **[Enable Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/config-analytics-settings.md)**  
You can enable or disable Usage Insights for specific applications on the Usage Insights settings table.
-   **[User privacy, tracking, and user consent management in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/user-exp-analytics-track-options.md)**  
Usage Insights relies on tracking user activity to measure the adoption, retention, and usage of KPIs \(key performance indicators\) to help you make better product and implementation decisions.

**Parent Topic:**[User Experience Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/user-exp-analytics-landing.md)


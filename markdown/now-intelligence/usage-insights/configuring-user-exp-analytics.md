---
title: Configuring Usage Insights
description: An admin can configure which ServiceNow applications to track in the Usage Insights application as well as user tracking consent policies.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Usage Insights, Platform Analytics]
---

# Configuring Usage Insights

An admin can configure which ServiceNow applications to track in the Usage Insights application as well as user tracking consent policies.

## Configuration overview

Tracking is enabled by default for Next Experience, Mobile, and Core UI applications. On Service Portal, Usage Insights may require enabling.

## Usage Insights plugin

The Usage Insights plugin \(com.glide.appsee\) is activated by default in the ServiceNow AI Platform in new and upgraded instances. The plugin is responsible for:

-   Checking hourly for new applications to register with the ServiceNow Usage Insights server
-   Providing access to Usage Insights functionality.

    **Note:** Usage Insights is not supported for on-prem instances.


-   **[Enable Usage Insights](../../task/enable-user-experience-analytics.md)**  
You can enable or turn off Usage Insights for all applications in Usage Insights Properties.
-   **[User privacy, tracking, and user consent management in Usage Insights](../../concept/user-exp-analytics-track-options.md)**  
Usage Insights relies on tracking user activity to measure the adoption, retention, and usage of KPIs to help you make better product and implementation decisions.
-   **[Add user properties as filters to Usage Insights](../../task/uxa-add-filters-uxa-pages.md)**  
In addition to the default filters on the pages of the Usage Insights application, you can add filters based on user properties. This allows you to effectively segment your Usage Insights data to develop a deeper understanding of your users and their usage patterns. User properties-based filters are supported as global filters for all pages and objects in the Usage Insights application.

**Parent Topic:**[Usage Insights](../landing-page/user-exp-analytics-landing.md)


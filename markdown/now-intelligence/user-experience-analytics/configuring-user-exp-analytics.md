---
title: Configuring User Experience Analytics
description: An admin can configure which ServiceNow applications to track in the User Experience Analytics application as well as user tracking consent policies.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics, Platform Analytics]
---

# Configuring User Experience Analytics

An admin can configure which ServiceNow applications to track in the User Experience Analytics application as well as user tracking consent policies.

## Configuration overview

Tracking is enabled by default for Next Experience, Mobile, and Core UI applications. On Service Portal, User Experience Analytics may require enabling.

## User Experience Analytics plugin

The User Experience Analytics plugin \(com.glide.appsee\) is activated by default in the ServiceNow AI Platform in new and upgraded instances. The plugin is responsible for:

-   Checking hourly for new applications to register with the ServiceNow User Experience Analytics server
-   Providing access to User Experience Analytics functionality.

    **Note:** User Experience Analytics is not supported for on-prem instances.


-   **[Enable User Experience Analytics](../../task/enable-user-experience-analytics.md#)**  
You can enable or turn off User Experience Analytics for all applications in User Experience Analytics Properties.
-   **[User privacy, tracking, and user consent management in User Experience Analytics](../../concept/user-exp-analytics-track-options.md)**  
User Experience Analytics relies on tracking user activity to measure the adoption, retention, and usage of KPIs \(key performance indicators\) to help you make better product and implementation decisions.
-   **[Add user properties as filters to User Experience Analytics](../../task/uxa-add-filters-uxa-pages.md)**  
In addition to the default filters on the pages of the User Experience Analytics application, you can add filters based on user properties. This allows you to effectively segment your User Experience Analytics data to develop a deeper understanding of your users and their usage patterns. User properties-based filters are supported as global filters for all pages and objects in the User Experience Analytics application.

**Parent Topic:**[User Experience Analytics](../landing-page/user-exp-analytics-landing.md)


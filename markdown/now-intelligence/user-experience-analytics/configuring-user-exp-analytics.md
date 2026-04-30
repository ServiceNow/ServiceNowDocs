---
title: Configuring User Experience Analytics
description: An admin can configure which ServiceNow applications to track in the User Experience Analytics application as well as user tracking consent policies.
locale: en-US
release: yokohama
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics, Platform Analytics]
---

# Configuring User Experience Analytics

An admin can configure which ServiceNow applications to track in the User Experience Analytics application as well as user tracking consent policies.

## Configuration overview

For Next Experience and Core UI, application tracking is enabled by default. On Service Portal, User Experience Analytics, requires enabling.

## User Experience Analytics plugin

The User Experience Analytics plugin \(com.glide.appsee\) is activated by default in the ServiceNow AI Platform in new and upgraded instances. The plugin is responsible for:

-   Checking hourly for new applications to register with the ServiceNow User Experience Analytics server
-   Providing access to User Experience Analytics functionality.

    **Note:** User Experience Analytics is not supported for on-prem instances.


-   **[Enable User Experience Analytics](../../task/config-analytics-settings.md)**  
You can enable or disable User Experience Analytics for specific applications on the User Experience Analytics settings table.
-   **[User privacy, tracking, and user consent management in User Experience Analytics](../../concept/user-exp-analytics-track-options.md)**  
User Experience Analytics relies on tracking user activity to measure the adoption, retention, and usage of KPIs \(key performance indicators\) to help you make better product and implementation decisions.
-   **[Domain separation in User Experience Analytics](user-experience-analytics-domain-separation.md)**  
Domain separation is not supported for the User Experience Analytics application.

**Parent Topic:**[User Experience Analytics](../landing-page/user-exp-analytics-landing.md)


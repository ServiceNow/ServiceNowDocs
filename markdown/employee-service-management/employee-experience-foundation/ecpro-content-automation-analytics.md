---
title: Content Analytics
description: Monitor and measure the impact of the content you provide through the Employee Center and in campaigns using Content Analytics.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setup continuous improvement, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Content Analytics

Monitor and measure the impact of the content you provide through the Employee Center and in campaigns using Content Analytics.

Content Analytics collects data and generates visualizations on employee engagement with content in the Employee Center. Content Analytics is powered by the Platform Analytics framework.

**Note:** Google Analytics is no longer supported as Google has stopped offering the integration.

## Content Analytics dashboards

Dashboards display data visualizations in widgets. Each widget displays data for specific parameters, such as user interactions with content. Content Analytics includes the following dashboards:

|Dashboard|Description of data visualizations|
|---------|----------------------------------|
|[Content Analytics](content-analytics-dashboards.md)|Portal engagement metrics, including unique users, average time per page, and bounce rate.|
|[Content Analytics - Basics](content-analytics-dashboards.md)|Portal page visits and views, including visits per day and most-frequently viewed pages.|
|[Campaign Analytics](ecpro-content-automation-content-pack.md)|Campaign engagement metrics, to-dos, and impact, filtered by campaign or campaign success goal.|
|[Campaign Overview](ecpro-content-automation-content-pack.md)|Campaign performance metrics by campaign, including tasks closed and user actions.|
|[Content Library Overview dashboard](content-library-overview-dashboard.md)|Performance metrics for content published to the portal or Now mobile app.|
|[Content engagement](ec-pro-content-engagement-dashboard.md)|Metrics on user engagement, such as content views, reaction icon clicks, comments, and replies to comments.|

## Setting up Content Analytics

1.  [Activate Content Analytics](../task/activate-content-analytics-plugin.md)
2.  Establish the tracking profile, by performing one of the following steps:

    -   Activate one of the out-of-the-box tracking profiles and set it as the default tracking profile: [Activate a tracking profile](../task/activate-tracking-profile.md)
    -   Create a custom tracking profile: [Create a Content Analytics tracking profile](../task/ecpro-content-analytics-setup.md)
    For more information on tracking profiles, see the section below.

3.  To track analytics for a custom widget or page, you must add the tracking profile to the header: [Set up Content Analytics tracking](../task/ecpro-content-analytics-tracking-setup.md)

    **Important:** A new **Enable Tracking** field has been introduced to content notifications, designed specifically for email content. Existing notification records will have this field disabled by default, in line with prior system settings and by default, existing email content will have tracking turned off. However, for new email notification contents, the **Enable Tracking**option will be available for your selection and will be automatically enabled on new record creation. This feature provides greater flexibility, allowing you to determine whether tracking should be applied to specific email content record.


## Tracking profiles

Tracking profiles define a bucket where you want to capture analytics. It can correspond to a portal, campaign, application, or any context you like.

Two tracking profiles are included out-of-the-box: Content Experiences and Content Publishing. You can use either one to collect data on content that is displayed with an out-of-the-box widget. If your portal is publishing content to custom widgets, you must update an out-of-the-box tracking profile to collect data for those widgets or create a new tracking profile.

## Data collection and storage

Content Analytics stores collected data in tables, which are organized by data type.

**Note:** If a dashboard does not display visualizations, check that the data is being collected by opening a table. Enter the table name in the navigation bar, appended by `.list`.

For a list of Content Analytics tables, see [Components installed with Content Analytics](../reference/ecpro-installed-content-analytics-1.md).

This is an overview of the process by which Content Analytics collects and moves data:

1.  The users performs an action, such as opening a page or clicking a link.
2.  Content Analytics collects that data point and stores in the browser memory.
3.  After a user navigates to other content or after five minutes, the data moves to the server in memory.
4.  The data moves to the content analytics tables.
    -   Tracked Event \[sn\_cda\_tracked\_evt\_agg\]
    -   Tracked Page \[sn\_cda\_tracked\_page\_agg\]
    -   Tracked Visit \[sn\_cda\_tracked\_visit\_agg\]
5.  The tracking profiles trigger runs to transfer data to the shared analytics tables.
    -   Event Statistic \[sn\_cda\_event\_stat\]
    -   Page Statistic \[sn\_cda\_page\_stat\]
    -   Analytics Visit Statistic \[sn\_cda\_analytics\_visit\_stat\]


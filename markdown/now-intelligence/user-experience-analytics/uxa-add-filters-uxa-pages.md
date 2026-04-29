---
title: Add user properties as filters to Usage Insights
description: In addition to the default filters on the pages of the Usage Insights application, you can add filters based on user properties. This allows you to effectively segment your Usage Insights data to develop a deeper understanding of your users and their usage patterns. User properties-based filters are supported as global filters for all pages and objects in the Usage Insights application.
locale: en-US
release: australia
product: User Experience Analytics
classification: user-experience-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Usage Insights, Usage Insights, Platform Analytics]
---

# Add user properties as filters to Usage Insights

In addition to the default filters on the pages of the Usage Insights application, you can add filters based on user properties. This allows you to effectively segment your Usage Insights data to develop a deeper understanding of your users and their usage patterns. User properties-based filters are supported as global filters for all pages and objects in the Usage Insights application.

## Before you begin

Role required: admin or analytics\_admin.

**Note:** You can add up to 20 fields including the Department and Role fields which are available by default.

## Procedure

1.  Navigate to **sys\_analytics\_user\_property\_config.list**.

2.  Select **New**.

3.  Choose the table with the user property to filter on:

    -   **sys\_user**

        Configure a filter on any field of type Boolean, choice, or reference.

    -   **sys\_user\_grmember**

        Get the groups a user belongs to.

    -   **sys\_user\_has\_role**

        Get the list of roles a user has.

4.  Select **Submit**.


## Result

The field you select is added as an optional filter for all Usage Insights pages including single and cross application overviews, Retention, Cohort, Funnel, Pages, Users, Events, and Sessions. Users can also apply them on Platform Analytics dashboards.

**Note:** While the filter is visible immediately, it takes 24-48 hours to synchronize the data with the filter so that it is useful.

**Parent Topic:**[Configuring Usage Insights](../content-framework/create/configuring-user-exp-analytics.md)


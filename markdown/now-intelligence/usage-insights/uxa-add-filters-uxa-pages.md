---
title: Add user properties as filters to Usage Insights
description: In addition to the default filters on the pages of the Usage Insights application, you can add filters based on user properties. This allows you to effectively segment your Usage Insights data to develop a deeper understanding of your users and their usage patterns. User properties-based filters are supported as global filters for all pages and objects in the Usage Insights application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/usage-insights/uxa-add-filters-uxa-pages.html
release: yokohama
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [User privacy, tracking, and consent, Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
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

**Parent Topic:**[User privacy, tracking, and user consent management in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/user-exp-analytics-track-options.md)


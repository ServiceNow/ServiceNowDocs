---
title: Enable User Experience Analytics
description: You can enable or disable User Experience Analytics for specific applications via the User Experience Analytics settings table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/now-intelligence/usage-insights/config-analytics-settings.html
release: xanadu
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Enable User Experience Analytics

You can enable or disable User Experience Analytics for specific applications via the User Experience Analytics settings table.

## Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

**Note:** To turn on user analytics tracking for Service Portal, see . [Create User Experience Analytics settings for Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-user-interface/service-portal/create-sp-analytics-settings.md).

## Procedure

1.  Navigate to **All** &gt; **User Experience Analytics** &gt; **Settings**.

2.  On the list, locate the record for the application you want to enable analytics tracking on.

    The application name is listed in the **Name** column.

3.  On the same row, ensure the **Enabled** column value is set to **false**.

4.  On the form, select **Enabled**.

5.  Select **Update**.

    \[Omitted image "enable-uea-application.png"\] Alt text: Enable a user experience analytics application


## What to do next

Assign a web\_analytics\_viewer or portal\_analytics\_viewer role to users to enable them to view the **Dashboard**.

**Parent Topic:**[Configuring User Experience Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/usage-insights/configuring-user-exp-analytics.md)


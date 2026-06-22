---
title: Enable Usage Insights
description: You can enable or turn off Usage Insights for all applications in Usage Insights Properties.You can enable or turn off Usage Insights for specific Core UI, Next Experience, and mobile applications on the Usage Insights Settings table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/usage-insights/enable-user-experience-analytics.html
release: zurich
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Usage Insights, Platform Analytics]
---

# Enable Usage Insights

You can enable or turn off Usage Insights for all applications in Usage Insights Properties.

## Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

Usage Insights is enabled by default for all applications.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **UX Analytics Settings &gt; Properties**.

2.  Confirm that the Usage Insights check box is selected.

    To turn it off for all applications, clear the check box.


**Parent Topic:**[Configuring Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/configuring-user-exp-analytics.md)

## Enable Usage Insights for specific applications

You can enable or turn off Usage Insights for specific Core UI, Next Experience, and mobile applications on the Usage Insights Settings table.

### Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

**Note:** These instructions are for Core UI, Next Experience, and mobile applications only. For instructions on enabling analytics tracking for portal applications, see [Track Usage Insights in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/service-portal/create-sp-analytics-settings.md).

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **UX Analytics Settings** &gt; **Settings**.

2.  On the list, locate the record for the application you want to enable analytics tracking on.

    The application name is listed in the **Name** column.

3.  Select the name of the application.

4.  On the form, select **Active**.

5.  Select **Update**.

    \[Omitted image "uxa-enable-application.png"\] Alt text: Enable a user experience analytics application

    **Note:** ServiceNow collects basic usage data to improve our products and services even when Usage Insights is disabled.


### What to do next

Assign a web\_analytics\_viewer or portal\_analytics\_viewer role to users to enable them to view the Usage Insights application.


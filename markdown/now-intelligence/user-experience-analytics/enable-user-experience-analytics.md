---
title: Enable Usage Insights
description: You can enable or turn off Usage Insights for all applications in Usage Insights Properties.You can enable or turn off Usage Insights for specific Core UI, Next Experience, and Mobile applications on the Usage Insights Settings table.
locale: en-US
release: australia
product: User Experience Analytics
classification: user-experience-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Usage Insights, Usage Insights, Platform Analytics]
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


**Parent Topic:**[Configuring Usage Insights](../content-framework/create/configuring-user-exp-analytics.md)

## Enable Usage Insights for specific applications

You can enable or turn off Usage Insights for specific Core UI, Next Experience, and Mobile applications on the Usage Insights Settings table.

### Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **UX Analytics Settings** &gt; **Settings**.

2.  On the list, locate the record for the application you want to enable analytics tracking on.

    The application name is listed in the **Name** column.

3.  Select the name of the application.

4.  On the form, select **Active**.

5.  Select **Update**.

    ![Enable a Usage Insights application](../image/uxa-enable-application.png)

    **Note:** ServiceNow collects basic usage data to improve our products and services even when Usage Insights is disabled.


### What to do next

Assign a web\_analytics\_viewer or portal\_analytics\_viewer role to users to enable them to view the Usage Insights application.

[Track Usage Insights in Service Portal](https://www.servicenow.com/docs/access?context=create-sp-analytics-settings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) to monitor key performance indicators with the Usage Insights application.


---
title: Enable User Experience Analytics
description: You can enable or turn off User Experience Analytics for all applications in User Experience Analytics Properties.You can enable or turn off User Experience Analytics for specific Core UI, Next Experience, and mobile applications on the User Experience Analytics Settings table.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, User Experience Analytics, Platform Analytics]
---

# Enable User Experience Analytics

You can enable or turn off User Experience Analytics for all applications in User Experience Analytics Properties.

## Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

User Experience Analytics is enabled by default for all applications.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **UX Analytics Settings &gt; Properties**.

2.  Confirm that the User Experience Analytics check box is selected.

    To turn it off for all applications, clear the check box.


**Parent Topic:**[Configuring User Experience Analytics](../content-framework/create/configuring-user-exp-analytics.md)

## Enable User Experience Analytics for specific applications

You can enable or turn off User Experience Analytics for specific Core UI, Next Experience, and mobile applications on the User Experience Analytics Settings table.

### Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

**Note:** These instructions are for Core UI, Next Experience, and mobile applications only. For instructions on enabling analytics tracking for portal applications, see [Track User Experience Analytics in Service Portal](https://www.servicenow.com/docs/access?context=create-sp-analytics-settings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **UX Analytics Settings** &gt; **Settings**.

2.  On the list, locate the record for the application you want to enable analytics tracking on.

    The application name is listed in the **Name** column.

3.  Select the name of the application.

4.  On the form, select **Active**.

5.  Select **Update**.

    ![Enable a user experience analytics application](../image/uxa-enable-application.png)

    **Note:** ServiceNow collects basic usage data to improve our products and services even when User Experience Analytics is disabled.


### What to do next

Assign a web\_analytics\_viewer or portal\_analytics\_viewer role to users to enable them to view the User Experience Analytics application.


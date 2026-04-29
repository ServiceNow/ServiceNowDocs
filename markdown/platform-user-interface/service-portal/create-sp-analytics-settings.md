---
title: Track Usage Insights in Service Portal
description: Track Usage Insights for Service Portal to monitor key performance indicators with the Usage Insights application.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Usage Insights for Service Portal, Analytics and Reporting Solutions for Service Portal, Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Track Usage Insights in Service Portal

Track Usage Insights for Service Portal to monitor key performance indicators with the Usage Insights application.

## Before you begin

Role required: portal\_analytics\_admin

## About this task

By default, tracking is not enabled for portals. You need to enable tracking for a specific portal only if you enabled tracking for some portals but not others in a previous version.

Portals that have been configured for tracking are listed in the Usage Insights settings \[sys\_analytics\_bucket\] table. For information about managing existing analytics settings for a portal, see [Configure Usage Insights Settings](https://www.servicenow.com/docs/access?context=config-analytics-settings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  Select the portal title.

3.  On the portal form, select **Create Analytics Settings**.

    **Note:** If a portal has already been configured for tracking, the button name will be **View Analytics Settings**.

4.  On the Usage Insights Settings form, specify which users to track.

    -   To track analytics only for authenticated users, clear the **Enable Unauthenticated User Tracking** check box.
    -   To track analytics for both unauthenticated and authenticated users, select the **Enable Unauthenticated User Tracking** check box.
    **Note:** If you enabled unauthenticated user tracking, you might be required by law to notify unauthenticated users that you are tracking their usage for analysis. To display a legal notice, activate the Privacy Notice announcement, which is inactive by default. For more information, see [Activate the privacy notice for unauthenticated users](activate-privacy-notice.md).

5.  Select **Update**.


## Result

You can now view user analytics tracking for the selected portal by navigating to **All** &gt; **Platform Analytics** &gt; **Usage Insights**. For more information on using the Usage Insights application, see [Overview of the Usage Insights application](https://www.servicenow.com/docs/access?context=user-exp-analytics-dashboard&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Usage Insights for Service Portal](../concept/sp-analytics.md)

**Related topics**  


[Enable Usage Insights](https://www.servicenow.com/docs/access?context=enable-user-experience-analytics&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)


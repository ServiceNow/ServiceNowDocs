---
title: Activate the privacy notice for unauthenticated users
description: If you enabled unauthenticated user tracking in your portal, you may be required by law to notify unauthenticated users that you are tracking their usage for analysis. You can display a legal notice by activating the Privacy Notice announcement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-user-interface/service-portal/activate-privacy-notice.html
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics for Service Portal, Analytics and Reporting Solutions for Service Portal, Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate the privacy notice for unauthenticated users

If you enabled unauthenticated user tracking in your portal, you may be required by law to notify unauthenticated users that you are tracking their usage for analysis. You can display a legal notice by activating the Privacy Notice announcement.

## Before you begin

By default, unauthenticated user tracking is turned off for portals. To modify analytics settings for a portal, see [Configure User Experience Analytics Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/config-analytics-settings.md).

Role required: sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Announcements** and open the inactive record named **Privacy Notice**.

2.  Review the form.

    You can modify the default text of the **Summary** field or leave it as-is.

    \[Omitted image "privacy-notice-announcement.png"\] Alt text: The Privacy Notice form, including the default text of the notice.

    By default, the **Unauthenticated only** option is selected to display the announcement only to users who haven't logged in to the portal. The announcement disappears after the user logs in.

3.  In the Portals section, select a portal in which to display the announcement.

    If no portals are available, select **Insert a new row** and specify a portal.

    \[Omitted image "portal-section-privacy-announcement.png"\] Alt text: Portals section in the Announcement form.

    **Note:** The Privacy Notice announcement appears only in portals for which have User Experience Analytics settings.

4.  Activate the announcement by selecting the **Active** option.

5.  Select **Update**.


## Result

The Privacy Notice announcement is displayed to unauthenticated portal users.

\[Omitted image "privacy-notice-example.png"\] Alt text: Privacy Notice announcement in a portal.

**Parent Topic:**[User Experience Analytics for Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-user-interface/service-portal/sp-analytics.md)

**Related topics**  


[Create an announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-user-interface/service-portal/create-announcement.md)


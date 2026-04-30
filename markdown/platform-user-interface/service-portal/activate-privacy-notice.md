---
title: Activate the privacy notice for unauthenticated users
description: If you enabled unauthenticated user tracking in your portal, you may be required by law to notify unauthenticated users that you are tracking their usage for analysis. You can display a legal notice by activating the Privacy Notice announcement.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics for Service Portal, Analytics and Reporting Solutions for Service Portal, Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate the privacy notice for unauthenticated users

If you enabled unauthenticated user tracking in your portal, you may be required by law to notify unauthenticated users that you are tracking their usage for analysis. You can display a legal notice by activating the Privacy Notice announcement.

## Before you begin

By default, unauthenticated user tracking is turned off for portals. To modify analytics settings for a portal, see [Configure User Experience Analytics Settings](https://www.servicenow.com/docs/access?context=enable-user-experience-analytics&version=zurich&pubname=zurich-now-intelligence&section=config-analytics-settings&ft:locale=en-US).

Role required: sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Announcements** and open the inactive record named **Privacy Notice**.

2.  Review the form.

    You can modify the default text of the **Summary** field or leave it as-is.

    ![The Privacy Notice form, including the default text of the notice.](../image/privacy-notice-announcement.png "Privacy Notice announcement form")

    By default, the **Unauthenticated only** option is selected to display the announcement only to users who haven't logged in to the portal. The announcement disappears after the user logs in.

3.  In the Portals section, select a portal in which to display the announcement.

    If no portals are available, select **Insert a new row** and specify a portal.

    ![Portals section in the Announcement form.](../image/portal-section-privacy-announcement.png "Portals section")

    **Note:** The Privacy Notice announcement appears only in portals for which have User Experience Analytics settings.

4.  Activate the announcement by selecting the **Active** option.

5.  Select **Update**.


## Result

The Privacy Notice announcement is displayed to unauthenticated portal users.



**Parent Topic:**[User Experience Analytics for Service Portal](../concept/sp-analytics.md)

**Related topics**  


[Create an announcement](create-announcement.md)


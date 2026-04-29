---
title: Posting announcements to portal users
description: Announcements broadcast messages to Service Portal users. They display in an announcement banner or an announcement widget instance.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Portal, Configure UIs and portals, Configure user experiences]
---

# Posting announcements to portal users

Announcements broadcast messages to Service Portal users. They display in an announcement banner or an announcement widget instance.

Announcements are active on new instances. To activate announcements after upgrade, you can activate the Service Portal Announcements plugin \(com.glide.service-portal.announcements\).

When creating announcements, you can define the way an announcement displays.

-   **Sort order**

    Announcements are displayed depending on the order defined in:

    -   The **glide.service\_portal.announcement.default\_sort\_order** system property. See [Service Portal properties](properties-service-portal.md).
    -   The **Display First** field in the announcement record.
    If there is a tie between two records set to **Display first**, the sort order defined in the system property is honored.

-   **Display location**

    Announcements can display in the following locations:

    -   Announcement banner
    -   [Announcements widget](announcements-widget.md) instance
    To define the announcement display location, define the announcement type in the announcement record.

-   **Display Style**

    Using display styles, you can:

    -   Create a custom color scheme.
    -   Change the text alignment.
    Announcements that appear in a banner use the display style defined in the Announcement record by default. To use the display style in an instance of the Announcements widget, you can select the **Use Display Style** instance option.

-   **User criteria**

    If user criteria is set up for the Service Portal, you can define who can and who cannot view an announcement. Through user criteria, you can create announcements only visible to specific users, groups, roles, organizations, and more.


-   **[Create an announcement](../task/create-announcement.md)**  
An announcement appears as a banner in Service Portal or within the announcements widget.
-   **[Create an announcement display style](../task/create-announcement-style.md)**  
Define the background color, foreground color, and text alignment of an announcement.
-   **[Create an announcement type](../task/add-announcement-type.md)**  
Announcement types determine where an announcement displays. Announcements include two base system types: banner and widget.

**Parent Topic:**[Service Portal](c_ServicePortal.md)


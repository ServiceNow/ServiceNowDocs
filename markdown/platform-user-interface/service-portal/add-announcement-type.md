---
title: Create an announcement type
description: Announcement types determine where an announcement displays. Announcements include two base system types: banner and widget.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Posting announcements to portal users, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create an announcement type

Announcement types determine where an announcement displays. Announcements include two base system types: banner and widget.

## Before you begin

Role required: admin, sp\_admin, or announcement\_admin

## About this task

Similar to creating a category tag, you can create alternative types to define custom locations. For example, to display an announcement only in a specific widget instance, you can create an announcement type for that widget instance. Any announcements tagged with that type will only display in the desired widget instance.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **Announcement Consumer Type**.

    The Announcement Consumer Type table \[announcement\_consumer\_type\] opens.

2.  In the Columns section of the form, Click **New**.

3.  Define a **Name**.

    The name is used to associate an announcement with a widget instance.

4.  Click **Save**.

5.  Add the custom type to an announcement.

    1.  Navigate to **Service Portal** &gt; **Announcements**.

    2.  Open an existing announcement or create a new announcement.

    3.  In the **Type** field, select the custom type.

    4.  Click **Save**.

6.  If using the type in a widget, define the type as a widget instance option.

    The announcement banner only displays announcements tagged with the **Banner** type.

    1.  Navigate to an instance of the Announcement widget.

    2.  Control + right-click the widget instance and select **Instance Options**.

    3.  In the **Type** field, select the custom announcement type.


## Result

The widget instance associated with the type displays any announcements tagged with the same type.

**Parent Topic:**[Posting announcements to portal users](../concept/announcements.md)

**Related topics**  


[Create an announcement](create-announcement.md)

[Create an announcement display style](create-announcement-style.md)


---
title: Create an announcement display style
description: Define the background color, foreground color, and text alignment of an announcement.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Posting announcements to portal users, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create an announcement display style

Define the background color, foreground color, and text alignment of an announcement.

## Before you begin

Role required: admin, sp\_admin, or announcement\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Announcements**.

2.  Open an existing announcement or create a new announcement.

3.  In the **Display style** field, click the reference lookup icon to open the referenced table.

    The Announcement Styles \[announcement\_style\] list view opens.

4.  Click **New** to create a new display style.

5.  Complete the form.

<table id="table_esz_sfs_w1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Internal name of the display style.

</td></tr><tr><td>

Application

</td><td>

The application scope of the announcement. This value is read-only.

</td></tr><tr><td>

Background color

</td><td>

Color name or HEX value in the format \#000000 for the announcement background.

</td></tr><tr><td>

Foreground color

</td><td>

Color name or HEX value in the format \#000000 for the announcement text.

</td></tr><tr><td>

Alignment

</td><td>

Text alignment. Options include:-   Left align
-   Center align


</td></tr></tbody>
</table>6.  Click **Submit**.


## Result

By default, the announcement appears in both the portal banner and the Announcements widget, but only the banner uses your new display style. You can configure the widget to use the display style also. For more information, see the instance options in [Announcements widget](../concept/announcements-widget.md).

**Parent Topic:**[Posting announcements to portal users](../concept/announcements.md)

**Related topics**  


[Create an announcement](create-announcement.md)

[Create an announcement type](add-announcement-type.md)


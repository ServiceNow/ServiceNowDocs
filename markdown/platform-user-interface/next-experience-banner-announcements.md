---
title: Next Experience banner announcements
description: Banner announcements enable you to communicate planned maintenance, unplanned outages, or important events like ESPP stock plans or benefits enrollment to those affected or to everyone. You can target specific experiences or all experiences.Configure banner announcements to communicate important information to your users while they are in an experience.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Next Experience banner announcements

Banner announcements enable you to communicate planned maintenance, unplanned outages, or important events like ESPP stock plans or benefits enrollment to those affected or to everyone. You can target specific experiences or all experiences.

**Note:** Beginning with the San Diego release, configure banner announcements instead of updating the **glide.product.description** system property.

![Banner announcement.](../image/pol-banner-announcement.png)

You can configure the following aspects of banner announcements:

-   Use colors and icons to communicate the type of announcement and the importance of the banner announcement.
-   Provide a link for information or to complete a task.
-   Schedule banner announcements for a specific time.

    **Note:** If a user dismisses a banner announcement during a session and the announcement is still active, it will re-appear once the user logs out and back in to a new session.


**Parent Topic:**[Configuring the Next Experience UI](next-experience-ui-admin.md)

## Configure Next Experience banner announcements

Configure banner announcements to communicate important information to your users while they are in an experience.

### Before you begin

Role required: announcement\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Banner Announcements** to create an announcement.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_yyw_xxr_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Heading

</td><td>

Unique name for your banner announcement mapping, which will display as the title of the banner announcement.**Note:** The heading character limit is 100 characters.

</td></tr><tr><td>

Summary

</td><td>

Optional additional banner content, which displays below the Heading in the banner announcement.**Note:** The summary character limit is 200 characters.

</td></tr><tr><td>

Start

</td><td>

Date and time the banner announcement will begin displaying in the UI.

</td></tr><tr><td>

End

</td><td>

Date and time the banner announcement will stop displaying in the UI.

</td></tr><tr><td>

Color

</td><td>

Color to show the importance or urgency of the banner announcement.

</td></tr><tr><td>

Add a link

</td><td>

Option to provide a link in the banner announcement.

**Note:** The link label character limit is 50 characters.

 Selecting this option displays the following link configuration fields:

 -   Click behavior: Behavior of the link when selected, either opening in the same window or a new window.
-   Label: Text displayed with the link.
-   URL: URL of the link.


</td></tr><tr><td>

Non-dismissible

</td><td>

Option to make the banner non-dismissible by users. Non-dismissible banners cannot be closed.

</td></tr><tr><td>

Non-stackable

</td><td>

Option to make the banner non-stackable. Non-stackable banners are displayed individually in the banner announcement area.

</td></tr><tr><td>

Show for

</td><td>

Scope of the banner announcement display, either for all logged-in users, users with specific roles or groups, or anonymous plus all logged-in users.

</td></tr><tr><td>

Icon

</td><td>

Icon to depict the urgency or category of the banner announcement. For example, a flame icon can show increased urgency and a graduation cap icon can notify of continuing learning opportunities.

</td></tr><tr><td>

Icon tooltip

</td><td>

Text describing the icon.

</td></tr><tr><td>

Content position

</td><td>

Options for the horizontal position of the banner content.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

    The Associated to Configurations related list displays at the bottom of the form.

5.  In the Associated to Configurations related list, select **New**.

    ![Associated to Configurations related list.](../image/next-exp-associated-config.png "Associated to Configurations related list")

6.  In the Announcement Config field, select the Lookup using list icon ![The Lookup using list icon.](../image/QueryIcon.png).

7.  Select **Unified Navigation** from the Banner Announcement Configs list.



    ![Banner Announcement Configs list with Unified Navigation selected.](../image/next-exp-banner-config.png)

8.  On the Banner Announcement Mapping form, set the order of the banner announcement mapping.

    The lower the order of the banner announcement mapping, the higher the priority is of the banner announcement mapping. An order value of 0 is not allowed.

9.  On the Banner Announcement Mapping form, select **Submit**.

10. On the Banner Announcement form, select **Update**.



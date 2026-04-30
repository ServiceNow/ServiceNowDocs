---
title: Create an announcement
description: An announcement appears as a banner in Service Portal or within the announcements widget.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Posting announcements to portal users, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create an announcement

An announcement appears as a banner in Service Portal or within the announcements widget.

## Before you begin

Role required: announcement\_admin, sp\_admin, or admin

## About this task

The title and summary of an announcement can be localized in the Translated Text \[sys\_translated\_text\] table. For more information, see [Translating text fields](https://www.servicenow.com/docs/access?context=c_UseTranslatedText&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Announcements**.

    The Announcements \[announcement\] table displays all announcements.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_hzl_5tj_r1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Internal title that doesn't display in the announcement.

</td></tr><tr><td>

Active

</td><td>

Option to activate the announcement. To hide an announcement, clear the **Active** check box.

</td></tr><tr><td>

Title

</td><td>

Title to appear in the announcement.

</td></tr><tr><td>

From

</td><td>

Date and time that the announcement begins to appear.

</td></tr><tr><td>

To

</td><td>

Date and time that the announcement ends. If left empty, the announcement continues to appear until it's deactivated.

</td></tr><tr><td>

Summary

</td><td>

Text to appear in the announcement.

</td></tr><tr><td>

Display style

</td><td>

Defines the background color, text color, and text alignment of banner announcements. Base system styles include: -   **Normal**: Blue background and left-aligned, white text.
-   **Urgent**: Red background and left-aligned, white text.
 Announcements that appear in a banner use the display style defined in the Announcement record, by default. To use the display style in an instance of the Announcements widget, you can select the **Use Display Style** instance option.

</td></tr><tr><td>

Type

</td><td>

Defines where an announcement displays. By default, announcements appear in the following locations:

 -   **Banner**: Announcement banner above the banner frame in the Service Portal.
-   **Widget**: Instance of the announcements widget.
 You can create an announcement type to define other widget instances to display an announcement.

</td></tr><tr><td>

Glyph

</td><td>

Glyph to display to the left of the title in banner announcements.

</td></tr><tr><td>

Glyph alt text

</td><td>

Alternative text for the glyph icon used with screen readers.

</td></tr><tr><td>

Public

</td><td>

Option to display the announcement to users before and after they've logged in.

</td></tr><tr><td>

Display first

</td><td>

If selected, the announcement displays before all other announcements. If there is a tie between two records set to **Display first**, the sort order defined in the **glide.service\_portal.announcement.default\_sort\_order** system property is honored. See [Service Portal properties](../concept/properties-service-portal.md).

</td></tr><tr><td>

Roles

</td><td>

If **Public** is not selected, you can define the roles that the announcement is visible to. If left empty, the announcement is visible to all roles.**Note:** Alternatively, you can define user criteria for the announcement instead. To do so, set up [User criteria for Service Portal](../concept/user-criteria.md) and clear the **Public** check box. Announcements display to only the users who pass the access criteria.

</td></tr><tr><td>

Unauthenticated only

</td><td>

Option to display the announcement only to users who haven't logged in.This option appears only if **Public** is selected.

</td></tr><tr><td>

Click target

</td><td>

Creates a link below the announcement body that opens to a target page or URL. -   **None**: Announcement doesn't include a link.
-   **Page**: Opens a Service Portal page in the current browser tab.
-   **URL in current browser tab**: Opens a URL in the current browser tab.
-   **URL in new browser tab**: Opens a URL in a new browser tab.


</td></tr><tr><td>

Details page

</td><td>

The page that opens in the current browser tab. Available if the **Click target** is **Page**.

</td></tr><tr><td>

Details URL

</td><td>

The URL that opens in the current or new browser tab. Available if the **Click target** is **URL in current browser tab** or **URL in new browser tab**.

</td></tr><tr><td>

Details link text

</td><td>

Link text for the page or URL click target. If you leave this field empty and define a click target, the title of the announcement is "Learn More".

</td></tr><tr><td>

Dismiss options

</td><td>

Determines whether the user can dismiss the announcement. Options include: -   User can dismiss - no redisplay
-   User can dismiss for current session only
-   User cannot dismiss


</td></tr><tr><td>

Portals

</td><td>

Portals that display the announcement. If this field is empty, the announcement displays in all portals.

</td></tr></tbody>
</table>4.  Save or submit the record.


## What to do next

If the **Type** is **Banner**, test your announcement by navigating to the portal defined in the **Portals** field. If the **Type** is **Widget** or a custom type, test your announcement by navigating to the page with the associated widget instance.

**Parent Topic:**[Posting announcements to portal users](../concept/announcements.md)

**Related topics**  


[Create an announcement display style](create-announcement-style.md)

[Create an announcement type](add-announcement-type.md)


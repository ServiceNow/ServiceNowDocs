---
title: Manage an announcement for communicating about major incidents
description: Create and manage an announcement to broadcast messages for Service Portal users to keep them informed about the ongoing major incident. Major incident managers can create and deploy announcements from Service Operations Workspace \(SOW\).
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Communicating with stakeholders about incidents and major incidents, Managing a major incident record, Major Incident Management in Service Operations Workspace, Incident Management in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Manage an announcement for communicating about major incidents

Create and manage an announcement to broadcast messages for Service Portal users to keep them informed about the ongoing major incident. Major incident managers can create and deploy announcements from Service Operations Workspace \(SOW\).

## Before you begin

Role required: announcement\_admin, sp\_admin or admin

As a major\_incident\_manager, you must inherit any of the required roles to create and manage announcements in Major Incident Management.

## About this task

Announcements can be displayed in an announcement banner or an announcement widget instance. For more information, see [Posting announcements to portal users](https://www.servicenow.com/docs/access?context=announcements&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Procedure

1.  On the incident record page, select the **Communicate** tab.

2.  Select **Manage announcements**.

    A list of all major incident announcement records, is displayed. You can select any announcement record and modify the record. Else, create a new announcement record.

3.  Select **New**.

4.  On the **Details** tab of the form, fill in the fields.

<table id="table_hzl_5tj_r1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Announcement

</td></tr><tr><td>

Name

</td><td>

Internal title that isn't displayed in an announcement.

</td></tr><tr><td>

Active

</td><td>

Option to activate the announcement. To hide an announcement, clear the **Active** check box.

</td></tr><tr><td>

Title

</td><td>

Title that appears in the announcement.

</td></tr><tr><td>

From

</td><td>

Date and time at which the announcement begins to appear.

</td></tr><tr><td>

To

</td><td>

Date and time at which the announcement ends. If no date and time is entered, the announcement continues to appear until it's deactivated.

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

Defines where an announcement displays. By default, announcements appear in the following locations:-   **Banner**: Announcement banner above the banner frame in the Service Portal.
-   **Widget**: Instance of the announcement widget.
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

Option to display the announcement before all other announcements. **Note:** If two records set to **Display first** exist, the sort order defined in the **glide.service\_portal.announcement.default\_sort\_order** system property is implemented. For more information, see [Service Portal properties](https://www.servicenow.com/docs/access?context=properties-service-portal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Roles

</td><td>

User roles to whom the announcement is visible. If left empty, the announcement is visible to all roles.**Note:**

-   If the **Public** check box is cleared, you can define the user roles to whom the announcement is visible.
-   Alternatively, you can define user criteria for the announcement instead. To do so, set up [User criteria for Service Portal](https://www.servicenow.com/docs/access?context=user-criteria&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) and clear the **Public** check box. Announcements are displayed to only the users who pass the access criteria.


</td></tr><tr><td>

Unauthenticated only

</td><td>

Option to display the announcement only to users who haven't logged in.**Note:** This option appears only if the **Public** check box is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Behaviour

</td></tr><tr><td>

Click target

</td><td>

Creates a link below the announcement body that opens to a target page or URL. Possible values:-   **None**: Announcement doesn't include a link.
-   **Page**: Opens a Service Portal page in the current browser tab.
-   **URL in current browser tab**: Opens a URL in the current browser tab.
-   **URL in new browser tab**: Opens a URL in a new browser tab.


</td></tr><tr><td>

Details page

</td><td>

Page that opens in the current browser tab. **Note:** This option is applicable only if the **Click target** field is set to **Page**.

Available if

</td></tr><tr><td>

Details URL

</td><td>

URL that opens in the current or new browser tab. **Note:** This option is applicable only if the **Click target** is set to **URL in current browser tab** or **URL in new browser tab**.

</td></tr><tr><td>

Details link text

</td><td>

Link text for the page or URL click target. If you leave this field empty and define a click target, the title of the announcement is "Learn More".

</td></tr><tr><td>

Dismiss options

</td><td>

Determines whether the user can dismiss the announcement. Possible values: -   User can dismiss - no redisplay
-   User can dismiss for current session only
-   User cannot dismiss


</td></tr><tr><td>

Portals

</td><td>

Portals that display the announcement. If this field is empty, the announcement displays in all portals.

</td></tr></tbody>
</table>5.  Select **Save**.

    A **Related records** tab appears.

6.  On the **Related records** tab, you use the following related links.

    -   Can View: Contains a list of user criteria to enable the users to view the announcements based on role, department, group, location, or company.
    -   Cannot View: Contains a list of user criteria to block users from viewing the announcements based on role, department, group, location, or company.
    You can select an existing user criteria or select **New** to create a user criteria. For more information, see [User criteria for Service Portal](https://www.servicenow.com/docs/access?context=user-criteria&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


## What to do next

If the **Type** is **Banner**, test your announcement by navigating to the portal defined in the **Portals** field. If the **Type** is **Widget** or a custom type, test your announcement by navigating to the page with the associated widget instance.

**Parent Topic:**[Communicating with stakeholders about incidents and major incidents](../concept/communicating-with-stakeholders-sow.md)


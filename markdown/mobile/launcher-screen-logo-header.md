---
title: Configure launcher screen header with logo
description: Add a logo to the launcher screen header to match your organization’s branding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/launcher-screen-logo-header.html
release: australia
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [Launcher screen headers, Create a launcher screen, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure launcher screen header with logo

Add a logo to the launcher screen header to match your organization’s branding.

## Before you begin

Role required: admin

-   This feature is supported from iOS version 26 and later.
-   You must be on ServiceNow mobile client version 22.2 or later.
-   You must be using one of the following ServiceNow patches:
    -   Brazil Patch 1 and later
    -   Australia Patch 7 and later
    -   Zurich Patch 13 and later

## About this task

Configure a logo image to display in the top navigation bar of a launcher screen instead of a text title. The logo is sourced from an image stored in the instance's local database, and this setting is configured individually for each launcher screen.

For the images used in the logo, consider the following:

-   Logo proportions vary by design, so exact sizing isn't fixed. Provide a high-resolution, transparent PNG or JPEG image for both light and dark themes
-   The display height can vary between 16px and 38px on the mobile device. However, the size of the logo on the mobile device is determined according to the logo proportions.
-   Use a different logo for light and dark theme to create visibility and contrast against both types of background.

**Note:** The configuration of the logo-based launcher screen header is performed in the ServiceNow AI Platform.

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_applet\_launcher.list**.

2.  Select **New** in the Launcher screens table.

3.  Complete the fields in the launcher screen table as needed.

    The mandsatory fields for this feature are detailed after the table.

<table id="table_ob2_jtl_tkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the header function instance. This name is internal and isn't visible to end-users.

</td></tr><tr><td>

Access control type

</td><td>

User roles and user criteria permissions are access control mechanisms that enable you to define roles or segment users into groups within the mobile platform.

</td></tr><tr><td>

Active

</td><td>

Toggle that turns the header function on and off. If the toggle is enabled, the header function is enabled.

</td></tr><tr><td>

Required roles

</td><td>

**Note:** This option is displayed when User roles is selected in the **Access control type** field.

 Select User roles to control access to features and components within mobile apps for defined target audiences.

</td></tr><tr><td>

Available offline

</td><td>

Select to enable the display of the launcher screen header in offline mode.

</td></tr><tr><td>

Header display mode

</td><td>

Select whether to use text or a logo in the header area of the launcher screen.

</td></tr><tr><td>

Launcher header title

</td><td>

**Note:** This option is displayed when Show title is selected in the **Header display mode** field.

Select the target record to display the launcher screen header title.

</td></tr><tr><td>

Logo

</td><td>

**Note:** This option is displayed when Show title is selected in the **Header display mode** field.

Select the search button to select existing logos or to create a logo.

</td></tr></tbody>
</table>4.  Enter a name for your launcher screen record.

5.  Select Show logo in the **Header display mode** field.

6.  Select the magnify glass in the **Logo** field.

7.  Select **New** in the Logo table.

8.  Enter the name for your logo record.

9.  Add your preconfigured light and dark logos, by selecting the attachment icon.

    **Note:** Using a different logo for both light and dark modes creates visibility and contrast against both types of background.

10. Select **Choose file** in the Attachments pop-up.

11. Select the images for the light and dark logos.

12. Back in the Logo record, enter the names of the lights and dark logos

13. Select **Submit**.

    The Launcher screen displays, with your named logo record in the Logo field.

14. In the Launcher screen page, right-click in the header and select **Save**.



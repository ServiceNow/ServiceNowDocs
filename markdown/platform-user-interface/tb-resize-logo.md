---
title: Resize a logo for your login screen
description: After you have uploaded a logo for your login screen, you can resize the logo by creating and setting a system property.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Upload new logo, Global styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Resize a logo for your login screen

After you have uploaded a logo for your login screen, you can resize the logo by creating and setting a system property.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

## Procedure

1.  In the Unified Navigation All menu, enter `sys_properties.list` and press **Enter**.

    ![All menu.](../../../get-started/servicenow-overview/image/pol-nav-all-p.png "Unified Navigation All menu")

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) called glide.ui.polaris.login.logo.height.

3.  Set the system property **Value** to the maximum CSS height value for your logo.

    For example, any of the following would be valid entries:

    -   150px
    -   6em
    -   75%
    -   auto
    If you select **auto**, the browser calculates a height for the specified element.

    **Note:** An entry of 100% returns the logo to its original size.

4.  Save the system property.

    At the next launch, your logo is resized based on how you configured the system property.


**Parent Topic:**[Upload a new logo to your Theme Builder theme](tb-upload-logo.md)


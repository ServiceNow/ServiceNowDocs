---
title: Resize a logo for your login screen
description: After you have uploaded a logo for your login screen, you can resize the logo by creating and setting a system property.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Upload a logo while publishing a theme with Theme Builder, Publish your themes with Theme Builder, Configuring Next Experience with Theme Builder, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Resize a logo for your login screen

After you have uploaded a logo for your login screen, you can resize the logo by creating and setting a system property.

## Before you begin

Role required: admin

## Procedure

1.  In the Navigation filter, enter `sys_properties.list` and press **Enter**.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) called glide.ui.polaris.login.logo.height.

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


**Parent Topic:**[Upload a logo while publishing a theme with Theme Builder](tb-upload-logo.md)


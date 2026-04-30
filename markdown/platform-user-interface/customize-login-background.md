---
title: Customize the Next Experience login background illustration
description: Customize and change the background illustration applied to your Next Experience login page.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-29"
reading_time_minutes: 1
breadcrumb: [Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Customize the Next Experience login background illustration

Customize and change the background illustration applied to your Next Experience login page.

## Before you begin

Role required: admin

## About this task

This procedure is specific to login pages and does not apply if you are using Single Sign-On \(SSO\).

The background illustration that you upload automatically scales to fit the screen.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Images**.

2.  Select **New** to create an image record.

3.  On the new image record, enter a file name such as `login_background.jpg`

    **Note:** Image names must end with .gif, .png, .jpg, .ico, .svg or .bmp.

4.  Select **Click to add** image.

    ![Image record form with Name entered and Click to add image selected.](../image/next-exp-new-image-record.png "Image record form")

5.  Choose your image file.

6.  Select **Update**.

    The Images table displays.

7.  Enter your file name in the **Name** field to confirm your new image is listed.

8.  Navigate to the **All** menu and enter `sys_properties.list` in the filter navigator.

9.  Select **New** to create a system property.

10. In the **Name** field, enter `glide.ui.login.style.background.image`.

11. In the **Value** field, enter your image file name.

12. In the **Type** drop-down list, select **String**.

13. Verify that the Ignore cache option is selected.

14. Select **Submit**.

    ![System property new record with Submit selected.](../image/next-exp-sys-prop-record.png "System property record")


## What to do next

Log out of your experience to view the new login page background.

**Parent Topic:**[Working with themes in Next Experience](../concept/next-experience-theming.md)


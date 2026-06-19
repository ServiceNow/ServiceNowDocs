---
title: Customize the Next Experience login background illustration
description: Customize and change the background illustration applied to your Next Experience login page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/customize-login-background.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "next-exp-new-image-record.png"\] Alt text: Image record form with Name entered and Click to add image selected.

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

    \[Omitted image "next-exp-sys-prop-record.png"\] Alt text: System property new record with Submit selected.


## What to do next

Log out of your experience to view the new login page background.

**Parent Topic:**[Working with themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/next-experience-theming.md)


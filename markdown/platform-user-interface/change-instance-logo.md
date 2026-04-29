---
title: Change instance banner logo in Next Experience
description: Change the instance banner logo displayed on the Unified Navigation and the login page to reflect your company logo.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Next Experience themes, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Change instance banner logo in Next Experience

Change the instance banner logo displayed on the Unified Navigation and the login page to reflect your company logo.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **My Company**.

2.  To upload your company logo, select **Update** beside **UI16 Banner Image**.

    ![UI16 banner image field with Update selected.](../image/next-exp-banner-logo.png)

3.  Select **Choose file** and select the file, and then select **OK**.

    To use an image URL instead of a file on your hard drive, enter the URL in the file upload window.

    **Note:** The image can be high resolution, but when it displays it is scaled based on the aspect ratio. It scales to a maximum of 20px high.

4.  Select **Update**.

5.  If new banner image doesn't display, perform a `cache.do` and `logout.do` and log back into your instance.

6.  To restore the default instance logo, update the **glide.product.image.light** system property value to **now-next-experience-logo.svg**.


**Parent Topic:**[Configuring Next Experience themes and preferences](config-next-experience-themes-prefs.md)


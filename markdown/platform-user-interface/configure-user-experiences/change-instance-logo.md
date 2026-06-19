---
title: Change instance banner logo in Next Experience
description: Change the instance banner logo displayed on the Unified Navigation and the login page to reflect your company logo.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/change-instance-logo.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
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

    \[Omitted image "next-exp-banner-logo.png"\] Alt text: UI16 banner image field with Update selected.

3.  Select **Choose file** and select the file, and then select **OK**.

    To use an image URL instead of a file on your hard drive, enter the URL in the file upload window.

    **Note:** The image can be high resolution, but when it displays it is scaled based on the aspect ratio. It scales to a maximum of 20px high.

4.  Select **Update**.

5.  If new banner image doesn't display, perform a `cache.do` and `logout.do` and log back into your instance.

6.  To restore the default instance logo, update the **glide.product.image.light** system property value to **now-next-experience-logo.svg**.


**Parent Topic:**[Configuring Next Experience themes and preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/config-next-experience-themes-prefs.md)


---
title: Customize the favicon
description: Use the glide.product.icon property to change the icon that appears in bookmarks and the browser address bar.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/customize-favicon.html
release: australia
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Create a company profile, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Customize the favicon

Use the **glide.product.icon** property to change the icon that appears in bookmarks and the browser address bar.

## Before you begin

Before you can update the favicon, you must upload the image into the database.

Role required: admin

## Procedure

1.  To upload the image, complete the following steps.

    1.  Navigate to **System UI** &gt; **Images** and click **New**.

    2.  Enter a **Name** for your image.

        Valid names must end in `.gif`, .`png`, `.jpg`, `.ico`, or `.bmp`.

    3.  Click the **Click to add** link in the **Image** field, then select and upload the image.

    4.  Click **Update**.

2.  To set the uploaded image to the favicon, complete the following steps.

    1.  Navigate to **System Properties** &gt; **System**.

    2.  In the **Icon image displayed in the bookmarks and browser address bar** field, enter the file name of the uploaded image.

    3.  Click **Save**.


## Result

The favicon appears in the bookmarks and browser address bar for the platform or the Content Management System \(CMS\). For more information on how to change the favicon for Service Portal, see [Create a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/create-a-portal.md).

**Parent Topic:**[Create a company profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_CreateACompanyProfile.md)

**Related topics**  


[Banner logo link]()

[Customize the banner logo in Core UI]()

[Examples of how to modify the banner]()

[Modify the banner]()


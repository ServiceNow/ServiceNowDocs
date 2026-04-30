---
title: Control whether users can view attachments in external applications on Android devices
description: Set the glide.sg.block\_mobile\_attachments\_external\_viewing system property to true to prevent Android users from opening attachments in third-party applications.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-05-21"
reading_time_minutes: 1
breadcrumb: [Mobile system property configurations, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Control whether users can view attachments in external applications on Android devices

Set the **glide.sg.block\_mobile\_attachments\_external\_viewing** system property to true to prevent Android users from opening attachments in third-party applications.

## Before you begin

Role required: admin

## About this task

When **glide.sg.block\_mobile\_attachments\_external\_viewing** system property is set to `true`, all attachments that are supported to be opened in the internal native viewer are opened there so the user can't open the attachment in a third-party application.

**Note:** This system property only applies to Android devices and has no effect on iOS devices. The **glide.sg.block\_mobile\_attachments\_external\_viewing** system property is available to use on Android clients, version 19.5.1 and later.

The supported file types that can be opened in the internal, native viewer on the Android OS are:

-   Images
-   Videos
-   PDFs

When a user attempts to open an attachment that isn't supported, an error message displays. For example:

![mobile attachment error message](../image/mobile-attachment-error.png)

**Note:** The following supported file types can be opened in the internal, native viewer on iOS devices:

-   iWork and Microsoft Office documents
-   Images
-   Live photos
-   Text files
-   PDFs
-   Audio files
-   Video files

However, the **glide.sg.block\_mobile\_attachments\_external\_viewing** property has no effect on iOS devices.

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Open the record for **glide.sg.block\_mobile\_attachments\_external\_viewing**.

3.  In the form, match the following values.

<table id="table_cc5_zlf_kfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.sg.block\_mobile\_attachments\_external\_viewing**

</td></tr><tr><td>

Type

</td><td>

**true \| false**

</td></tr><tr><td>

Value

</td><td>

Enter one of the following values:-   Enter `true` to prevent users from opening attachments in third-party applications on Android devices. The following attachments can only be opened in the internal native viewer: images, videos, and PDFs.
-   Enter `false` to enable users to open files in third-party applications on Android devices.


</td></tr></tbody>
</table>4.  Right-click the banner at the top of the **glide.sg.block\_mobile\_attachments\_external\_viewing** form and select **Save**.


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)


---
title: Manage attachments on details screens
description: Add, remove, rename, and view attachments in your mobile record screens.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure a details screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Manage attachments on details screens

Add, remove, rename, and view attachments in your mobile record screens.

## Enable attachments on your mobile record screens

You can enable attachments on a mobile record screen. Navigate to your record screen in Mobile App Builder. Find and select the **Activity Stream** entry in the configuration tree. Then, select **Show "Attachment" button** option in the **Settings** section of the configuration panel.

![Attachment check box on the screen configuration form in Mobile App Builder.](../image/mobile-attach-checkbox.png "Attachment check box on the screen configuration form")

For details on the record screen configuration, see [Configure a record screen for use with a list screen](../task/sg-configure-form-applet.md).

## View the attachment list on your record screens

When enabled by an administrator, the attachment list appears at the bottom of the **Details** tab of your mobile record screens. The attachment list shows a preview of each attachment that is associated with the current record. If there are no attachments, you see "No attachment" instead of the attachment list.

The following file types are supported for previewing files:

-   image files — .png, .svg, .webp, .jpg, and .jpeg
-   video files — .mp4, .mov, and .m4v
-   document files — .pdf, .xlsx, .doc, .ppt, .csv, .xls, .txt, and .docx

**Note:**

-   Audio files are not supported.
-   Some of the above file types require an external app to be installed on the device to open the file. For example, Android users can't open .docx files if Microsoft Word isn't installed on their device.
-   Some other file types might work intermittently on iOS and Android devices, but ServiceNow does not support these other file types. ServiceNow only supports the above listed file types on both iOS and Android devices.

<table id="table_y3b_mhl_t3b"><tbody><tr><td>

![Mobile record screen with an attachment](../image/sg-attachment-example.png)

</td><td>

![Mobile record screen with no attachments](../image/sg-no-attachment-example.png)

</td></tr></tbody>
</table>Tap an attachment to show a preview of the attachment.

<table id="table_cym_bkl_t3b"><tbody><tr><td>

![Mobile record screen with an attachment](../image/sg-attach-image-preview.png)

</td><td>

![Mobile record screen with no attachments](../image/sg-attach-pdf-preview.png)

</td></tr></tbody>
</table>## Manage attachments

<table id="table_e5b_4ml_t3b"><tbody><tr><td>

To delete an attachment, tap the **Delete** \(![Delete icon](../image/sg-button-delete-attachment.png)\) icon, and then click **Yes** in the confirmation pop-up window.

</td><td>

![Attachment delete confirmation](../image/sg-attachment-delete-confirm.png)

</td></tr><tr><td>

To rename an attachment, tap the **Rename** \(![Rename icon](../image/sg-button-rename-attachment.png)\) icon. Then, in the **Edit name** field, enter a name.

</td><td>

![Attachment Edit name field](../image/sg-attachment-rename.png)

</td></tr></tbody>
</table>**Note:** The ability to perform these actions are controlled by the Access Control List rules on your instance.


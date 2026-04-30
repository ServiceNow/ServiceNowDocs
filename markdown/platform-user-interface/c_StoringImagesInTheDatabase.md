---
title: Storing images in the database
description: Administrators and users with the image\_admin or content\_admin role can upload and store images in the database. These images are saved in the Images \[db\_image\] table. Uploading an image to the database allows it to be referenced from HTML fields by appending the name of the image to the URL of the instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Storing images in the database

Administrators and users with the image\_admin or content\_admin role can upload and store images in the database. These images are saved in the Images \[db\_image\] table. Uploading an image to the database allows it to be referenced from HTML fields by appending the name of the image to the URL of the instance.

**Note:** The db\_image table is a public table that does not have any security restrictions. Unauthenticated users have full access to images uploaded to the db\_image table.

## Images vs attachments

If you want to access an image from a record, or if you want to prevent users from appending the image name to the URL of the instance, upload it as an attachment instead. When you upload an image as an attachment, the image is saved in the Attachments \[sys\_attachment\] table. See [Administer attachments](https://www.servicenow.com/docs/access?context=r_AdministeringAttachments&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Add and manage attachments](../../../use/using-forms/task/t_AddingAnAttachment.md) for more information.

## Acceptable image file types

Upload image files with the following extensions:

-   .gif
-   .jpg
-   .png
-   .bmp

**Note:** The system does not support uploading zip files that contain .bmp images.

If you upload an image that may not be supported in Internet Explorer browsers, a warning message appears.

The system does not support uploading images in the .ico format through this interface. Microsoft Internet Explorer requires the .ico format for favorite icons. To upload an .ico image, attach the .ico image to a record instead of using the standard image upload interface.

To understand how to insert an image into a form record, see the [Insert an image into your article, incident, or other form record](https://www.servicenow.com/community/now-platform-blog/insert-an-image-into-your-article-incident-or-other-form-record/ba-p/2286128) blog post in the ServiceNow Community.

-   **[Update an existing image](../task/t_UpdatingAnExistingImage.md)**  
You can change an existing image to an updated version.
-   **[Upload one or more images](../task/upload-multiple-images.md)**  
You can upload one image or multiple images at one time.
-   **[Restrict file extensions](../task/restrict-file-extensions.md)**  
Use the glide.ui.strict\_content\_types to restrict the image file extensions that appear in the UI.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)


---
title: Upload one or more images
description: You can upload one image or multiple images at one time.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Storing images in the database, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Upload one or more images

You can upload one image or multiple images at one time.

## Before you begin

Role required: image\_admin or content\_admin

## Procedure

1.  To upload one image at a time, complete the following steps:

    1.  Navigate to **System UI** &gt; **Images** to see the list of images stored in the database.

    2.  Click **New** to add a new image.

    3.  Complete the form.

        |Field|Input|
        |-----|-----|
        |**Name**|Enter the file name by which to reference the image in HTML.|
        |**Active**|Select the check box to allow the image to be referenced in HTML.|
        |**Category**|Select a category in which to organize the image file.|
        |**Image**|Select **Click to add...** to upload an image. If an image is already uploaded, click **\[Update\]** to upload a new version of the image or **\[Delete\]** to remove the image.|
        |**Format**, **Size bytes**, **Height**, and **Width**|View current image metadata. This information is automatically populated when the image is uploaded.|

2.  To upload multiple images at once, complete the following steps:

    1.  Create a .zip file that contains only [acceptable image file types](../concept/c_StoringImagesInTheDatabase.md#AcceptableImageFileTypes).

        **Note:** The system does not support uploading zip files that contain .bmp images.

    2.  Navigate to **System UI** &gt; **Image Zip Upload**.

    3.  Click **Choose File** then select the file.

    4.  Click **Upload**.

    A message indicates that the files are uploaded to the database, and the images list is sorted by updated date in descending order \(the uploaded images appear first\).

    **Note:**

    -   If the .zip file contains a folder structure, the resulting image names are the path name with underscores in place of the slashes. For example, if the .zip contains `myimages/image1.gif`then the resulting image is named `myimages_image1.gif`.
    -   Image names cannot exceed 100 characters in length, including folder structure. Files with excessively long names are rejected.
    -   Uploads are logged in the system. View system logs to see whether files are uploaded or rejected.

**Parent Topic:**[Storing images in the database](../concept/c_StoringImagesInTheDatabase.md)

**Related topics**  


[Update an existing image](t_UpdatingAnExistingImage.md)

[Restrict file extensions](restrict-file-extensions.md)

[System log](https://www.servicenow.com/docs/access?context=r_SystemLogs&version=australia&pubname=australia-platform-security&ft:locale=en-US)


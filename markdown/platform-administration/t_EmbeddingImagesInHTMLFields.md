---
title: Embed images in the HTML editor
description: You can use the HTML field image picker to embed images into HTML fields, and to add images to the image library.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Extended functions in HTML field editor, Configure the HTML toolbar, Configure a field editor for the HTML field, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Embed images in the HTML editor

You can use the HTML field image picker to embed images into HTML fields, and to add images to the image library.

## Before you begin

Role required: the role necessary to update the record that contains the HTML field. For example, any user with a role can create a knowledge article and embed an image in it.

## About this task

**Note:** Administrators and users with the image\_admin role manage the image library at **System UI** &gt; **Images**. See [Storing images in the database](https://www.servicenow.com/docs/access?context=c_StoringImagesInTheDatabase&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) .

## Procedure

1.  Open the form that contains the HTML field.

2.  Click the position where the image is to appear, or to modify an existing image, click the image.

3.  Click the insert/edit image icon \(![Insert or edit image icon](../image/TinyMCEV4Image.png)\) on the HTML editor toolbar.

4.  In the Insert/Modify image form, enter information in each field.

<table id="table_insert_modify_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Type**

</td><td>

Select the image type.-   **Image Library**: Images stored in the db\_image table. You can reuse images in the image library in multiple locations.
-   **Attachment**: Available in the current record only


</td></tr><tr><td>

**Image**

</td><td>

Begin typing a file name and select an image from the list, or click the reference lookup icon and select an image.To upload a new image, click **New**, click **Choose File**, locate the image, and click **Upload**.

 If you chose the **Attachment** type, click **Choose File**, locate the image, and click **Attach**.

</td></tr><tr><td>

**Tooltip**

</td><td>

Enter alternate text that appears when a user points to the image.

</td></tr><tr><td>

**Alt**

</td><td>

Enter alternate text that can be used to improve accessibility. For example, it could be used with a screen reader. If this field is left blank, it defaults to the text entered in the **Tooltip** field.

</td></tr></tbody>
</table>    **Note:** To resize an embedded image, click the image. The sizing frame appears. Drag a sizing point until the image is the desired size. Corner points adjust the size proportionally. Depending on your browser, you may need to highlight the image before the sizing frame appears.

5.  To provide additional control over the appearance of an image, click **Advanced options**.

    |Field|Description|
    |-----|-----------|
    |**Layout**|Select the image **Alignment** \(default is **Baseline**\) and enter the **Border thickness**.|
    |**Spacing**|Enter the number of **Horizontal** and **Vertical** pixels around the image.|
    |**Size**|Enter the **Width** and **Height** of the image \(in pixels\).|

6.  Click **OK**.

7.  Paste an image into the HTML editor.

    To edit the image, save the entry then select the image. Click the insert/edit image icon and complete the form using the same tables for adding an image.

    Pasted images are saved in the system as attachments.


**Parent Topic:**[Extended functions in HTML field editor](../reference/r_ExtendedFunctions.md)


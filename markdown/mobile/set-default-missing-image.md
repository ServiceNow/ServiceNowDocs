---
title: Configure a placeholder image for missing images in mobile apps
description: You can specify an image on your instance as a placeholder for missing images. This image appears in your mobile apps when a record has an image field with an empty value, such as a user avatar or catalog item. You can select a different image to use for each table on your instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure a placeholder image for missing images in mobile apps

You can specify an image on your instance as a placeholder for missing images. This image appears in your mobile apps when a record has an image field with an empty value, such as a user avatar or catalog item. You can select a different image to use for each table on your instance.

## Before you begin

Role required: admin

## About this task

You configure placeholder images by creating properties on the System Properties \[sys\_properties\] table. The property is table-specific. If you want to define placeholder images for many tables, you must create multiple properties. Multiple tables can use the same image as a placeholder.

## Procedure

1.  Upload an image to your instance to use as a placeholder. For details on uploading images, see [Storing images in the database](https://www.servicenow.com/docs/access?context=c_StoringImagesInTheDatabase&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

2.  To open the system properties list, type `sys_properties.list` in the Application Navigator.

    Some tables already have a placeholder image defined. You can search the system properties table for properties that start with **glide.sg.image.default** to see any existing properties. Creating multiple properties for the same table can cause inconsistent results.

3.  Click **New**.

4.  Use the following information to complete the fields on the system property form.

    |Field|Value|
    |-----|-----|
    |**Name**|Enter `glide.sg.image.default.[tablename]`. Replace `[tablename]` with the name of the table you want this property to apply to. For example to use the Catalog Item table, enter `glide.sg.image.default.sc_cat_item`.|
    |**Type**|Select **String**|
    |**Value**|Enter the name of your image. This value is the same as the **Name** field on the image \[db\_image\] record.|

5.  Click **Update**.


## Example

To set a different default user image, upload an image and then enter its file name as the value for system property **glide.sg.image.default.sys\_user**.

<table id="table_pkq_zvz_1nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.sg.image.default.sys\_user**

</td></tr><tr><td>

Type

</td><td>

string

</td></tr><tr><td>

Value

</td><td>

&lt;`file-name`&gt;**Note:** Match &lt;`file-name`&gt; to the file name of the image that you have uploaded.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)


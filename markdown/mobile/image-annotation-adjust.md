---
title: Turn off image annotation option
description: By default users can edit and annotate images including actions like adding text, drawing, and highlighting areas. This feature is supported for all attachment locations, including: activity stream, functions with type “attachments,” and input form screens with field type “attachment."
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with images and attachments, Mobile app components, Building mobile apps, Mobile Platform]
---

# Turn off image annotation option

By default users can edit and annotate images including actions like adding text, drawing, and highlighting areas. This feature is supported for all attachment locations, including: activity stream, functions with type “attachments,” and input form screens with field type “attachment."

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

2.  Select **New** to create a new mobile property record.

3.  Enter the name `imageAnnotationEnabled` in the **Name** field.

4.  Select **True/False** in the **Type** field.

5.  In the **Value** field, enter `false` to turn off the ability for users to annotate images.

    If the field is empty, the image annotation feature is enabled.

6.  Select the **Active** field if you want this mobile property to be active.

    **Note:** The selections made in the fields **Mobile App Config** and **Mobile Application**, have no effect on the implementation of this parameter.

7.  Select **Submit**.

    |Image annotation button and panel for iOS devices|Image annotation panel for Android devices|
    |-------------------------------------------------|------------------------------------------|
    |![Image annotation button and panel for iOS devices.](../image/image-annotation-ios.png)|![Image annotation button and panel for Android devices.](../image/image-annotation-android.png)|


**Parent Topic:**[Working with images and attachments in mobile](../concept/images-and-attachments.md)


---
title: Storing media locally when taken from ServiceNow mobile apps
description: Provide users with the option to save and retrieve pictures and videos taken with the camera on their mobile app, onto their device. By default, these images are saved for 24 hours on the phone’s local storage. You can set the storage time to be from 1 to 168 hours \(1 week\).
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with images and attachments, Mobile app components, Building mobile apps, Mobile Platform]
---

# Storing media locally when taken from ServiceNow mobile apps

Provide users with the option to save and retrieve pictures and videos taken with the camera on their mobile app, onto their device. By default, these images are saved for 24 hours on the phone’s local storage. You can set the storage time to be from 1 to 168 hours \(1 week\).

## Before you begin

Role required: admin

Users must have the passcode feature enabled on their device. A passcode is a security measure to protect your users’ phone and its data.

## About this task

Media captured using the camera within a ServiceNow mobile app may not upload onto the app successfully. Instead of losing this data, the parameter  **storeFailedAttachmentsLocally ** enables you to reattempt uploading media when an initial upload fails. The parameter **failedAttachmentsRetentionTime** defines for how long the media is saved on your local device.

By default, these images and videos are saved for 24 hours on the phone’s local storage. You can set the storage time to be from 1 to168 hours \(1 week\).

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_properties.list**.

2.  Select  **New**  to create a mobile property record.

3.  Enter the name  `storeFailedAttachmentsLocally`  in the  **Name**  field.

4.  Select  **True/False**  in the **Type ** field.

5.  In the  **Value**  field, enter  **true**  to turn enable users to store media locally on their mobile device.

6.  Select the  **Active**  field if you want this mobile property to be active.

7.  Set the **Mobile App Config** field to who you want to use the mobile property.

8.  Set the **Mobile Applications** to who you want to send the mobile property.

9.  Select **Submit**.

    The Mobile Properties page displays with your recently created property.

10. Select  **New**  to create a mobile property record.

11. Enter the name  `failedAttachmentsRetentionTime` in the  **Name** field.

12. Select  **Integer**  in the  **Type**  field.

13. In the  **Value**  field, enter a number in hours to define for how long attachments are saved locally before being automatically deleted.

    **Note:** You can define a value between 1 – 168 hours \(1 week\).

    -   If the field is empty, the default value is 24 hours.
    -   For this property to be activated, the property **storeFailedAttachmentsLocally** must be set to **true** .Select the Active field if you want this mobile property to be active.
14. Select the  **Active**  field if you want this mobile property to be active.

15. Set the **Mobile App Config** field to who you want to use the mobile property.

16. Set the **Mobile Applications** to who you want to send the mobile property.


**Parent Topic:**[Working with images and attachments in mobile](../concept/images-and-attachments.md)


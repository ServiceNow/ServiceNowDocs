---
title: Configure an activity stream screen for a record screen
description: Configure an activity stream on your form to give your users access to comments, work notes, and attachments relating to the record they are viewing.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an activity stream screen for a record screen

Configure an activity stream on your form to give your users access to comments, work notes, and attachments relating to the record they are viewing.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select the record screen you want to configure with an activity stream.

4.  In the **Record screen segments** section, select **New**.

5.  Select the **Record screen segment** from the Create a record screen segment screen, and then select **Continue**.

6.  In the **Embedded screen** section, select **New**.

7.  Select **Activity stream** from the Create a Screen screen, and then select **Continue**.

8.  Complete the following fields as needed.

<table id="table_l4s_2cr_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your screen. This name appears as a tile in the mobile application.

</td></tr><tr><td>

Description

</td><td>

Additional information about the screen.

</td></tr><tr><td>

Fetch type

</td><td>

Settings that determine when data is loaded in your screen. Select from the following optional fetch types:

 -   **On-demand:** The app sends a network request to load the app only when end users navigate to it.
-   **Background**: The app makes a background network request to load embedded screens or record screen segments.


</td></tr><tr><td>

Dynamic prefetch count

</td><td>

You can change the number of rows loaded with prefetch by changing the value of the Dynamic prefetch count field.

</td></tr><tr><td>

Hide screen name

</td><td>

Option to hide the record's screen name.

</td></tr><tr><td>

Show "Work Note" button

</td><td>

Show/hide the work note button.

</td></tr><tr><td>

Show "Additional comment" button

</td><td>

Show/hide the additional comment button.

</td></tr><tr><td>

Show "Attachment" button

</td><td>

Show/hide the attachment button.

</td></tr><tr><td>

Available offline

</td><td>

Configure whether the activity stream is available when the device is offline.

</td></tr><tr><td>

Table

</td><td>

The table that the activity stream will use. This must match the table used on the parent record screen.

</td></tr><tr><td>

Icon

</td><td>

Icon used to represent your activity stream.

</td></tr></tbody>
</table>9.  Fill in the **Data** section with the table that is used for the activity stream.

10. In the **Icon** section, select an icon for the activity screen.

11. Select **Save**.


## Result

Your record screen includes an **Activity** tab. Your users can tap this tab to view comments, work notes, and attachments relating to the record.

![Activity Stream tab](../image/mobile-activity-stream.png "Stream tab")

The following file types are supported for previewing files:

-   image files — .png, .svg, .webp, .jpg, and .jpeg
-   video files — .mp4, .mov, and .m4v
-   document files — .pdf, .xlsx, .doc, .ppt, .csv, .xls, .txt, and .docx

**Note:**

-   Audio files are not supported.
-   Some of the above file types require an external app to be installed on the device to open the file. For example, Android users can't open .docx files if Microsoft Word isn't installed on their device.
-   Some other file types might work intermittently on iOS and Android devices, but ServiceNow does not support these other file types. ServiceNow only supports the above listed file types on both iOS and Android devices.


---
title: Define attachment sources available to users
description: Control the origin of where images and files are sourced from, including a phone's gallery, camera, or file system. This capability confirms that images can’t be reused and verifies that they aren't AI-generated.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with images and attachments, Mobile app components, Building mobile apps, Mobile Platform]
---

# Define attachment sources available to users

Control the origin of where images and files are sourced from, including a phone's gallery, camera, or file system. This capability confirms that images can’t be reused and verifies that they aren't AI-generated.

## Before you begin

Role required: admin

## About this task

You can limit the origins of attachments to ensure that images are sourced from one or all of the following:

-   On-site via a camera
-   From the user’s phone gallery
-   From the user’s file system

This feature is supported for all attachment locations including: activity stream, functions, and input form screen.

**Note:** This feature is also supported for scripted screens within Mobile App Bridge and the Cabrillo JS module.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the attachment location for where you want to control the origin of the attachment source.

<table id="choicetable_odj_n5y_zdc"><thead><tr><th align="left" id="d91036e122">

Attachment location

</th><th align="left" id="d91036e125">

Procedure

</th></tr></thead><tbody><tr><td id="d91036e131">

**Function**

</td><td>

1.  Select **Functions** from the menu and then select **New**. Alternatively, select an existing function record.
2.  Select **Upload attachment** in the **Type** field of the Properties section.
3.  Select **New** in the **Buttons attribute** section. The Button attribute record opens.
4.  Leave the **Button** field with the default name.
5.  Select **hidden\_attachment\_sources** from the **Name** field menu.
6.  Enter values in the **Value** field from where you don’t want images sourced from.

Values can be `camera`, `files`, or `gallery`, or any combination separated by commas. If this field is empty, then images and files can be sourced from all locations.

7.  Select **Save**.


</td></tr><tr><td id="d91036e209">

**Activity stream**

</td><td>

1.  Select the  **All mobile records** option from the menu.
2.  From the  **Record type**  field, select Activity stream screen \[sys\_sg\_activity\_stream\_screen\].
3.  Select **New** or an existing activity stream record. The activity stream screen opens.
4.  Select **Choose** in the Hidden attachment sources area.
5.  Select the attachment sources that you want to hide.
6.  Select **Apply**.
7.  Select **Save**.


</td></tr><tr><td id="d91036e261">

**Input form screen**

</td><td>

1.  Select the  **Screens ** category, and then select  **New**.
2.  Select the  **Input form ** option in the Create a screen page, and then select  **Continue**.
3.  Select **New** in the Inputs section.
4.  Enter a **Name** and **Label** in the Properties section.
5.  Select `Attachment` from the **Input type** field in the **Settings** section.
6.  Select **New** in the Input attributes section. The Input record opens.
7.  Select **HiddenAttachmentSources** from the Name field.
8.  Select either camera, files, or gallery, from the **Value** field. The value you select is where you don’t want images sourced from.

**Note:** To prevent images and files from more than one source, add additional **HiddenAttachmentSources** attributes after you save the attribute you're currently configuring.

9.  Leave the **Input** field value with its default entry.
10. Select **Save**.


</td></tr></tbody>
</table>
**Parent Topic:**[Working with images and attachments in mobile](../concept/images-and-attachments.md)


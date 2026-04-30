---
title: Define attachment sources available to users
description: Control the origin of where images and files are sourced from, including a phone's gallery, camera, or file system. This capability confirms that images can’t be reused and verifies that they aren't AI-generated.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Working with images and attachments in mobile, Mobile app components, Building mobile apps, Mobile Platform]
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

This feature is supported for all attachment locations including: activity stream, functions, and input form screen. Within the input form screen, attachments can be added from the following areas, as shown in the table.

**Note:** You can source image attachments from the camera and the gallery from both these areas. You cannot source videos or record videos. Only from the input action menu can you source images from the file system.

|Adding attachment types within an individual input value|Adding attachment types as part of an input action|
|--------------------------------------------------------|--------------------------------------------------|
|![Adding attachments next to an input value.](../image/ifs-attach-input-value.png)|![Adding attachments next to an input action.](../image/ifs-attach-input-action.png)|

**Note:** This feature is also supported for scripted screens within Mobile App Bridge and the Cabrillo JS module.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the attachment location for where you want to control the origin of the attachment source.

<table id="choicetable_odj_n5y_zdc"><thead><tr><th align="left" id="d85018e159">

Attachment location

</th><th align="left" id="d85018e162">

Procedure

</th></tr></thead><tbody><tr><td id="d85018e168">

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


</td></tr><tr><td id="d85018e246">

**Activity stream**

</td><td>

1.  Select the  **All mobile records** option from the menu.
2.  From the  **Record type**  field, select Activity stream screen \[sys\_sg\_activity\_stream\_screen\].
3.  Select **New** or an existing activity stream record. The activity stream screen opens.
4.  Select **Choose** in the Hidden attachment sources area.
5.  Select the attachment sources that you want to hide.
6.  Select **Apply**.
7.  Select **Save**.


</td></tr><tr><td id="d85018e298">

**Input form screen \(attachment type\)**

</td><td>

1.  Select the  **Screens ** category.
2.  Select an existing input form screen.

**Note:** If you need to create a new input form screen, follow the instructions starting from the topic [Configure an input form screen](parameter-screen-config.md).

3.  Select **New** in the Inputs area. For an explanation of the fields, refer to [Configure input form screen inputs](param-screen-config-inputs.md).
4.  Enter a **Name** and a **Label** for your new input.
5.  Select `Attachment` in the **Input type** field.
6.  Select **New** in the **Input attributes** area. The Input form action attribute record opens.
7.  Select **HiddenAttachmentSources** from the **Name** field.
8.  Select either `camera`, `files`, or `gallery`, from the **Value** field. The value you select is where you don’t want images sourced from.

**Note:** To prevent images and files from more than one source, add additional **HiddenAttachmentSources** attributes after you save the attribute you're currently configuring.

9.  Select **Save**.


</td></tr><tr><td id="d85018e404">

**Input form screen \(attachment input action\)**

</td><td>

1.  Select the  **Screens ** category.
2.  Select an existing input form screen.

**Note:** If you need to create a new input form screen, follow the instructions starting from the topic [Configure an input form screen](parameter-screen-config.md).

3.  Select **New** or open an existing record in the **Actions** area.

**Note:** For an explanation of the fields, refer to [Configure input form actions in an input form screen](input-actions-configure.md).

4.  Select `Input action` in the **Input type** field.
5.  Select **New** in the **Action attributes** area. The Input form action attribute record opens.
6.  Select **HiddenAttachmentSources** from the **Name** field.
7.  Select either `camera` or `gallery`, from the **Value** field. The value you select is where you don’t want images sourced from.

**Note:** To prevent images and files from more than one source, add additional **HiddenAttachmentSources** attributes after you save the attribute you're currently configuring.

8.  Select **Save**.


</td></tr></tbody>
</table>

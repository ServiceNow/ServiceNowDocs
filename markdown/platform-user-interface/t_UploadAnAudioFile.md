---
title: Manage audio files
description: You can upload and store .mp3 or .ogg audio files. Once uploaded, you can reference audio files using HTML.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Manage audio files

You can upload and store `.mp3` or `.ogg` audio files. Once uploaded, you can reference audio files using HTML.

## Before you begin

Role required: image\_admin

## About this task

The Database Storage for Audio Files \(com.glide.db\_audio\) feature must be activated to store audio files. The plugin is activated by default on new instances. For upgraded instances, you can activate the plugin if you have the admin role. For more information on activating a plugin, see Activate a plugin.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Audio Files**.

2.  Click **New**.

3.  Enter a **Name** for the audio file, including the file extension.

4.  Add the **Audio** file.

5.  Save the record.

6.  Complete the following steps to reference audio files using HTML.

    1.  Use the `<audio>` HTML tag and set the **src** attribute to the name of the file as set by the **Name** field of the Audio record.

    2.  Use the **controls** attribute to display the audio controls.

        Use the following HTML.

        ```
        <audio src="Beep.mp3" title="Beep" control="control"/>
        ```


**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)


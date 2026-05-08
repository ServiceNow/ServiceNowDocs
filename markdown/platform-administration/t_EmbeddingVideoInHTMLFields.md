---
title: Embed videos in the HTML editor
description: You can insert videos into HTML fields. You can also add videos to the video library using the HTML Insert/Modify Video form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Extended functions in HTML field editor, Configure the HTML toolbar, Configure a field editor for the HTML field, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Embed videos in the HTML editor

You can insert videos into HTML fields. You can also add videos to the video library using the HTML Insert/Modify Video form.

## Before you begin

**Note:** The Videos \[db\_video\] table is a public table that does not have any security restrictions. Unauthenticated users have full access to videos uploaded to the db\_video table.

Role required: The role necessary to update the record that contains the HTML field. For example, any user with a role can create a knowledge article and embed a video in it.

## About this task

The following file formats are supported in the base system.

-   MPEG-4 video `.mp4`
-   WebM Video `.webm`

The larger the file size, the longer it takes to download before the video starts. To reduce file size, you can reduce the bit rate, but doing so reduces the quality of the video. The following bit rates optimize download speed and video quality:

|Video resolution|Recommended bitrate|
|----------------|-------------------|
|Standard definition \(480p\)|1.5–2.5 megabits per second \(mbps\)|
|High definition \(720p\)|3–5 mbps|
|High definition \(1080p\)|6–8 mbps|

**Note:** For the best viewing experience the following specifications are suggested:

|Type|Definition|
|----|----------|
|Size|20MB|
|Bit rate|320KBPS|
|Resolution|480\*320|

Internet Explorer and Safari have difficulty streaming videos uploaded to the database. Attach a file rather than embedding if you intend to use one of these browsers or an unsupported file type. For more information on attaching files, see Add and manage attachments.

**Note:** Administrators and users with the image\_admin role can manage the video library at **System UI** &gt; **Videos**.

## Procedure

1.  Open the form that contains the HTML field.

2.  Click the position where the video is to appear, or to modify an existing video, click the video.

3.  Click the insert/edit video icon \(![Insert or edit video](../image/TinyMCEV4Video.png)\) on the HTML editor toolbar.

4.  Enter information in each field.

<table id="table_insert_edit_embedded_media_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select the video type.-   **Video Library**: List of videos stored in the db\_video table. You can reuse it.
-   **URL**: from an external source
-   **Attachment**: available in the current record only
 For an attachment or video library file, select a video from the list or click **New**. For an external URL, enter the URL.

</td></tr><tr><td>

Size

</td><td>

Enter the **Width** and **Height** of the video in pixels.

</td></tr></tbody>
</table>5.  Click **OK**.



---
title: Define video file types for HTML fields
description: You can define the types of video files that can be added to HTML fields.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Extended functions in HTML field editor, Configure the HTML toolbar, Configure a field editor for the HTML field, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Define video file types for HTML fields

You can define the types of video files that can be added to HTML fields.

## Before you begin

Role required: image\_admin

## About this task

Users can add videos to HTML fields. By default, users can add one of the following types of videos to HTML fields: `.mp4`, `.webm`, and `.swf` video file types. You can inactivate video types that you do not want to allow users to add, or add new video types. `.swf` files are only minimally supported. `.mp4` files might be limited by browser type.

**Note:** By default, the HTML Sanitizer removes videos from HTML fields. To allow video file types, see [Embed videos in the HTML editor](t_EmbeddingVideoInHTMLFields.md)

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Embed Object Types**.

2.  To deactivate a video type, set the **Active** field to **false**.

3.  To add an additional video type, click **New** and complete the form.

    **Note:** If you specify values for the **Codebase** or **Pluginspage** fields, which instruct the browser where to get the plugin, point to `https` pages to avoid warnings from Internet Explorer about unsecure content on the page.



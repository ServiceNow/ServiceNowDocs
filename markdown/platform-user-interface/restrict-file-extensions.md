---
title: Restrict file extensions
description: Use the glide.ui.strict\_content\_types to restrict the image file extensions that appear in the UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/restrict-file-extensions.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Storing images in the database, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Restrict file extensions

Use the glide.ui.strict\_content\_types to restrict the image file extensions that appear in the UI.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the Navigation filter.

2.  Verify that the property does not exist by searching for the property name.

3.  Click **New**.

4.  Complete the system property using the following table.

    |Field|Description|
    |-----|-----------|
    |Name|glide.ui.strict\_content\_types|
    |Type|string|
    |Value|Comma-separated list of acceptable image file names. Use any of the following file types: ico,gif,png,jpg,jpeg,bmp,js,css,htm,html,ogg,mp3,eot,woff,woff2,svg,ttf,swf,cur,map|

    **Note:** Any files that use a file extension that is not included in the list of values appear broken in the UI.


**Parent Topic:**[Storing images in the database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_StoringImagesInTheDatabase.md)

**Related topics**  


[Update an existing image]()

[Upload one or more images]()


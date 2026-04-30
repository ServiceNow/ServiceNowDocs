---
title: Define a frame in a style sheet
description: Add style definitions for any custom frame UI macro you create.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Format a frame, Style in Content Management, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Define a frame in a style sheet

Add style definitions for any custom frame UI macro you create.

## Before you begin

Role required: content\_admin or admin

## About this task

Each frame has its own class name.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Design** &gt; **Style Sheets**.

2.  Select a style sheet to contain the frame definition.

    Base system themes use a separate **Frames** style sheet.

3.  Add the following code, substituting the desired frame name and style:

    ```
    div.FRAMENAME{border:STYLE;}
    ```

4.  Click **Update**.


**Parent Topic:**[Format a frame](t_Frame.md)


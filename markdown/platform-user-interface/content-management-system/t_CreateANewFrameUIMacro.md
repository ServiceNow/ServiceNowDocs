---
title: Create a frame UI macro
description: Copy an existing frame UI macro to display content in a custom frame.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Format a frame, Style in Content Management, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Create a frame UI macro

Copy an existing frame UI macro to display content in a custom frame.

## Before you begin

Role required: content\_admin or admin

## About this task

Create a custom frame UI macro if you want to control the style of the frame with your own style sheet definitions.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Design** &gt; **Frames** and select one of the existing frame UI macros.

2.  Change the name to match the FRAMENAME you used in the style sheet.

3.  Right-click the header bar and select **Insert and Stay**.

4.  Update the frame name in the XML field as shown:

    ```
    <div class="FRAMENAME">
    ```

5.  Click **Submit**.


## What to do next

-   In any content block form, select the UI macro.
-   Define the frame in a style sheet.

**Parent Topic:**[Format a frame](t_Frame.md)

**Related topics**  


[Content blocks](../concept/c_ContentBlocks.md)


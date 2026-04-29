---
title: Format a frame
description: Frames provide a way to manage decorative containers for content blocks and any other elements within the site. For example, one frame can be a container, made of div or span tags, that is styled with rounded corners.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Style in Content Management, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Format a frame

Frames provide a way to manage decorative containers for content blocks and any other elements within the site. For example, one frame can be a container, made of div or span tags, that is styled with rounded corners.

## Before you begin

Role required: content\_admin or admin

## About this task

Individual content blocks use a frame UI macro to define the frames. When viewing a content block form, the **Frame** field offers a choice between the different frame UI macros. The frame UI macro does not, however, have the definition for the frame within its Jelly script. Instead, it references a particular frame as defined in a style sheet.

Configuring a new frame is a two-step process.

## Procedure

1.  Define the frame in a style sheet.

2.  Create the frame UI macro to invoke the frame definition.


-   **[Define a frame in a style sheet](t_DefineTheFrameInAStyleSheet.md)**  
Add style definitions for any custom frame UI macro you create.
-   **[Create a frame UI macro](t_CreateANewFrameUIMacro.md)**  
Copy an existing frame UI macro to display content in a custom frame.

**Parent Topic:**[Style in Content Management](../concept/c_StyleInContentManagement.md)


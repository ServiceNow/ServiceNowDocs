---
title: Configure Activity stream
description: Set up the options of how agents can interact with Activity stream to make their job easier.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering Activity stream for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure Activity stream

Set up the options of how agents can interact with Activity stream to make their job easier.

## Before you begin

Role required: admin

## About this task

**Note:**

-   Once you use system properties to enable these options, the sliders in the configuration menu appear.
-   Journal entries for a record generated via a script are inserted into the sys\_journal\_field table and reference the applicable document. If entries don't appear in the Activity stream of the record, set the workflow to false.

Activity stream enables agents to communicate with requesters and make internal notes about the work done on a record. Internal notes are only visible to fellow agents. External comments are visible to agents and requesters.

In Activity stream, agents can embed knowledge articles, import solutions from Agent Assist, and ask requesters for more information.

![Activity stream](../image/activity-stream-washington.png)

You can set system properties that give agents the option of using a:

-   Rich text editor.

    The rich text editor includes the formatting icons for bold, italics, underlining, font, and so forth, as shown in the following image.

-   Single box or separate text boxes to enter internal and external comments.

## Procedure

1.  In the Filter Navigator, enter `sys_properties.list`.

    The list of system properties displays.

2.  To give agents the stacked view option \(separate boxes for internal and external communications\), search for and set the **glide.ui.activity.journal.stacked** property to **true** and ensure that no mandatory fields are present in the Activity stream.

    **Note:** Mandatory fields in the Activity stream prevent the stacked view option from displaying.

3.  To give agents the option of using a rich text editor, search for and set the **glide.ui.journal.use\_html** property to **true** .



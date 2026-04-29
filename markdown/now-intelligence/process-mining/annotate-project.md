---
title: Adding notes to a project
description: Add, view, and remove notes for a project to help manage tasks, ideas, and insights. Tag others to notify them to view a note.Review notes posted for a project.Add a note to a project to review later.Update a project note.Delete a project note once you resolve or want to remove it.Review snapshots of process maps posted for a project.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Analyzing and getting process insights, Use, Process Mining, Platform Analytics]
---

# Adding notes to a project

Add, view, and remove notes for a project to help manage tasks, ideas, and insights. Tag others to notify them to view a note.

From the project overview panel, you can add a note or see a list of notes associated with a project.

**Note:** To add or delete notes, you must have the sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin role.

**Parent Topic:**[Analyzing and getting process insights](analyze-get-process-insights.md)

## View a note

Review notes posted for a project.

### Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

Notes can be viewed from a main or linked process. A note can be edited or deleted from the process map in which it was created.

**Note:** Notes do not display in comparison view.

### Procedure

1.  Select the project to view a note from.

2.  From the project view, select the Notes icon \(![Notes icon](../image/notes-icon.png)\) to open the Notes panel.

3.  From the **Show** list, select whether to show one or more of these options:

    -   **Current Model Notes** - Shows notes created on the process you're currently viewing.
    -   **Main Model Notes** - From a linked process, shows notes created on the main process.
    -   **All Linked Notes** - Shows all notes created on the main and all linked processes.

## Add a note

Add a note to a project to review later.

### Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

### Procedure

1.  Select the project to add a note to.

2.  From the project view, select the Notes \(![Notes icon](../image/notes-icon.png)\) icon to open the Notes panel.

3.  Select **New note** and type a note into the box.

    You can get someone's attention in a note by mentioning them. For each user you want to notify, add an @mention containing the user's name. When the note saves, users receive an email notification.

4.  Check **Attach snapshot** to add a snapshot of the current process map view.

    Scroll the view to include the area you want to snapshot. To add a larger or smaller view of the process map image, zoom the map in the main screen before adding it as a snapshot.

    -   Adding snapshots can be helpful for restoring settings at a later time. For example, when revisiting a note, you can preview an attached snapshot and see the configured settings at the time the snapshot was added. You will have a picture of how you can replicate a project to the same state.
    -   If viewing a linked process, a snapshot of both the main and linked projects add to the note.
5.  Select **Post**.


## Edit a note

Update a project note.

### Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

### About this task

A note can be edited from the main or linked process in which it was created.

### Procedure

1.  From the project view, select the Notes icon \(![Notes icon](../image/notes-icon.png)\).

2.  From the Notes panel, select the context menu of a note, then select **Edit**.

    ![Edit a note](../image/edit-note.png)

3.  After you edit the note, select **Update**.

    The update shows in the refreshed list.


## Delete a note

Delete a project note once you resolve or want to remove it.

### Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

### About this task

A note can be deleted from the main or linked process in which it was created. Deleting a note doesn't destroy it, but only removes it from the project view. A note's record remains accessible from the Notes tab of the Related lists section.

### Procedure

1.  From the project view, select the Notes icon \(![Notes icon](../image/notes-icon.png)\).

2.  From the Notes panel, select the context menu of a note, then select **Delete**.

3.  Select **Yes** to confirm.

    The note is removed from the refreshed list.


## View a snapshot

Review snapshots of process maps posted for a project.

### Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

### About this task

Snapshots are helpful for seeing a process map and its configuration settings at the time the snapshot was added. You can view snapshots from and for main and linked process maps.

**Note:** This task explains how to view a snapshot from the process map in which the note was created. The **Preview** option is not available for notes created in another model.

### Procedure

1.  Select the project to view a snapshot from.

2.  From the project view, select the Notes icon \(![Notes icon](../image/notes-icon.png)\) to open the Notes panel.

3.  Select the **Preview** button on a note.

    The snapshot displays the preview in the main map window, along with its model's statistics.

    ![Example snapshot image](../image/snapshot.png)

    -   On the preview map, you can adjust view of the primary and secondary metrics, select activities and connections to view, and zoom in and out. Viewing filters and routes is not possible from a snapshot preview, however.
    -   Snapshots cannot be updated.
4.  Once done viewing the snapshot preview, select **Stop Preview** to return to the previous map and filter tools, or select to preview a different snapshot.



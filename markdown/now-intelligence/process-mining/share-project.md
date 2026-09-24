---
title: Share a Process Mining project
description: Share a project so that other have access to the data, and enable a process owner to analyze further.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/share-project.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Share a Process Mining project

Share a project so that other have access to the data, and enable a process owner to analyze further.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## About this task

You can share a project in two ways:

-   Adding users to the share list
-   Sharing a link of the project with the users

When you share a Process Mining project, you choose one of two permission levels for each person: Can view or Can edit. These are mutually exclusive; selecting one automatically deselects the other.

|Action|Can view|Can edit|
|------|--------|--------|
|Explore the analyst workbench, run on-the-fly mining jobs|Yes|Yes|
|Edit project fields \(name, description, configuration\)|No|Yes|
|Run a full or sample mine|No|Yes|
|Delete the project|No|Yes, unless a mining job is currently running|
|Share the project with others|No|No|

Granting someone **Can edit** access only works if they have the `sn_process_mining_analyst` role or higher. If they don't, they're treated as **Can view** regardless of the permission you assigned them.

Process Mining admins and power users always have the same level of access as the project owner, regardless of how the project was shared with them.

This permission model doesn't apply to content pack projects or templates. Those remain governed by their own read-only rules.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  From any tab on the Process Mining Workspace, select the **Share** button.

    Alternatively, you can share a project from the Overview page after creating a project.

    \[Omitted image "po-share-button.png"\] Alt text: Share button on Process Mining Workspace

    The Share project window is displayed.

    1.  Select **Copy Link** button if you want to share a link with a user.

        The permanent link is copied to your clipboard. This link does not expire when the project is remined by the owner. However, inactive versions get cleaned up after 90 days of inactivity. You can share the link with any user who has access to the table.

    2.  Enter any user, role, or group that you want to share the project with, and select the exact name from the drop-down list if you want to add the user to the share list.

    3.  Select **Add**.

    4.  From the dropdown next to their name, select a permission level.

        -   **Can view**: Selected by default
        -   **Can edit**: Can edit the project
        -   **Remove**: Removes this user's access
        \[Omitted image "share-project.png"\] Alt text: Permission level in sharing a project

    5.  Select **Confirm**.

        On this window, you see all the users, roles, and groups that the project is shared with. This list gets filtered by the value that you select in the **Audience type** list \(**All**, **Users**, **Roles**, or **Groups**\).

    6.  To remove any user, group, or role from giving the access to the project, from the **Actions** list for that user, group, or role select **Remove**.


**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/use-process-mining.md)


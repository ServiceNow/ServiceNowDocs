---
title: Create a Configurable Workspace experience
description: Create a Configurable Workspace experience from scratch using UI Builder and the Workspace App Shell.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Configure, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a Configurable Workspace experience

Create a Configurable Workspace experience from scratch using UI Builder and the Workspace App Shell.

## Before you begin

Role required: ui\_builder\_admin, admin

**Note:**

ServiceNow offers prebuilt Configurable Workspace experiences to target specific users and issues like CSM Configurable Workspace.

These prebuilt workspaces can be updated and modified in UI Builder instead of creating an experience from scratch.

For a list of prebuilt workspaces ServiceNow offers, see [List of workspaces](../../workspace/concept/list-of-workspaces.md).

To update an existing Configurable Workspace experience, see [Open a Configurable Workspace experience](../../workspace/task/open-your-configurable-workspace-experience-in-ui-builder.md)

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Create an experience by selecting **Create** &gt; **Experience**.

    A modal opens with fields to create an experience.

3.  Complete the following fields in the modal.

    -   **Name**

        Enter a name for the experience.

    -   **App shell UI**

        Select the **Workspace App Shell** from the menu.

    -   **URL path**

        The URL path is created automatically based on the experience name.

    -   **Landing path**

        The landing path is a prefix used to reach the experience home page. It appears automatically as `home`.

    -   **Roles**

        Define the roles that can access the experience. If you leave this field empty, the experience is open to all logged-in users by default.

4.  Select **Create**.

    A modal opens that confirms the experience is created.

5.  Select **Open your experience**.


## Result

Your Configurable Workspace experience opens in UI Builder.

![Configurable Workspace experience in UI Builder](../../workspace/image/configurable-workspace-experience-uib.png)

## What to do next

[Create a Configurable Workspace page](create-configurable-workspace-page-uib.md)


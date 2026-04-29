---
title: Upgrade a form action layout group
description: Upgrade an existing form action layout group to manage all actions in a single list and customize the order, label, and icons for declarative actions without altering the base action.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Upgrade a form action layout group

Upgrade an existing form action layout group to manage all actions in a single list and customize the order, label, and icons for declarative actions without altering the base action.

## Before you begin

Role required: admin

## About this task

A form action layout group enables you to group multiple related actions into a single menu or split button.

Existing UX Form Actions Layout Group records store actions in a glide list field, which creates the following limitations:

-   Changing the Order field for an action affects all layouts where the action appears.
-   Changing the Label field for an action affects all layouts where the action appears.
-   Adding actions from different scopes requires updates to group records and creates dependency bottlenecks.

You can upgrade a UX Form Actions Layout Group record to manage all actions in the group through a many-to-many \(M2M\) related list instead.

Upgrading a UX Form Actions Layout Group record provides the following capabilities:

-   Change the Order field for an action without affecting the base action.
-   Change the Label field for an action without affecting the base action.
-   Change the icon for an action without affecting the base action.
-   Add actions from different scopes without affecting the base action.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **UX Form Action Layout Groups**.

2.  From the UX Form Actions Layout Groups list, select a group.

    A UX Form Actions Layout Group record opens.

3.  Select **Upgrade Group**.

    **Important:** This upgrade can't be undone.

    The previous Actions glide list field is removed and replaced with the Form actions in group related list. The order and labels for actions in the group will be preserved.

4.  Select the **Form actions in group** related list.

    From this related list, you can change the visibility, order, label, and icons for the actions within this group without altering the base action.



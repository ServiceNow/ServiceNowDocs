---
title: Hide a global form action from a page layout
description: Configure a global form action to exclude a specified page or experience.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage action visibility, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Hide a global form action from a page layout

Configure a global form action to exclude a specified page or experience.

## Before you begin

Add a UX Form Actions Layout to a workspace page in UI Builder. The UX Form Action Layout record configured on the workspace page must contain the form action you want to hide from the page. For instructions, see [Configure an action layout for a workspace page](../task/configure-da-action-layout.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Form Actions**.

2.  Select the form action you want to hide.

    An Action Assignment record opens.

3.  Select the **Form Action Layouts** related list tab.

4.  Select the layout configured on the workspace page.

    The scope must match the application of the record.

    **Important:** Any UX Form Actions Layout records created in Washington DC or later are unified automatically. You will need to manually associate any form actions created in releases earlier than Washington DC.

    A UX Form Actions Layout record opens.

5.  Select the **UX Form Action Layout Items** related list tab.

6.  Locate the form action you want to hide and change the Active field to **false**.

7.  Select **Update**.


## Result

When the UX Form Actions Layout is configured on a workspace page in UI Builder, only enabled actions will appear on the page.


---
title: Restrict a global list action to a workspace page
description: Configure a global list action to display only on a specified workspace page.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-21"
reading_time_minutes: 1
breadcrumb: [Manage action visibility, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Restrict a global list action to a workspace page

Configure a global list action to display only on a specified workspace page.

## Before you begin

Configure an action configuration record for a list action, and copy the action configuration record's sys\_id. For instructions, see [Configure an action configuration record](config-da-action-configuration.md).

Role required: admin

## About this task

List actions are global and appear in all Configurable Workspace experiences by default. The action assignment record for a list action has a **Experience Restricted** field that is set to false by default.

When the **Experience Restricted** field is set to false, the list action appears on all list pages regardless of the Configurable Workspace experience.

When the **Experience Restricted** field is set to true, the list action doesn't appear in any list page across any Configurable Workspace experience. To display the list action, the workspace page in UI Builder must be configured with the action configuration record tied to the list action.

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **List Actions**.

2.  Select the list action you want to restrict.

    An Action Assignment record opens.

3.  Select the **Experience Restricted** checkbox to set it to true.

4.  Select **Update**.

5.  Open your workspace experience in UI Builder.

    For instructions, see Open a Configurable Workspace experience in UI Builder.

6.  Select or create a list page.

    For instructions on creating a workspace page in UI Builder, see [Create a Configurable Workspace page](create-configurable-workspace-page-uib.md).

7.  From the Content tree, select the **Record List Header**.

8.  Select the **Configure** tab and expand the **Declarative actions** section.

9.  In the Action configurations for declarative actions property, paste the sys\_id for the action configuration record tied to the list action you want to display.


## Result

The global list action displays only on the workspace page configured with the action configuration record's sys\_id.


---
title: Configure the Front-line case page action bar
description: Configure the action bar on the Front-line case page to include actions from other plugins.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure the Front-line case page action bar

Configure the action bar on the Front-line case page to include actions from other plugins.

## Before you begin

Role required: admin

## About this task

The Front-line case page supports actions from the following Customer Service Management and CSM Configurable workspace plugins:

-   Customer Service \(com.sn\_customerservice\)
-   CSM/FSM Configurable WS Foundation \(com.snc.uib.cwf\_workspace\)
-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   CSM Workspace \(com.snc.agent\_workspace.csm
-   Major Issue Management \(com.sn\_majorissue\_mgt\)
-   Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Customer Service with Request Management plugin \(com.sn\_cs\_sm\_request\)
-   Time Recording for Customer Service \(com.snc.csm\_time\_recording\)
-   Omni-Experience Standard Feature Set

If you are using any additional plugins, use the steps in this task to add the actions from those plugins to the Front-line case page action bar. You can add actions in the following ways:

-   Add actions to an existing layout group \(step 2\).
-   Create a new layout group and add actions to that group \(steps 3 and 4\).
-   Add actions directly to the action bar \(step 5\).

## Procedure

1.  Verify that the UI action or declarative action has a corresponding record in the UX Form Actions table \(sys\_ux\_form\_action\).

    1.  Enter **sys\_ux\_form\_action.list** in the application navigator and press Enter.

    2.  Search for the desired form action in the UX Form Actions list.

    3.  Create a form action record if it does not exist.

2.  Add the action to an existing layout group.

    You can create a new layout group and add the action to that group \(see step 3\). By default, the Front-line case page supports three groups: Compose, Create, and Manage.

    1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Form Action Layout Groups** and select a group.

    2.  Select the lock icon next to the **Actions** field, add the desired action from the Available UX Form Actions list, and select **Save**.

3.  Create a new layout group.

    1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Form Action Layout Groups** and select **New**.

    2.  Enter a name for the layout group in the **Name** field.

    3.  Select the lock icon next to the **Actions** field, add the desired action from the Available UX Form Actions list, and select **Save**.

    Because this is a new group, you need to add it to the Front-line case page layout \(see step 4\).

4.  If you created a new layout group in step 3, add the group to the Front-line case page layout.

    1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Form Action Layouts**.

    2.  Select the Front-line Case Actions layout.

    3.  Select **New** in the UX Form Action Layout Items related list.

    4.  On the new record page, set **Item Type** to Group and set **Group** to the group created in step 3.

    5.  Fill in the rest of the fields on the form and select **Save**.

5.  To add an action directly on the action bar:

    1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Form Action Layouts**.

    2.  Select the Front-line Case Actions layout.

    3.  Select **New** in the UX Form Action Layout Items related list.

    4.  On the new record page, set **Item Type** to Action and set **Action** to the desired UX Form Action.

    5.  Fill in the rest of the fields on the form and select **Save**.



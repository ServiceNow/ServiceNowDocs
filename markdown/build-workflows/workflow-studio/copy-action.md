---
title: Copy an action
description: Copy an action to give it a new name and move it to another application scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/copy-action.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an action in Workflow Studio, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Copy an action

Copy an action to give it a new name and move it to another application scope.

## Before you begin

Role required: action\_designer or admin

## About this task

You can copy a custom action that you created to give it a new name or move it to another application scope. The new action has the same action properties, inputs, steps, and outputs as the source action.

You can't copy the default actions created by ServiceNow, Inc., nor can you copy actions that have a protection policy. You must have write access to an action to copy it.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Select the action that you want to copy.

4.  Click the more actions icon \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions menu\) and select **Copy action**.

    **Note:** If the **Copy action** option is not visible, then you don't have permission to copy the action. This could be because the action has a protection policy or because you lack the necessary user role or developer permissions.

5.  In **New action name**, enter a unique name you want the copied action to have.

    \[Omitted image "example-copy-action-modal.png"\] Alt text: Copying a get notifications details action.

6.  From **Application**, select the application scope where you want to copy the action.

7.  Select **Copy**.


## Result

\[Omitted image "example-copy-action-result.png"\] Alt text: New copied action.

Workflow Studio opens the new action.

**Parent Topic:**[Create an action in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-action.md)


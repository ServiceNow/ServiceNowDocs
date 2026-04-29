---
title: Save as you go flows
description: Save flows, subflows, and actions automatically as you work on them.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Save as you go flows

Save flows, subflows, and actions automatically as you work on them.

As of the Zurich release, Workflow Studio no longer displays a Save button in the header of the editor canvas while you edit a flow, subflow, or action. Rather than manually saving, Workflow Studio automatically saves your work as you make changes.

## When Workflow Studio automatically saves flows

While editing a flow, your changes are automatically saved each time you perform one of these operations.

-   Activate a flow.
-   Add a flow step.
-   Deactivate a flow.
-   Delete a flow step.
-   Move a flow step to a new position.
-   Select a data pill from the Data pane or the data pill picker.
-   Select the Done option to finish configuring a flow step.
-   Select either the Undo last action or Redo last action options.

## Manually saving a flow

You can manually save a flow at any time with the Force save option available from the More actions menu. This option provides a backup in case the automatic save isn’t working for some reason. The option to save a flow requires that you first have edit rights to the flow.

![More actions menu showing the Force save option highlighted.](../../workflow-studio/images/force-save-option.png "Force save option")

## Last saved indicator

Workflow Studio displays the last saved icon after saving a flow ![Auto save icon](../../workflow-studio/images/icon-last-saved.png). Select or point to the last saved icon to display the duration or date since the flow was last saved.

![Pop-up displaying, "Last saved: 3 minutes ago."](../../workflow-studio/images/example-last-saved.png "Example last saved date")

## Read-only flow interactions

You can't save a flow that you don't have edit rights to. Make sure to save your work while you’re editing a flow. To avoid losing changes to the editing time-out value, perform any of the operations that trigger automatically saving the flow. For more information about when flows are in a read-only state, see [Default read-only flows](default-read-only-flows.md).

-   **[Restore save as you go functionality](../task/restore-save-as-you-go-functionality.md)**  
Restore save as you go functionality that was disabled in the Washington DC release.

**Parent Topic:**[Building flows](flows.md)


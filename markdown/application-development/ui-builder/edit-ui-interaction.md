---
title: Edit an existing UI interaction
description: Edit or modify an existing UI interaction by inserting new steps, swapping or deleting events, removing steps, or updating step configurations in the diagram editor.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-04-10"
reading_time_minutes: 3
breadcrumb: [UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Edit an existing UI interaction

Edit or modify an existing UI interaction by inserting new steps, swapping or deleting events, removing steps, or updating step configurations in the diagram editor.

## Before you begin

Role required: ui\_builder\_admin

## About this task

When you create a UI interaction, you can return to the diagram editor to modify its flow. You can insert steps before or after existing steps, swap the outgoing event that connects one step to the next, delete events or steps you no longer need, update step configurations, and add or remove branches.

**Important:** Before editing a UI interaction that is already in use, check the Settings and Usage pages to understand where the interaction is triggered. Consider duplicating the interaction before making changes to avoid unintended impacts to active pages or declarative actions. For information on duplicating an interaction, see [Duplicate a UI interaction](duplicate-ui-interaction.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **UI interactions** tab.

3.  In the search field, enter the name of the interaction you want to edit.

    ![UI interactions list with search field highlighted.](../image/uib-uii-search.png "UI interactions list")

4.  Select the interaction from the search results.

    The diagram editor opens with the existing flow displayed on the canvas.

5.  Choose how you want to edit the interaction.

<table id="table_zzy_wfw_w3c"><thead><tr><th>

Editing scenario

</th><th>

Steps

</th><th>

UI depiction

</th></tr></thead><tbody><tr><td>

Insert a step before or after an existing step

</td><td>

Select **+** before the step, then choose a step from the toolbox. The step is inserted and the topmost outgoing event is automatically assigned to continue the flow.**Note:** Steps with no outgoing events appear in an Unavailable section at the bottom of the toolbox. To add an unavailable step, use an And branch instead.

</td><td>

![Inserting step before a step.](../image/uib-uii-insert-step-before.png)

</td></tr><tr><td>

Work with unavailable steps

</td><td>

If a step cannot be added at the selected location, it appears in the Unavailable section. Review the explanation to understand why the step is not supported at that point and which alternatives are available.

</td><td>

![List of unavailable steps.](../image/uib-uii-unavailable-steps.png)

</td></tr><tr><td>

Delete a step

</td><td>

Select the step and select the delete icon ![](../image/uib-delete-event-mapping-icon.png). When a step is deleted, any dependent downstream bindings reset to their defaults, with a visual indicator confirming the reset. Any outgoing events for this step are deleted and displayed with red borders.

</td><td>

![Delete a step.](../image/uib-uii-delete-step.png)

</td></tr><tr><td>

Add a parallel branch

</td><td>

Insert an **And** step from the Logic section of the toolbox. Branches execute in order from top to bottom. If an **And** branch exists with no steps, you can’t add another **And** branch.

</td><td>

![Added an And branch.](../image/uib-uii-add-and-branch.png)

</td></tr><tr><td>

Insert If/Else logic

</td><td>

Insert an If/Else step from the Logic section of the toolbox. When inserted before an existing step, the downstream flow is preserved in the Else branch. Define conditions using formula building or a script. Branches evaluate top to bottom and the first true branch executes.**Note:** An If/Else step includes one If branch and one Else branch. These branches are required and can’t be deleted. Any additional If branches are optional and can be removed.

</td><td>

![Insert If/Else logic.](../image/uib-uii-if-else.png)

</td></tr><tr><td>

Delete If branch

</td><td>

Select the If branch and select the delete icon ![](../image/uib-delete-event-mapping-icon.png). You can delete an If branch only when more than one If branch exists. You cannot delete the last remaining If branch or the Else branch.

</td><td>

![Delete If branch.](../image/uib-uii-delete-if-branch.png)

</td></tr><tr><td>

Swap outgoing events

</td><td>

Select the event node on the diagram and choose which outgoing event continues the flow.**Note:** Each outgoing event can be used only once per step. Events already in use are read-only. Remove an existing branch to change event assignments

</td><td>

![Swap outgoing events.](../image/uib-uii-swap-event.png)

</td></tr><tr><td>

Delete an event

</td><td>

Select the event on the diagram and select the delete icon ![](../image/uib-delete-event-mapping-icon.png). Any associated connections and downstream steps are removed.

</td><td>

![Delete the event.](../image/uib-uii-delete-event.png)

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

The updated UI interaction is saved. Any page events or declarative actions that reference this interaction automatically use the updated flow the next time the interaction is triggered.

**Parent Topic:**[UI interactions](../concept/uib-ui-interactions.md)


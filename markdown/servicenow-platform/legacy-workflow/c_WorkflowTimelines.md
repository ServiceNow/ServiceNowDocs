---
title: Workflow timelines
description: The system provides a timeline view of history activities associated with a workflow context.By default, the timeline displays all activities and transitions requested when first opened.You can display a partial workflow timeline.In a workflow timeline, subflow spans appear as a different color than the activities of the main workflow.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow timelines

The system provides a timeline view of history activities associated with a workflow context.

Timelines display a linear calendar of activities, such as tasks and approvals, defined by their start and end dates. Each activity on the timeline is represented by a span, which is displayed as a horizontal, colored bar. Each span has a label and a tooltip that contains additional information about the activity. The left pane displays all the activities in the context \(or contexts\) in an expandable hierarchy. You can change the timeline's perspective for a more granular view of the data.

**Note:** Workflow timelines reflect context history only and are not real-time gauges of workflow activity.

**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

## Use a timeline

By default, the timeline displays all activities and transitions requested when first opened.

### About this task

Collapse any part of the hierarchy in the activity pane and the timeline adjusts automatically. Date/time and duration controls enable you to scale the timeline to view all the elements at once. To display a timeline, click a UI action within a Workflow Context record.

### Procedure

1.  Navigate to**All** &gt; **Workflow** &gt; **Live Workflows** &gt; **Active Contexts**.

2.  Select a context.

3.  In **Related Links**, click **Show Timeline** to display the timeline for the entire context.

    The timeline opens with all activities expanded and the view set to **Max**, which displays the entire timeline at the width of the pane. The title of the timeline is in the form Workflow context: &lt;context name&gt;, Requested Item: &lt;requested item number&gt;.

    ![Workflow timeline iPhone](../image/WorkflowTimelineIPhone4.png)

4.  Use the Range Selectors at the top of the timeline to change the perspective.

    ![Timeline perspective bar](../image/TimelinePerspectiveBar.png)

    The increments go from one day to one year. To limit the timeline to an increment between the start date of the first span and the end date of the last span, click **Max**.

5.  Use the starting and ending calendar fields to select the timeline perspective.

    These fields control the same perspective as the slider at the bottom of the timeline.

6.  Use the pink slider at the bottom of the timeline to change the perspective.

    ![Workflow timeline slider](../image/WorkflowTimelineSlider.png)

    1.  Move the slider from right to left to view all the spans on a long timeline.
    2.  Adjust the end points of the slider to make arbitrary changes to the magnification.

        A narrow slider zooms in on the spans and provides a more detailed view of complex timelines. A wide slider pulls the view out and makes more of the timeline visible on the screen.

7.  To focus the timeline view on selected activities, expand or collapse the activity tree.

    Spans not visible in the activity tree are not shown in the timeline pane.

    ![Workflow timeline collapsed](../image/WorkflowTimelineCollapsed.png)

8.  Hover over an activity span to display a tooltip with information about the activity.

    This action highlights the activity in the activity pane.

    ![Workflow timeline tooltip](../image/WorkflowTimelineTooltip.png)

9.  Hover over the transition between two activities to highlight the activity and the predecessor activity in the activity pane.

    ![Workflow timeline transitions](../image/WorkflowTimelineTransitions.png)

10. Double-click a span to display a history record for that activity.

    History records shows information such as the **State** and the starting and ending times.

    ![Workflow timeline history popup](../image/WorkflowTimelineHistoryPopup.png)


## Timeline for a selected activity

You can display a partial workflow timeline.

### Procedure

1.  Navigate to**All** &gt; **Workflow** &gt; **Live Workflows** &gt; **Active Contexts**.

2.  Open a Workflow Context record.

3.  On the **Workflow Activity History** related list, select one or more individual activities.

4.  Click **Show Timeline** from the action menu.

    The resulting view is a snapshot of the timeline, showing only the selected activities and their transitions, if any.

5.  Collapse the tree to confine the view even further.

    ![Partial workflow timeline](../image/WorkflowTimelinePartial.png)

6.  To view a timeline displaying activities from different contexts:

    You might use this feature to display a subflow's context with the parent workflow context.

    1.  Navigate to **Workflow** &gt; **Live Workflows** &gt; **History**.
    2.  Select individual history items from the list.
    3.  Select the **Show Timeline** option from the actions menu.

        History items are arranged in a hierarchy in the activities pane under their contexts. The timeline title is **Multiple Contexts**. The timeline draws only the activities and relationships of the history items selected.


## View subflows in a workflow timeline

In a workflow timeline, subflow spans appear as a different color than the activities of the main workflow.

![](../image/WorkflowTimelineSubflow.png "Workflow timeline subflow")


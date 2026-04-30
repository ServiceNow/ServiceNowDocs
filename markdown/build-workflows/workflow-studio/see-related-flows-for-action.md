---
title: See related flows for action
description: See the list of flows that include a custom action. Determine the impact that changes to an action have on published and draft flows.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Flow administration, Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# See related flows for action

See the list of flows that include a custom action. Determine the impact that changes to an action have on published and draft flows.

## Before you begin

Role required: admin or flow\_designer

## About this task

Determine the impact that your action changes have on published and draft flows. See a list of flows that include the action and determine if your changes require changes to the related flows. For example, if you change the inputs an action uses, someone must reconfigure the related flows to use the new or modified inputs.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Actions**.

3.  Select the action whose related flows that you want to see.

    The system displays the action in the Workflow Studio environment.

4.  From the More Actions menu, select **See related flows**.

    The system shows the Related Flows dialog.

    ![The Related Flows dialog box displays 1 related flow named Add a Pause. The related flow is marked as active.](../images/see-related-flows-example.png)

    The Related Flows dialog shows information about the flows that use the action.

    -   The number of flows using the action
    -   The name of each related flow
    -   The activation status of each related flow
    -   The number of flows using the action that are hidden by security constraints

## What to do next

Determine if your planned action changes require updates to the related flows. Publishing an action also displays a list of related flows that use the action.

**Parent Topic:**[Flow administration](../concept/flow-administration.md)


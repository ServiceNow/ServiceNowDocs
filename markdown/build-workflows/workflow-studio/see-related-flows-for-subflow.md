---
title: See related flows for subflow
description: See the list of flows that include a subflow. Determine the impact that changes to a subflow have on published and draft flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/see-related-flows-for-subflow.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Flow administration, Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# See related flows for subflow

See the list of flows that include a subflow. Determine the impact that changes to a subflow have on published and draft flows.

## Before you begin

Role required: admin or flow\_designer

## About this task

Determine the impact that your subflow changes have on published and draft flows. See a list of flows that include the subflow and determine if your changes require changes to the related flows. For example, if you change the inputs a subflow uses, someone must reconfigure the related flows to use the new or modified inputs.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Subflows**.

3.  Select the subflow whose related flows that you want to see.

    The system displays the subflow in the Workflow Studio environment

4.  From the More Actions menu, select **See related flows**.

    The system shows the Related Flows dialog.

    The Related Flows dialog shows information about the flows that use the subflow.

    -   The number of flows using the subflow
    -   The name of each related flow
    -   The activation status of each related flow
    -   The number of flows using the subflow that are hidden by security constraints

## What to do next

Determine if your planned subflow changes require updates to the related flows.

**Parent Topic:**[Flow administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/flow-administration.md)


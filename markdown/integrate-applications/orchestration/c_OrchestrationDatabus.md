---
title: Orchestration databus
description: The databus allows workflow designers to track the flow of data through an Orchestration workflow and provides access to output data that can be consumed by other custom activities.The Data tab in the Workflow Editor lists all custom activities used in the current workflow that produce data and displays that data for reuse in other custom activities.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Classic Orchestration, Workflow Data Fabric]
---

# Orchestration databus

The databus allows workflow designers to track the flow of data through an Orchestration workflow and provides access to output data that can be consumed by other custom activities.

Data is made available in a workflow when you use activities created with the [Orchestration activity designer](c_WorkflowActivityDesigner.md). The activity designer provides the ability to specify well defined inputs and outputs for your activities. When you use those activities on the workflow canvas, the outputs appear in the **Data** tab and are available for use as inputs in subsequent activities.

**Note:** Orchestration does not filter the data you are given for reuse in the **Data** tab. You must make sure an activity in the workflow canvas has executed before you consume its output data.

When you drop a custom activity onto the workflow canvas, the system assigns it an index. If you delete an activity from the canvas and add a new one, the indexes are not reused. This ensures that you don’t accidentally start subscribing to data you did not intend to use. If you update an activity in the activity designer, the system automatically updates the activity on the canvas to ensure the data you are subscribing to downstream is not affected.

**Parent Topic:**[Classic Orchestration](../../../product/orchestration/reference/r-orchestration.md)

## Reuse data in the activity designer

The **Data** tab in the Workflow Editor lists all custom activities used in the current workflow that produce data and displays that data for reuse in other custom activities.

### Before you begin

Roles required: workflow\_creator

### About this task

Activities are categorized by application in this tab and are available for use as data sources for other activities. The **Data** tab is a graphical representation of the workflow Databus, which manages all the temporary data used by the current workflow.

### Procedure

1.  Drag output variables from an activity in this tab into the inputs of another activity on the workflow canvas to link the activities together.

    You can use any of the outputs in the structure, regardless of the application to which they belong. An index number in parenthesis after the activity name provides a unique identifier for the parameters that you use as input data in other activities. If you do not name a custom activity, the only identifier for that activity in the **Data** tab is the index number. Index numbers indicate the sequence in which custom activities were added to the workflow and are not reused. When you drag a custom activity onto the workflow canvas, the system adds that activity and its output data to the structure. Conversely, if you remove a custom activity from the canvas, that activity and its outputs disappear from the data list.

    ![Reusing output variables from the data tab](../image/WorkflowDataTab.png)

2.  Point to an activity to display information about it in a pop-up window.

    Any output data reused by the activity is listed in the **Databus Output** field of the pop-up window.

    ![Databus output information screen](../image/DatabusPop-up.png)



---
title: Load data structure
description: Load a data structure of child variables within an Object variable.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Complex data, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Load data structure

Load a data structure of child variables within an Object variable.

## Before you begin

-   Role required: action\_designer, flow\_designer, or admin
-   [Create an action in Workflow Studio](create-action.md) or [Create a subflow in Workflow Studio](create-subflow.md)

## Procedure

1.  Create a data variable.

2.  From **Type**, select **Object**.

3.  Expand the Advanced options for the Object variable whose data structure you want to replace.

4.  From **Structure**, select **Start from Template**.

    Workflow Studio displays the **Template** field.

5.  From **Template**, select the template containing the template you want to load.

    If the Object variable has no existing data structure, Workflow Studio loads the data structure into it. If the Object variable has an existing data structure, Workflow Studio displays a confirmation dialog to replace the existing structure.


**Parent Topic:**[Complex data](../concept/complex-data.md)


---
title: Show subflow stages in a parent flow
description: Show subflow stages as part of the execution details of a parent flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/show-subflow-stages-in-a-parent-flow.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Flow and subflow stages, Building flows, Use, Workflow Studio, Build workflows]
---

# Show subflow stages in a parent flow

Show subflow stages as part of the execution details of a parent flow.

## Before you begin

This task assumes that you are familiar with flow and subflow stages, stage fields, and stage sets. For more information about stages, see [Flow and subflow stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/flow-designer-stages.md).

Role required: flow\_designer or admin

## Procedure

1.  Create a subflow that contains one or more stages.

    For more information about creating a subflow, see [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/create-subflow.md). For more information about adding stages to a subflow, see [Configure stages and add them to a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/add-stages.md).

2.  Create or open the parent flow that will call the subflow.

    For example, open the flow named My Item Request Flow.

3.  From an appropriate step of the flow, select **Subflow** and then select the subflow that you want to run.

    For example, select the Fulfillment subflow.

4.  Select the **Show Subflow Stages** option.

    \[Omitted image "example-subflow-stages-01-parent-flow.png"\] Alt text: Example Fulfillment Subflow configured to show subflow stages.

5.  Configure any required subflow inputs.

    For example, provide the Requested Item from the Service Catalog trigger.

6.  Add stages to the parent flow.

    For example, add the Manager Approval and Completed stages to the parent flow.


**Parent Topic:**[Flow and subflow stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/flow-designer-stages.md)


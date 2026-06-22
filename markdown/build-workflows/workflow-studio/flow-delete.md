---
title: Delete a flow
description: Delete a flow that you no longer need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/flow-delete.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a flow, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Delete a flow

Delete a flow that you no longer need.

## Before you begin

Role required: flow\_designer or admin

## About this task

You can only delete flows that are in the same application scope as the current session. You can't delete flows that are read-only protected. If your instance uses domain separation, make sure that you are in the Global scope. For more information, see [Domain separation and Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-designer-domain-separation.md).

## Procedure

1.  If needed, change application scope to that of the flow you want to delete.

    For more information about changing application scope, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/next-experience-pickers.md).

2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

3.  On the homepage, select **Flows**.

4.  From the list of flows, select the box next to the flow you want to delete.

    \[Omitted image "example-delete-flow-list-selection.png"\] Alt text: List of flows with the Demo delete flow row selected.

    **Tip:** You can filter the list of flows by name or application. For example, selecting the Filter icon on the **Name** column, selecting the **contains** operator, entering the string `demo`, and selecting **Apply** displays all flows that have the string demo in the name.

5.  Select **Delete**.

    If the delete option is unavailable, you may be in the wrong application scope, or the flow may be read-only protected.

    Workflow Studio displays a confirmation window.

6.  From the Confirmation window, select **Delete**.

    \[Omitted image "example-delete-flow-confirmation.png"\] Alt text: Delete confirmation window


## Result

Workflow Studio deletes the flow and removes it from the list of available flows.

**Parent Topic:**[Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md)


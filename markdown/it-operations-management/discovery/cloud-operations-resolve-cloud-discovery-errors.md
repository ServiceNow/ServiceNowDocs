---
title: Resolve Cloud Discovery errors in Cloud Discovery Workspace
description: View the Cloud Discovery errors that occurred during the discovery and resolve them. You can view the errors for all the Cloud Discovery runs or a single Cloud Discovery run.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Resolve Cloud Discovery errors in Cloud Discovery Workspace

View the Cloud Discovery errors that occurred during the discovery and resolve them. You can view the errors for all the Cloud Discovery runs or a single Cloud Discovery run.

## Before you begin

Role required: sn\_cloud\_ops\_ws.cloud\_ops\_admin

## Procedure

1.  Navigate to **Cloud Discovery Workspace** &gt; **Cloud Discovery**.

2.  Select **Errors**.

    The **Status** tab of the Schedules module displays the list of errors for the selected discovery run.

3.  Select a category tile to display the specific error codes that occurred in that category.

4.  Select the error code tile that you want to investigate.

    The list displays all occurrences of that error code for all the Cloud Discovery schedules. The list shows the error message, Configuration Item \(CI\) ID, IP address of each instance that experienced the error, and the error status.

5.  Perform one of the following actions:

    -   Select the specific errors, and then select the appropriate action from the **Selected errors** section.
    -   Select appropriate action from the **All errors** section.

        Cloud Discovery applies the selected action to all errors of the list.

<table id="table_sdv_frk_jsb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create task

</td><td>

You can create an error task and assign it to an user for resolution.Assigned errors are considered **Active errors**, and actions can still be performed on them.

 Cloud Discovery displays the error task number on the error code tile.

</td></tr><tr><td>

Retry discovery

</td><td>

Cloud Discovery retries an IP-based discovery.When you select **Retry discovery**, Cloud Discovery performs this action on all the active errors that are available in the list.

 You can retry the discovery, only if the ServiceNow® IP-based Discovery plugin \(com.snc.discovery.ip\_based\) is installed and activated in the instance.

</td></tr><tr><td>

Ignore

</td><td>

Cloud Discovery ignores the error.

</td></tr></tbody>
</table>6.  Check the **Error Status** column to see the results of the remediation.

    Single retries complete quickly. Retries for large numbers of IP addresses can take several minutes.

    An error can have one of the following statuses:

    -   **Active error**: Unresolved error. This is the default status of all new errors.
    -   **Resolved**: Resolved error.
    -   **Assigned**: Task assigned to resolve this error.
    -   **Pending Discovery**: Waiting for Discovery to start after you execute the **Retry discovery** action on all errors.
    -   **In Discovery**: Discovery is currently active.


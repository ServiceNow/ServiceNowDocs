---
title: Resolve Cases in Workspace through HQ Agents
description: Review assigned break-fix cases in the CSM/FSM workspace, select a service issue type, and propose resolutions using troubleshooting steps, service incidents, or work orders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/breakfix-resolve-workspace.html
release: australia
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 3
breadcrumb: [Manage Break-Fix cases, Retail]
---

# Resolve Cases in Workspace through HQ Agents

Review assigned break-fix cases in the CSM/FSM workspace, select a service issue type, and propose resolutions using troubleshooting steps, service incidents, or work orders.

## Before you begin

-   Break-fix case is assigned to your queue in the workspace
-   Review case details including affected equipment, store, and description
-   **Role required:** HQ Support Agent \(BREAKFIX\_AGENT role\)
-   **Note:** Work order creation requires the FSM integration plugin to be installed.

## About this task

The CSM/FSM workspace provides your case queue. Service issue type is mandatory before proposing resolution. Selecting "Break-fix Hardware" enables Create Work Order. Selecting "Break-fix IT" enables Create Incident. Troubleshooting steps can be added for either type. When incidents or work orders are created, their state changes and comments are added as work notes on the case.

**Role Requirements:** The BREAKFIX\_AGENT role is required for all case resolution, including creating work orders—the Create Work Order button appears only if the FSM integration plugin is installed. Creating an incident requires the sn\_incident\_write role assigned to the Break-fix agent.

## Procedure

1.  Open CSM/FSM workspace

2.  Navigate to **Retail Break-fix case** list

    **Note:** List displays all cases assigned to your queue.

3.  Open the break-fix case you want to resolve

    **Note:** Review: Case Number, Opened at, State, Requested by, Priority, Requesting store, Affected device \(Install base\), Short description, Description.

4.  In the **Service issue type** field, select **Break-fix Hardware** or **Break-fix IT**

    **Note:** Mandatory. Hardware enables work order creation. IT enables incident creation. You can change this selection later if needed.

5.  Propose resolution using one of three methods:

    1.  **Method 1 - Troubleshooting Steps:** Add step-by-step instructions in **Resolution notes** field or activity stream comments.

        Include KB article links if applicable.

    2.  **Method 2 - Create Incident \(IT Issues\):** Click **Create Incident**.

        Requires the sn\_incident\_write role assigned to the Break-fix agent. Verify short description, description, and priority carry forward to incident. Incident number appears in activity stream. Monitor the incident state and comments—they are added as work notes on the case.

    3.  **Method 3 - Create Work Order \(Hardware Issues\):** Click **Create Work Order**.

        If the button does not appear, verify the FSM integration plugin is installed. Verify details carry forward. Monitor the work order state and comments—they are added as work notes on the case.

        **Note:** The Create Work Order button appears if the FSM integration plugin is installed. Role access is based on the break-fix agent role. Contact your administrator if the button is missing and you need to create work orders.

6.  Click **Propose Solution**

    **Note:** Case state changes to "Resolution Proposed". Requestor receives notification and can Accept or Reject.


## Result

Case transitions to "Resolution Proposed" state. Requestor receives notification and can Accept \(closes case\), Reject \(reopens to your queue with reason\), or Self-Close \(closes without your involvement\). If you created an incident or work order, its state changes and comments are added as work notes on the case.

## What to do next

If requestor rejects resolution, case reopens to your queue with their reason documented. Propose an alternative resolution. See [Respond to Resolutions \(Portal and Mobile\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-respond-resolution.md) to understand the requestor's actions.

**Parent Topic:**[Manage Break-Fix cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-manage-cases.md)

**Related topics**  


[Break-Fix Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-overview.md)

[Submit Break-Fix Cases through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-submit-case.md)

[Respond to resolutions through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-respond-resolution.md)

[Components for Break-Fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-reference.md)


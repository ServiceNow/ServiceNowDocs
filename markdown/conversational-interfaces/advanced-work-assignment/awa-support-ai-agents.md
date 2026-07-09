---
title: Support AI agents
description: Enable AI agents to automatically accept work items by configuring the Include AI agents flag in AWA assignment rules. This allows eligible AI agents in a group to participate in work distribution alongside live agents, improving coverage and reducing manual assignment overhead.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/advanced-work-assignment/awa-support-ai-agents.html
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 4
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Support AI agents

Enable AI agents to automatically accept work items by configuring the Include AI agents flag in AWA assignment rules. This allows eligible AI agents in a group to participate in work distribution alongside live agents, improving coverage and reducing manual assignment overhead.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home** &gt; **Settings** &gt; **Assignment Rules**.

2.  Do one of the following:

    -   To create an assignment rule, select **New**.
    -   To edit an assignment rule, select the assignment rule you want to update.
3.  On the Assignment Rules form, fill in the fields.

<table id="table_dkx_dpy_h5b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the assignment rule.

</td></tr><tr><td>

Application

</td><td>

Name of the application to which this assignment rule belongs. The default application is **Global**.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the assignment rule.

</td></tr><tr><td>

Assign by

</td><td>

Type of assignment. Select one of the following values:-   **Last Assigned**: Routes a work item to the agent who has gone the longest without being assigned work.
-   **Most Capacity**: Routes a work item to the agent who has the greatest availability for handling the work.


</td></tr><tr><td>

Auto-assign handling

</td><td>

Work items are automatically accepted without agents having to select **Accept** or **Reject**.-   **Enable auto-assign work items**: Select this option to have work items automatically accepted on behalf of agents. Agents are unable to manually **Accept** or **Reject** work items.
-   **Display options**: Select one of the following values:
    -   Select **Inbox card** to accept the chat interactions and add them to the agent inbox. Agents can open the accepted interaction from the inbox.
    -   Select **Inbox card and workspace tab** to accept chat interactions and open a tab for each accepted interaction.


</td></tr><tr><td>

Rejection handling

</td><td>

Work items are rejected and handled. -   Allow agents to reject: Enable agents to reject work items in their inbox.
-   Reassign on timeout: Enable reassignment of work items not accepted or rejected by agents within the specified timeout period:
    -   Timeout value \(Days and Hours, Minutes, Seconds\): Length of time allowed for an agent to accept or reject a work item before the assignment times out \(ends\) and is reassigned to another agent.
    -   Timeout presence state: Agent availability state after the timeout occurs: Available, Away, or Offline.
This tab isn't available when auto-assign handling is activated.

</td></tr><tr><td>

Skill handling

</td><td>

Skill-based work assignments.-   **Enable skills**: Route work items to agents with the appropriate skills. When selected, the **Evaluate skill level** and **Enforce mandatory skills** check boxes appear cleared.
-   **Evaluate skill level**: Route work items to the most qualified agents based on their skill level.
-   **Enforce mandatory skills**: Route work items to agents with required skills.


</td></tr><tr><td>

Shift handling

</td><td>

Work items are assigned to agents based on shifts.-   Enable-shift based assignment: Assign work items to agents based on time available in their shifts.
-   Add time constraints: Add the time required to complete work items in shifts and whether agents should be continuously available for the required time period.

This field appears only when the **Enable shift-based assignment** option is selected.

-   Agent criteria: Select an agent based on the time left in the agent's shift.

This field appears only when the **Enable shift-based assignment** option is selected.

Available options:

    -   Least time left in shift: Assign a work item to an agent from a group of available agents based on the least amount of time available in their shifts.
    -   Most time left in shift: Assign a work item to an agent from a group of available agents based on the maximum time available in their shifts.
-   Time required: Time required to complete a work item.
-   Available continuously for the required time: Assign work items to agents who are continuously available for the required time period without any breaks in a shift. Agents who don’t have the minimum time required in their shifts aren’t considered for work item assignments.

**Note:** The **Shift handling** field is available only if the Advanced Work Assignment plugin \(com.glide.awa\) is activated and the Workforce Optimization for Customer Service plugin \(com.snc.wfo.csm\) or the Workforce Optimization for ITSM plugin \(com.snc.wfo\_itsm\) plugin, or both, is activated. As a manager, you must have planned schedules for agents to assign them shifts. For more information, see [Scheduling in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/explore-scheduling-configurable-wfo-cs.md) and [Scheduling in Workforce Optimization for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/explore-schedule-configurable-wfo-itsm.md).

This field appears only when the **Add time constraints** option is selected.

</td></tr><tr><td>

Manage AI agents

</td><td>

Work items are assigned to AI agents.

 Previously, assignment rules could only route work to live agents, leaving AI agents unable to participate in automated work distribution. The Include AI agents flag solves this by extending assignment rule logic to recognize and target AI agents as eligible recipients. When enabled, the flag allows the system to identify AI agents in a group \(by their identity\_type = 'ai\_agent'\), recognize their "AI Available" presence state, and automatically route matching work items to them for immediate acceptance. This eliminates the need for manual AI agent assignment and enables seamless hybrid work distribution across both live and AI agents within the same group.

</td></tr></tbody>
</table>4.  Select **Submit** for a new assignment rule or **Update** if modifying an existing assignment rule.



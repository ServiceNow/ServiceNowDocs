---
title: Advanced Work Assignment dashboard for operations
description: Enable managers to monitor work items across all service channels so that their agents can better support customer needs.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics Solutions for Advanced Work Assignment, Analytics &amp; Reporting Solutions, Reference, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Advanced Work Assignment dashboard for operations

Enable managers to monitor work items across all service channels so that their agents can better support customer needs.

This dashboard is available in the Performance Analytics - Content Pack - Advanced Work Assignment plugin. For information on activating the content pack, see [Platform Analytics Solutions for Advanced Work Assignment](../../application-content-packs/concept/awa-content-pack.md).

The Overview tab of the Operations dashboard displays information across all queues, teams, and channels.

![The overview tab of the dashboard displays indicators and reports to track agent operations with customers.](../../../administer/advanced-work-assignment/image/awa-operations-dashboard-update.png "AWA dashboard for Operations - Overview")

The Queue Manager tab of the Operations dashboard displays overall queue information. You can select the queue you want to look at from the left-hand panel.

![The queue manager tab of the dashboard displays indicators and reports to track agent operations with customers.](../../../administer/advanced-work-assignment/image/awa-operations-dashboard-queue-manager.png "AWA dashboard for Operations - Queue Manager")

The Team Manager tab of the Operations dashboard displays information at a group level. You can select the group you want to look at from the left-hand panel.

![The team manager tab of the dashboard displays indicators and reports to track agent operations with customers.](../../../administer/advanced-work-assignment/image/awa-operations-dashboard-team-manager.png "AWA dashboard for Operations - Team Manager")

The Channel Owner tab of the Operations dashboard displays overall channel data, depending on the service channel you select from the drop-down list.

![The channel owner tab of the dashboard displays indicators and reports to track agent operations with customers.](../../../administer/advanced-work-assignment/image/awa-operations-dashboard-channel-owner.png "AWA dashboard for Operations - Channel Owner")

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|AWA administrator: Configures AWA to best fit the business needs of customer service.|awa\_admin|
|AWA manager: Identifies the areas of concern for routing and assignment of work items across service channels.|awa\_manager|
|Agent manager: Manages agents or agent groups. The agent manager wants to know what agents are working on to make sure that customer needs are being met.|sn\_customerservice\_manager|
|Performance Analytics administrator: Ensures that business managers are making the best use of Performance Analytics solutions.|pa\_admin or pa\_viewer|

## Use case

This dashboard provides support managers with an overview of incoming work items and the availability of agents to handle them. Managers can monitor these daily trends to determine if adjustments should be made to the routing criteria, agent capacity values, and other settings that determine how work is pushed to agents.

## Breakdowns

Breakdowns divide information into different categories. To analyze data according to different categories, select a breakdown from the dashboard menu:

-   Service Channel
-   Queue

For more information on analyzing data with breakdowns, see Using breakdowns on dashboards.

## Data visualizations

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work Items Waiting

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Work items that are pending accept or queued.

</td></tr><tr><td>

Available Agents

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Number of agents that are available.

</td></tr><tr><td>

Accepted Work Items \(Today\)

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Number of operation work items that agents accepted today. This includes auto-assigned work items that are accepted.

</td></tr><tr><td>

Average Wait Time \(Today\)

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Average time it takes for an agent to accept a chat in the queue today.

</td></tr><tr><td>

Timed out Work Items \(Today\)

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Work items that have timed out today.

</td></tr><tr><td>

Rejected Work Items \(Today\)

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Work items that were rejected but not timed out.

</td></tr><tr><td>

Presence State of Agents

</td><td>

 

</td><td>

Distribution of agents across different presence states.

</td></tr><tr><td>

Agent Presence &amp; Capacity

</td><td>

 

</td><td>

Count and list of agents in an assignment group with their current presence state, time since the user entered in the current presence state, and capacity in use for each channel.-   Agent
-   Current presence state
-   Updated
-   Channel
-   Capacity in use
-   Applied Max Capacity
-   Universal Capacity In Use
-   Max Universal Capacity

</td></tr></tbody>
</table>
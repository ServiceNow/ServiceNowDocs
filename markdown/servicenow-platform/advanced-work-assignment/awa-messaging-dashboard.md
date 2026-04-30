---
title: Advanced Work Assignment dashboard for messaging
description: Enable managers to monitor Conversation \[interaction\] work items so that their agents can better support customer needs.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Platform Analytics Solutions for Advanced Work Assignment, Analytics &amp; Reporting Solutions, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Advanced Work Assignment dashboard for messaging

Enable managers to monitor Conversation \[interaction\] work items so that their agents can better support customer needs.

This dashboard is available in the Performance Analytics - Content Pack - Advanced Work Assignment plugin. For information on activating the content pack, see [Platform Analytics Solutions for Advanced Work Assignment](../../application-content-packs/concept/awa-content-pack.md).

![The dashboard displays indicators and reports to track agent messaging with customers.](../../../administer/advanced-work-assignment/image/AWAMessaging-update.png "AWA dashboard for Messaging")

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|AWA administrator: Configures Advanced Work Assignment to best fit the business needs of customer service.|awa\_admin|
|AWA manager: Identifies the areas of concern for routing and assignment of work items across service channels.|awa\_manager|
|Agent manager: Manages agents or agent groups. The agent manager needs to know what agents are working on to make sure customer needs are being met.|sn\_customerservice\_manager|
|Performance Analytics administrator: Ensures that business managers are making the best use of Performance Analytics solutions.|pa\_admin or pa\_viewer|

## Use case

This dashboard provides support managers with an overview of incoming work items and the availability of agents to handle them. Managers can monitor these daily trends to determine if adjustments should be made to the routing criteria, agent capacity values, and other settings that determine how work is pushed to agents.

## Indicators

Indicators define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior.

|Indicator|Description|
|---------|-----------|
|Abandon Rate|Percentage of conversations that have been abandoned by the requestor.|

## Data visualizations

<table id="table_gcg_5zn_qsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active Conversations

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Agent Chat messaging conversations that are not Closed Complete or Closed Abandoned and are not cancelled.

</td></tr><tr><td>

Unassigned Conversations

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Agent Chat messaging conversation that is in a pending accept or queued state.

</td></tr><tr><td>

In Progress Conversations

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Agent Chat messaging conversation that is on hold, new, or work in progress.

</td></tr><tr><td>

Average Wait Time - Last 24 Hours

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Average time it takes for an agent to accept a chat in the queue today.

</td></tr><tr><td>

Consumer Average Response Time - Past Month

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Messaging conversation that is Closed Complete or Closed Abandoned and is assigned and the requester average response time is not empty and it was created after one month.

</td></tr><tr><td>

Time To First Response - Last 24 Hours

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Inbound messaging conversation where the first response wait time is not empty and it was created after 24 hours.

</td></tr><tr><td>

Customer Satisfaction - Past Month

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Customer satisfaction score over the past month

</td></tr><tr><td>

Service Level

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

-   Type
-   Service Channel
-   Queue
-   Service Level

</td></tr><tr><td>

Agent Presence &amp; Capacity

</td><td>

 

</td><td>

-   Agent
-   Current presence state
-   Updated
-   Channel
-   Capacity in use
-   Applied Max Capacity
-   Universal Capacity In Use
-   Max Universal Capacity

</td></tr><tr><td>

Average Handling Time - Last 24 Hours

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Average time of the interactions handling duration in the last 24 hours.

</td></tr><tr><td>

Agent Average Response Time - Last 24 Hours

</td><td>

Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)

</td><td>

Average agent response time in the last 24 hours.

</td></tr></tbody>
</table>**Parent Topic:**[Platform Analytics Solutions for Advanced Work Assignment](../../application-content-packs/concept/awa-content-pack.md)


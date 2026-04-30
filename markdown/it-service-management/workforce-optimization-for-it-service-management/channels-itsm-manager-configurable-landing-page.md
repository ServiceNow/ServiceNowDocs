---
title: Workforce Optimization for ITSM Channels landing page
description: Manage queues and analyze the status of incidents and chats using the Channels landing page. You can also monitor team performance and work assignments from one location.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workforce Optimization for ITSM landing pages, Advanced configurations for Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Workforce Optimization for ITSM Channels landing page

Manage queues and analyze the status of incidents and chats using the Channels landing page. You can also monitor team performance and work assignments from one location.

![Channels Landing Page](../../../product/configurable-workforce-optimization-itsm/image/channels-landing-page1.png)

## End user and roles

As an admin, you can create or customize landing pages for the channel manager. For more information, see Creating custom landing pages for workspaces. If you have multiple landing pages, you can set the order for the landing pages. The lower the order, the higher the precedence in displaying the pages.

<table id="table_znp_cdb_34b"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

As a channel manager, you can:-   Analyze real-time data such as:
    -   The number of incidents with critical priority, breached SLAs, escalated or unassigned incidents.
    -   The number of chats that are in progress or with requests for help.
    -   Agent distribution across work assignments, work items awaiting to be assigned, and number of agents available.
    -   The performance of your team.
-   Drill down into each report or analytics to get more data.

</td><td>

sn\_channel\_mgmt.user

</td></tr></tbody>
</table>## Use cases

As a channel manager, you can monitor key information such as the number of SLAs that have been breached, how many open incidents have critical priority, and how many work items are waiting to be assigned from one location.

## Performance Analytics Indicator

**Incidents closed this week**: The number of incidents closed during the current week.

## Breakdowns

-   Assigned to
-   Assignment group

## Data visualizations

|Title|Type|Source table or database view|Description|
|-----|----|-----------------------------|-----------|
|Open Critical|Single score![Single score](../../performance-analytics/image/single-score.png)|Incident \[incident\]|Number of open incidents with critical priority.|
|Unassigned|Single score![Single score](../../performance-analytics/image/single-score.png)|Incident \[incident\]|Number of open incidents that have not been assigned.|
|Escalated|Single score![Single score](../../performance-analytics/image/single-score.png)|Incident \[incident\]|Number of open incidents that have been escalated.|
|SLAs breached|Single score![Single score](../../performance-analytics/image/single-score.png)|Task SLA \[task\_sla\]|Number of open incidents with Service Level Agreements that have been breached.|
|Updated &gt; 7 days|Single score![Single score](../../performance-analytics/image/single-score.png)|Incident \[incident\]|Number of open incidents that have not been updated in the last 7 days.|
|Open for 30 days|Single score![Single score](../../performance-analytics/image/single-score.png)|Incident \[incident\]|Number of incidents that have not been updated in the last 30 days.|
|In-progress chats|Single score![Single score](../../performance-analytics/image/single-score.png)| |Number of open interactions where agents are currently on a chat with customers resolving issues.|
|Help requested|Single score![Single score](../../performance-analytics/image/single-score.png)| |Number of current open interactions where agents are requesting help from a manager while on a chat with customers to resolve issues.|
|Agent distribution|Bar chart![Bar chart](../../../reuse/reporting/image/bar-trend.svg)|Presence States \[awa\_presence\_state\]|The current presence status of agents distributed on work assignments.|
|Waiting work items|Single score![Single score](../../performance-analytics/image/single-score.png)| |Number of work items that are currently waiting to be assigned.|
|Available agents|Single score![Single score](../../performance-analytics/image/single-score.png)| |Number of agents currently available to work on work items.|
|Total open incidents|Bar chart![Bar chart](../../../reuse/reporting/image/bar-trend.svg)| |Total number of incidents that are in various workflow states and have not been closed.|

**Parent Topic:**[Workforce Optimization for ITSM landing pages](../../../product/configurable-workforce-optimization-itsm/concept/configurable-wfo-itsm-landing-pages.md)


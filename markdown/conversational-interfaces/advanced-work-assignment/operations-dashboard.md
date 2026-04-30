---
title: Operations dashboard
description: Enable managers to monitor work items across all service channels so that their agents can better support customer needs.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analytics &amp; Reporting Solutions, Reference, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Operations dashboard

Enable managers to monitor work items across all service channels so that their agents can better support customer needs.

This dashboard is available in the Advanced Work Assignment content pack. For information on activating the content pack, see [Platform Analytics Solutions for Advanced Work Assignment](../../../use/application-content-packs/concept/awa-content-pack.md).

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|AWA administrator: Configures Advanced Work Assignment to best fit the business needs of customer service.|awa\_admin|
|AWA manager: Identifies the areas of concern for routing and assignment of work items across service channels.|awa\_manager|
|Agent manager: Manages agents or agent groups. The agent manager wants to know what agents are working on to make sure that customer needs are being met.|sn\_customerservice\_manager|
|Performance Analytics administrator: Ensures that business managers are making the best use of Performance Analytics solutions.|pa\_admin or pa\_viewer|

## Use case

This dashboard provides support managers with an overview of incoming work items and the availability of agents to handle them. Managers can monitor these daily trends to determine if adjustments should be made to the routing criteria, agent capacity values, and other settings that determine how work is pushed to agents.

## Indicators

<table id="table_kbm_5wt_rhb"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New Work Items

</td><td>

Total number of interaction work items that were created today. The goal for this indicator is to minimize the number of interaction work items that agents receive.

</td></tr><tr><td>

Accepted Work Items

</td><td>

Percentage of interaction work items that agents have accepted.

</td></tr><tr><td>

Exceeding Target Work Items

</td><td>

Percentage of interaction work items that have exceeded the target wait time.

</td></tr><tr><td>

Rejected Work Items

</td><td>

Percentage of interaction work items that agents have rejected.

</td></tr><tr><td>

Timed Out Work Items

</td><td>

Percentage of interaction work items that timed out.

</td></tr><tr><td>

Weekly Trends

</td><td>

Number of work items in each of the following states for the past week:-   New
-   Exceeding Target
-   Abandoned
-   Rejected
-   Timed Out

</td></tr></tbody>
</table>## Breakdowns

To analyze data according to different categories, select a breakdown from the dashboard menu:

-   Service Channel
-   Queue
-   Assignment Group

For more information on analyzing data with breakdowns, see [Using breakdowns on dashboards](https://www.servicenow.com/docs/access?context=c_SpecialDashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## Reports

|Title|Type|Description|
|-----|----|-----------|
|Accepted Work Items - Last Hour|Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)|Number of interaction work items that agents have accepted in the past hour.|
|Abandoned Work Items - Last Hour|Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)|Number of interaction work items that agents have abandoned in the past hour.|
|Average Wait Time - Last Hour|Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)|Average amount of time that customers have spent waiting for an agent response in the past hour.|

**Parent Topic:**[Analytics &amp; Reporting Solutions](analytics-reporting-awa.md)


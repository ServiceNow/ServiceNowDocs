---
title: Insight cards on the Workplace Central dashboard
description: Display key metrics and AI-generated insights from workplace data sources using Insight cards on the Workplace Central dashboard. These Insight cards are auto-generated using generative AI, enabling Space Planners, and Facilities Managers to make data-driven decisions to optimize workplace resources. Insight cards provide proactive insights into various workplace metrics such as space utilization, occupancy rates, attendance patterns, and reservation trends.
locale: en-US
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Workplace Advisor Overview, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Insight cards on the Workplace Central dashboard

Display key metrics and AI-generated insights from workplace data sources using Insight cards on the Workplace Central dashboard. These Insight cards are auto-generated using generative AI, enabling Space Planners, and Facilities Managers to make data-driven decisions to optimize workplace resources. Insight cards provide proactive insights into various workplace metrics such as space utilization, occupancy rates, attendance patterns, and reservation trends.

## Insight cards tables

Workplace Insights adds the following tables.

<table id="table_tpd_fhk_dhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Config Execution\[sn\_wsd\_ai\_agents\_ai\_config\_execution\]

</td><td>

Stores all the logs for all the prompt configuration runs.

</td></tr><tr><td>

AI Prompt Configuration\[sn\_wsd\_ai\_agents\_ai\_prompt\_config\]

</td><td>

Table with information about instructions and data provided to the large language model \(LLM\).

</td></tr><tr><td>

Insights\[sn\_wsd\_ai\_agents\_insights\]

</td><td>

Table that stores all generated insights.

</td></tr><tr><td>

AI Prompt User\[sn\_wsd\_ai\_agents\_m2m\_ai\_prompt\_user\]

</td><td>

Table that holds M2M mapping between the prompt configuration and user criteria.

</td></tr><tr><td>

Insight User\[sn\_wsd\_ai\_agents\_m2m\_insight\_user\]

</td><td>

Table that lists all the users in the User Criteria for whom the insights are mapped or generated.

</td></tr></tbody>
</table>## Scheduled jobs for Insight cards

Several types of scheduled jobs are added to generate Insight cards for workplace operations on the Workplace Central dashboard.

|Scheduled job|Run frequency|Description|
|-------------|-------------|-----------|
|Generate Workplace Insights - Weekly|Weekly|This scheduled job generates workplace Insight cards based on the configured data source and prompt configuration.|
|Send Insight Notifications - Weekly|Weekly|This schedule job runs weekly and sends email notifications to users when new workplace insights are generated.|
|WSD Reservation Historic Data Collection Job|On Demand|The PA admin role \(pa\_admin\) must be explicitly assigned to users for them to run historic indicator jobs and edit indicators.|
|WSD Reservation Daily Collection Job|Daily|This scheduled job runs daily to collect indicator data.|
|Workplace Connectors Daily Collection Job|Daily|This scheduled job runs daily to collect scores and text index.|
|Workplace Connectors Historic Collection Job|On Demand|Run this adhoc scheduled job to to collect scores and text index for the specified date.|


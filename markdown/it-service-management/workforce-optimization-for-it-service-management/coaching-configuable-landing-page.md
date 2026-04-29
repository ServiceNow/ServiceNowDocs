---
title: Workforce Optimization for ITSM Coaching landing page
description: Monitor the performance of your agents and measure the quality of how they resolved issues using the Coaching landing page. Analyze patterns in skill usage over time and see which skills are in demand.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Landing pages, Advanced configurations, Workforce Optimization for ITSM, IT Service Management]
---

# Workforce Optimization for ITSM Coaching landing page

Monitor the performance of your agents and measure the quality of how they resolved issues using the Coaching landing page. Analyze patterns in skill usage over time and see which skills are in demand.

![Coaching landing page](../../../product/configurable-workforce-optimization-itsm/image/coaching-landing-page1.png)

## End user and roles

As an admin, you can create or customize landing pages for the coach to monitor the quality of how agents resolve incidents. If you have multiple landing pages, you can set the order for the landing pages. The lower the order, the higher the precedence in displaying the pages.

<table id="table_znp_cdb_34b"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

As a coach, you can analyze real-time data such as:-   The quality of how agents resolved incidents.
-   The mean time it took to resolve the incidents.
-   The trends in customer satisfaction, the type of skills used to resolve incidents, and completed assessments.
-   List of overdue training and assessments.

</td><td>

sn\_coaching.coach

</td></tr></tbody>
</table>## Use cases

As a coach, you can monitor the quality of agents resolving issues and take corrective actions by assessing their ability to resolve skills and provide them with training to address their skill gaps.

## Indicators

|Indicator name|Description|
|--------------|-----------|
|CSAT|Average customer satisfaction based on CSAT survey results.|
|Quality|Average score, in percentage, of all surveys taken by the coach to assess the trainee.|
|Incident Mean Time to Resolve|Average time agents have taken to work on an incident until they've marked it as closed or resolved.|
|Completed Assessment|Assessment closed over time.|

## Breakdowns

-   Assigned to
-   Assignment group

## Data visualizations

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Trainings|List![List](../../../reuse/reporting/image/score-list-tile.svg)|Assigned Training \[sn\_coaching\_assessment\_recommended\_learning\]|List of training that agents need to complete.|
|Coaching Assessments|List![List](../../../reuse/reporting/image/score-list-tile.svg)|Assessed Record \[sn\_coaching\_assessed\_records\]|List of assessments that coaches need to complete for their agents.|

**Parent Topic:**[Workforce Optimization for ITSM landing pages](../../../product/configurable-workforce-optimization-itsm/concept/configurable-wfo-itsm-landing-pages.md)


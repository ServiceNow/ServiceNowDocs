---
title: Accept an improvement
description: Accept and assign a new improvement request so it can be assessed for approval. You can reject the improvement request if it does not align with company strategic objectives.
locale: en-US
release: yokohama
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing improvements, Continual Improvement Management, IT Service Management]
---

# Accept an improvement

Accept and assign a new improvement request so it can be assessed for approval. You can reject the improvement request if it does not align with company strategic objectives.

## Before you begin

Role required: sn\_cim.improvement\_manager, sn\_cim.improvement\_coordinator

## About this task

![CIM accept and assign initiative](../image/cim-accepted.png "Continual Improvement Management")

Precondition: Improvement Requester created an improvement request.

## Procedure

1.  Identify the new improvement request.

    1.  Navigate to **Continual Improvement** &gt; **Open**.

    2.  In the Improvement Register list, open an improvement in the **New** state.

2.  Align the improvement request with company strategic objectives, and assign an Improvement Coordinator.

    1.  On the Improvement Initiative form, unlock the **Strategies** field to access your company strategic objectives, then click the lookup list.

    2.  Select the [enterprise strategy](https://www.servicenow.com/docs/access?context=overview-business-planning&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) aligned with the improvement request.

        **Note:** Only the Improvement Manager can create a strategy.

    3.  Click the **CIM Coordinator** lookup list and select an Improvement Coordinator to manage the improvement.

3.  Complete the fields for business service, business process, priority, effort estimate, benefits, and why this improvement is important.

4.  In the header bar, click **Accept** to progress the improvement request to the **Assess** state.

    Improvement Coordinator is notified of assignment.

5.  Complete the content in the Goals, Details, and Schedule tabs on the Improvement Initiative form.


## Accept improvement request

In the process of reviewing KPI performance in the Performance Analytics application, the incident manager noticed the **Average time to resolve an incident** KPI scorecard was too high \(24 hours\).

As part of the acceptance process, the Improvement Manager determined that KPI performance improvement aligned with the Automation/Effort Reduction strategic objective, assigned the Improvement Coordinator that drives KPI improvements, and accepted the improvement request.

|Field|Value|
|-----|-----|
|Number|CIM0000135 \(set internally\)|
|Business service|IT Services|
|Business Process|Incident Management|
|CIM Coordinator|Adela Cervantsz|
|Approver Group|CIM Approvers|
|Strategies|Automation/Effort Reduction|
|State|Accepted|
|Priority|4 - Low|
|Effort estimate|Medium|
|Benefits|High|
|Percent complete|0|
|Short description|Improve average time to resolve an incident by 25%|
|Business justification|Average time to resolve an incident time is bad compared to Industry average. I compared our value with global values from companies in the same industry using the Benchmarks application.|

|Field|Value|
|-----|-----|
|Success measurement method|Automated: PA Indicator|
|Improvement KPI|Average close time of incidents|
|Breakdown|--|
|Aggregation|--|
|Base value|100|
|Percentage improvement|25|
|Target value|75|
|Target review date|2018-06-30|
|Expected outcomes|Improvement in average time to resolve an incident.|

|Field|Value|
|-----|-----|
|Requested for|Mabel Weeden|
|Type|Process|
|Watch list|--|

|Field|Value|
|-----|-----|
|Planned start date|2018-03-18|
|Planned end date|2018-06-19|
|Actual start date|2018-03-11|
|Actual end date|--|

|Field|Value|
|-----|-----|
|Additional comments \(Customer visible\)|--|
|Work notes|--|

**Parent Topic:**[Managing improvements](../concept/cim-improvement-initiative-mgmt.md)

**Related topics**  


[Improvement field descriptions](../reference/cim-field-descriptions.md)


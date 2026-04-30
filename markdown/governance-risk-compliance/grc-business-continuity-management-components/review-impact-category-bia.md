---
title: Review an impact category and assess its recovery time
description: Review the impact categories and define the timeframe during which the organization would experience the downtime of its business processes. Analyze the downtime or disruption duration, which helps to determine the recovery time objective for the asset that is assessed.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Assess impact categories and dependencies of process, Structured workflows for BIA, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Review an impact category and assess its recovery time

Review the impact categories and define the timeframe during which the organization would experience the downtime of its business processes. Analyze the downtime or disruption duration, which helps to determine the recovery time objective for the asset that is assessed.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

BCM administrators configure the impact categories that are relevant to your business. For more information on configuring an impact category in the classic BCM workspace, see [Configure an impact rating to assess an impact category](configure-impact-rating-bcp.md) and [Structured workflows for Business Impact Analysis](../concept/structured-workflows-bia.md).

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Select the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  In the **Name** column, select the link to the BIA record that is in the **In Draft** state.

    An impact assessment is displayed as shown in the example.![Impact assessment.](../image/impact-rating-ws.png)

4.  To update a business impact category with its recovery time, select the **RTO Impact Assessment** tab.

    The state of the impact category changes to **Pending** and the grid is editable.

5.  Double-click the **Disruption Duration** cell for each Impact rating.

    Disruption duration is an estimated duration of the disruption that is based on your responses to the assessment questions and your subject matter expertise. If you’re the BIA owner, you have to select the right disruption duration based on your responses to the assessment questions and your subject matter expertise. The disruption duration is used for calculating the recovery time objective \(RTO\).

6.  Select the duration from the list that pops up depending on the criticality of the impact.

    The system prompts you to complete entering the disruption duration for all impact ratings of an impact category.

    The list of values displays only those durations that are configured as applicable timeframes for the recovery time objective \(RTO\) type impact category.

7.  Select the **Disruption Duration** cell of the next Impact Rating to enter its value and save similarly.

8.  Select the **Complete** button after you’ve assessed the duration for all impact ratings of an impact category.

    The state changes to **Complete** and is closed for editing unless you select the **Edit** button again.


**Parent Topic:**[Assess impact categories and dependencies of a process](assess-impact-categories-bia.md)


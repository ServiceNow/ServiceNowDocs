---
title: Assess RPO impact of technology assets on the business
description: Use the RPO impact assessment tab to enter asset information. The information can be critical from the objective of its recovery, the data value of the asset, and the frequency at which the data changes in the asset.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assess impact categories and dependencies of process, Structured workflows for BIA, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Assess RPO impact of technology assets on the business

Use the RPO impact assessment tab to enter asset information. The information can be critical from the objective of its recovery, the data value of the asset, and the frequency at which the data changes in the asset.

## Before you begin

Role required: sn\_bcm.program\_manager or sn\_bcm.planner

## About this task

Not all elements require data backup, however technology assets like IT hardware and software require data backup due to the critical information content.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon.](../../grc-workspace-audit/image/ListsIcon.jpg)\).

    By default the records in the **In Draft** state of the Business Impact Analysis list opens.

3.  To create a business impact analysis \(BIA\) record, click **New**.

4.  To update an existing BIA, click the link to the record in the **Name** column.

5.  To assess a BIA of its recovery point objective, click the **RPO Impact Assessment** tab.

    The **RPO Impact Assessment** tab appears only if you, as a BCM administrator, had set the **Requires data backup** field as **Yes** in the [Configure element definitions for Business Continuity Management](configure-element-definitions.md).

6.  Enter the data value of the asset in terms of its RPO impact on the business in the **Response** cell of the Data Value grid.

7.  Click **Complete**.

8.  To mention the frequency at which the data changes in the asset, enter your response to the questions in the Data Change Frequency grid.

9.  Click **Complete** after you answer all the RPO related questions.


## Result

Calculation of **Recovery Point Objective \(RPO\)** for **Impact Assessment Result**

If the impact category contributes to RPO, then the RPO calculation is as follows:

RPO depends on the rating or the response that you give for each question in the impact category of RPO Impact Assessment.

![Responses provided for RPO Impact Assessment](../image/RPOImpactAssessment.png "RPO assessment result")

Based on your response that you have selected for each Impact analysis question of an impact category, the system calculates the RPO.

For example, if two questions have a Medium \(value is 20\) response and one question has High \(value is 30\) as response, then the system considers the response whose value is maximum. Hence, in this case the impact rating is considered as High and the value is 30.

The impact rating has an integer value preconfigured in the Impact Rating table \[sn\_bcm\_impact\_rating\]. This value is updated as the **Category score** for the corresponding impact category in the Impact Category Results table \[sn\_bia\_category\_result\]. The system picks up the maximum category score across all impact categories. This score falls within a range of lower and upper threshold values. The threshold range within which the maximum score falls corresponds to a timeframe, which is stamped as **Recovery Point Objective \(RPO\)** in the **Impact Assessment Result** card of the BIA.

![The RPO value, calculated based on the responses provided, displays on the Impact Assessment Result card.](../image/RPOCalculation.png "RPO value in Impact Assessment Result card")

The mapping results of the threshold score and the timeframe are stored in the Score timeframe mapping table \[sn\_bia\_score\_timeframe\_mapping\].


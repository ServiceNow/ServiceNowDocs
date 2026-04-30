---
title: RTO, RPO, and recovery tiers
description: Due to unforeseen disruptive events, the business processes in your organization can face a downtime. It is important to classify your business processes in the recovery tiers and calculate the amount of time and amount of data loss that your organization can handle without significant effect on the operations.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# RTO, RPO, and recovery tiers

Due to unforeseen disruptive events, the business processes in your organization can face a downtime. It is important to classify your business processes in the recovery tiers and calculate the amount of time and amount of data loss that your organization can handle without significant effect on the operations.

## Recovery time objective

Recovery time objective \(RTO\) is the maximum amount of time a computer, system, network, or application takes to recover after an outage event or data loss without causing much effect to your business operations.

The business users and IT owners can perform business impact analysis and technical impact analysis respectively by responding to the assessment in the BIA component in the BCM UIB Workspace. A sample view of the **Assessments** tab is shown in the following example.

![Assessments in the BIA.](../image/bia-assessments-tab.png)

If you are the business user, you can estimate the recovery time objective for your business services and processes by responding to the Recovery time objective assessment in the **Assessments** tab. The questions are displayed in the **Recovery time objective assessment** tab according to the configuration set up by the BCM administrator. A sample Recovery time objective assessment with demo data is shown in the following example.

![Recovery time objective assessment.](../image/rto-assessment-questions.png)

## Recovery point objective

Recovery point objective \(RPO\) defines the maximum acceptable data loss that a business process can handle without significant effect on operations.

If you are the IT owner, you can estimate the recovery point objective for your data applications and systems by responding to the Recovery point objective assessment in the BIA. Based on the configuration set up by the BCM administrator, the questions are displayed in the **Recovery time objective assessment** tab as shown in the following example.

![Recovery point objective assessment.](../image/rpo-assessment-questions-1.png)

## Recovery tier

If you are the BCM administrator, you can classify a set of business applications that follow a similar range of recovery time objective \(RTO\) values in one type of recovery tier. For example, for the Mission Critical recovery tiers, recovery time objectives can be Immediately, one Hour, and four Hours.

The recovery tiers and their associated recovery time objectives are displayed in the following example.

![Recovery tiers and their configured recovery time objectives.](../image/recovery-tiers-rto.png)

The BCM administrator can configure a recovery tier and set its recovery time objective as shown in the following example.

![Recovery tier and its recovery time objective.](../image/new-recovery-tier-rto.png)

Recovery tiers are also associated with other organizational expectations such as levels of support, escalation, and communication. Recovery tiers are used in the following areas:

-   BIA scores and impact assessment result
-   Element recovery times

Although there is no limitation to the number of the recovery tiers, an organization can set 4 to 6 recovery tiers. Recovery tiers are automatically calculated on BIAs and element RTO by selecting the nearest recovery tier maximum time.

Recovery tiers can be classified as per their importance and criticality:

-   Mission Critical
-   Business Critical
-   Essential
-   Non-essential
-   Critical
-   Non-Critical

## Recovery tier configuration by the administrators

For more information on how to configure a recovery tier in the Business Continuity Management application, see [Configure recovery tiers for BIA](../task/configure-recovery-tier-bia-uib-ws.md).

## Recovery timeframe

You can set up the recovery timeframe for a recovery tier. It is the timeframe that starts from when a disruptive event happens to the time when your business can resume usual operations. The BCM administrator can configure the recovery timeframe and its start time. You can configure different recovery timeframes as shown in the following example:

-   Immediately
-   1 Hour
-   4 Hours
-   8 Hours
-   24 Hours
-   72 Hours
-   1 Week
-   2 weeks

The following example shows the configured recovery timeframes in the Business Continuity Management application. ![Recovery timeframes.](../image/recovery-timeframes.png)

The following example shows the configuration of a recovery timeframe in the Business Continuity Management application. ![New recovery timeframe.](../image/new-recovery-timeframe.png)

For more information on how to configure a recovery timeframe in the Business Continuity Management application, see [Set up recovery timeframe for a recovery tier](../task/configure-recovery-timeframe-bcm.md).

**Parent Topic:**[Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md)


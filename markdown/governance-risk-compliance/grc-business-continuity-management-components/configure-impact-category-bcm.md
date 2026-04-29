---
title: Configure an impact category for Business Continuity Management
description: Configure an impact category to define the timeframe during which the organization would experience a downtime of its business processes. Based on the timeframe, you can determine the recovery time objective \(RTO\) of the assets that the business process depends on.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [BCM in the Classic Workspace, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure an impact category for Business Continuity Management

Configure an impact category to define the timeframe during which the organization would experience a downtime of its business processes. Based on the timeframe, you can determine the recovery time objective \(RTO\) of the assets that the business process depends on.

## Before you begin

Role required: sn\_bcm.admin

## About this task

Recovery time objective \(RTO\) measurement helps to verify the key points:

-   Assets are recovered in time to support any parent dependencies.
-   Identify gaps in asset recovery capabilities.
-   Prioritize asset recovery if there is a loss scenario.

While RTO calculates the acceptable time by which the business function is restored, Recovery Point Objective \(RPO\) confirms that the maximum tolerable data loss for a function is not exceeded.

## Procedure

1.  Navigate to **Business Continuity** &gt; **General Administration** &gt; **Impact Categories**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the impact category.|
    |Contributes to|Contribution to RPO or RTO as a result of the impact on business disruption. If the impact category contributes to Recovery Point Objective, then the Impact analysis questions related list appears.|
    |Applicable timeframes|Duration of business process disruption. This field appears only if the **Contributes to** field value is RTO.|
    |Maximum RTO value|Metric that calculates the maximum time limit within which the business must recover an element after a disruption.|
    |Description|Brief description of the impact category.|

4.  Click **Submit**.

5.  If your impact category contributes to the recovery point objective, click the record that you created in the Impact Categories list.

    1.  Click **New** in the Impact analysis questions related list.

    2.  Enter an impact question on the impact category in the **Question** field.

        The Impact category field auto-populates the category of business impact.

    3.  Enter a short description about the impact analysis question in the **Description** field.

    4.  Click **Submit**.



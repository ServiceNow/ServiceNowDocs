---
title: Configure recovery tier for impact assessment
description: Configure and use recovery tier to assign a single recovery time and name to a similar range of recovery time objective \(RTO\) values.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [BCM in the Classic Workspace, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure recovery tier for impact assessment

Configure and use recovery tier to assign a single recovery time and name to a similar range of recovery time objective \(RTO\) values.

## Before you begin

Role required: sn\_bcm.admin

## About this task

Recovery tiers are also associated with other organizational expectations such as levels of support, escalation, and communication.

Recovery tiers are used in these areas:

-   BIA scores and impact assessment result.
-   Element recovery times.

Some examples of recovery tiers include:

-   Tier 1 – Mission Critical: 2 hours RTO.
-   Tier 5 – Non-Essential: 1 week RTO.

Although there is no limitation to the number of recovery tiers, an organization can set 4 to 6 recovery tiers.

**Note:** Recovery tiers are automatically calculated on BIAs and element RTO by selecting the nearest recovery tier maximum time.

## Procedure

1.  Navigate to **Business Continuity** &gt; **General Administration** &gt; **Recovery Tiers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the recovery tier level.|
    |Recovery time objectives|Metric that calculates how quickly the business should recover an element after a disaster.|

4.  Click **Submit**.



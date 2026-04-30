---
title: Risk score rollup in Advanced Risk Assessment
description: In Advanced Risk Assessment, risk scores are calculated across risk statement hierarchy, entity hierarchy, or a combination of both. These methods enable stakeholders to monitor their risk posture and provide visibility of the overall aggregated risk score.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Risk score rollup in Advanced Risk Assessment

In Advanced Risk Assessment, risk scores are calculated across risk statement hierarchy, entity hierarchy, or a combination of both. These methods enable stakeholders to monitor their risk posture and provide visibility of the overall aggregated risk score.

Before you understand the rollup feature, consider the following points:

-   Each entity might have multiple scores based on the different risk assessment methodologies.
-   Only the risk assessments in the **Monitor** state contribute to the risk score.
-   Each risk assessment methodology might have a different formula to calculate the rollup qualitative score and the rollup quantitative score. The formula is specified in the **Rollup configurations**section in the risk assessment methodology form.
-   Whenever the Advanced Risk plugin is activated the risk scores get rolled up.

## Risk statement hierarchy

Based on the assessments, the system automatically rolls up the inherent risk scores, the Annual Loss Expectancy \(ALE\), control effectiveness score, residual risk score, and ALE across the risk statement hierarchy for the selected methodology​. This rollup allows the risk managers to monitor their enterprise risk posture​.

## Entity hierarchy

Like risk statement hierarchy, the system also automatically rolls up the risk scores and ALE values across the entity hierarchy for a risk assessment methodology​. This rollup allows the entity owner to monitor the entity's risk posture. The rollups are done using the following formulae:

-   Sum
-   Average
-   Maximum
-   Minimum

## Entity hierarchy and risk statement

Using the Manage Aggregated Risk report, customers can define additional reporting dimensions on which they want to monitor the risk posture for an entity. For example, if you want to understand an internal fraud related risk for Retail Banking, you can define that reporting dimension and monitor the risk.

## Changes in reports and risk rollup method after migrating to Advanced Risk Assessment

To utilize the new rollup score calculation, the risk administrator, with the role sn\_risk.admin, must first enable the **Migrate to Advanced Risk Assessments** property by navigating to **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties**. This property is not enabled by default.

**Note:** It is crucial to note that when you enable the mentioned property, any customizations in the risk overview dashboard will be hidden. Contact ServiceNow for assistance. Also, the following properties in risk are not hidden when you migrate to advanced risk rollup:

-   Compare risk tolerance based on
-   Compare calculated risk score with

When customers migrate to Advanced Risk, the following reports are hidden from the user's view:

-   Aggregated Risk Report
-   Exposure by Entity
-   Exposure by Risk Statement

In the Risk Overview dashboard, the following tabs are hidden:

-   Entity Tolerance Status
-   Risk Tolerance Status
-   Aggregated Entity Information
-   Aggregated Risk Information

Under the Aggregated Risk Report, the following modules are visible that show the rolled up risk scores:

-   Aggregation by Risk Statements
-   Aggregation by Entities
-   Entity by Risk Statements

When you migrate to advanced risk assessment, individual risk score values do not roll up to give you the risk score. Instead, the values from advanced risk assessment are considered. For example, for an entity, in the Entity form, the Risk Rollup and Tolerance section is not displayed. The same applies to any risk statement. Instead, a related list called Aggregated Risk is displayed. The Aggregated Risk related list contains the following values derived from various risk assessments:

-   Risk assessment methodology
-   Residual rating
-   Inherent rating
-   Control effectiveness
-   Residual ALE
-   Inherent ALE
-   Contributing risk assessments
-   Risk rollup status

**Parent Topic:**[Advanced Risk Assessment](advanced-risk-assessment.md)


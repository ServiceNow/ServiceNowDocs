---
title: Risk score rollup in Advanced Risk Assessment
description: In Advanced Risk Assessment, risk scores are calculated across risk statement hierarchy, entity hierarchy, or a combination of both. These methods enable stakeholders to monitor their risk posture and provide visibility of the overall aggregated risk score.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/risk-rollup-ara-concept.html
release: brazil
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-11-11"
reading_time_minutes: 4
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Risk score rollup in Advanced Risk Assessment

In Advanced Risk Assessment, risk scores are calculated across risk statement hierarchy, entity hierarchy, or a combination of both. These methods enable stakeholders to monitor their risk posture and provide visibility of the overall aggregated risk score.

Before you understand the rollup feature, consider the following points:

-   Each entity might have multiple scores based on the different risk assessment methodologies.
-   Only active risk assessments in the **Monitor** state contribute to the risk score. Assessments in Closed, Cancelled, or any earlier state are excluded.
-   Each risk assessment methodology might have a different formula to calculate the rollup qualitative score and the rollup quantitative score. The formula is specified in the **Rollup Configurations** section in the risk assessment methodology form.
-   Risk scores are rolled up only when rollup is turned on. See [When rollup runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-rollup-ara-concept.md).

## When rollup runs

Rollup is calculated by a scheduled job, **GRC rollup assessment scores**, which runs every 5 minutes. The job calculates nothing unless one of these settings is on: the rollup migration setting that the **Migrate to Advanced Risk Assessments** property turns on, or the separate setting **Enable risk rollup for advanced risk assessments**. Changes to assessments are picked up on the job's next run.

## Primary risk assessment methodology

Rollup is calculated for every risk assessment methodology that applies to an entity, and the primary methodology is listed first. Only two places follow the primary methodology: the rollup result linked to the entity, and the risk assessment instance linked to the risk. The other methodologies' results are still calculated and listed.

When the primary methodology for an entity class changes, the entity's linked result and the linked risks are updated by business rules. They do not wait for the rollup job.

## Risk statement hierarchy

Based on the assessments, the system automatically rolls up the inherent risk scores, the Annual Loss Expectancy \(ALE\), control effectiveness score, target score, residual risk score, and ALE across the risk statement hierarchy for the selected methodology. A risk statement's rollup includes the statement itself and every statement below it in the hierarchy. Inactive statements are not excluded. This rollup allows the risk managers to monitor their enterprise risk posture.

## Entity hierarchy

Like risk statement hierarchy, the system also automatically rolls up the risk scores and ALE values across the entity hierarchy for a risk assessment methodology. This rollup allows the entity owner to monitor the entity's risk posture. An entity's rollup includes the entity itself and every downstream entity. Inactive downstream entities, and everything below them, are excluded.

Both hierarchies use the same score options:

-   Average
-   Maximum
-   Minimum
-   Worst case

Worst case selects one contributing risk assessment and copies all of its score values. It picks the assessment with the highest residual score. If no residual score is assessed, it picks the lowest control score, then the highest inherent score. Ties are resolved by the lowest control score, then the highest inherent score, then the lowest target score.

For example, if assessment A has inherent 1 and residual 5, and assessment B has inherent 5 and residual 3, Maximum gives inherent 5 and residual 5. Worst case gives inherent 1 and residual 5, because it copies assessment A.

ALE is calculated by a separate rule, so the ALE values in a worst case result can come from a different assessment than the scores.

Sum is available only for ALE.

## Entity hierarchy and risk statement

Using the Manage Aggregated Risk report, customers can define additional reporting dimensions on which they want to monitor the risk posture for an entity. For example, if you want to understand an internal fraud related risk for Retail Banking, you can define that reporting dimension and monitor the risk.

## Changes in reports and risk rollup method after migrating to Advanced Risk Assessment

To utilize the new rollup score calculation, the risk administrator, with the role sn\_risk.admin or sn\_risk.implementation\_admin, enables the **Migrate to Advanced Risk Assessments** property by navigating to **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties**. This property is not enabled by default. Enabling it also turns on the rollup migration setting, which is not shown on the Properties page.

**Note:** After you enable this property, you can't disable it, and the rollup migration setting it turns on can't be disabled either. Trying to disable it shows the message "You cannot disable advanced risk assessment after it is activated."

**Note:** It is crucial to note that when you enable the mentioned property, any customizations in the risk overview dashboard are hidden. Contact ServiceNow for assistance. The properties **Compare risk tolerance based on** and **Compare calculated risk score with** stay listed on the Properties page. Changing either one shows the message that it is no longer applicable because you have migrated to advanced risk.

When customers migrate to Advanced Risk, the following reports are deactivated:

-   Aggregated Risk Report
-   Aggregated Risk Report Management

The following aggregation modules remain visible and show the rolled up risk scores:

-   Aggregation by Risk Statements
-   Aggregation by Entities
-   Entity by Risk Statements

When you migrate to advanced risk assessment, individual risk score values do not roll up to give you the risk score. Instead, the values from advanced risk assessment are considered. For example, for an entity, the Entity form no longer shows the Risk Rollup and Tolerance section, and the same applies to any risk statement. Instead, a related list called Aggregated risks is displayed. The Aggregated risks related list contains the following values derived from various risk assessments:

-   Risk assessment methodology
-   Residual rating
-   Inherent rating
-   Control effectiveness
-   Residual ALE
-   Inherent ALE
-   Contributing risk assessments
-   Risk rollup status

**Parent Topic:**[Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/advanced-risk-assessment.md)


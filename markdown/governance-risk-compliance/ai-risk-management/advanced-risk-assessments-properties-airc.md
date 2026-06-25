---
title: Set up Advanced Risk assessments properties
description: Enable Advanced Risk Assessments \(ARA\) to confirm that risk‑based assessments and risk score roll‑up function correctly in the AI Risk and Compliance application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/advanced-risk-assessments-properties-airc.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 2
keywords: [Advanced Risk Assessments, migrate to advanced risk, risk score roll-up, AI Risk and Compliance]
breadcrumb: [Configure, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Set up Advanced Risk assessments properties

Enable Advanced Risk Assessments \(ARA\) to confirm that risk‑based assessments and risk score roll‑up function correctly in the AI Risk and Compliance application.

## Before you begin

Make sure that the Advanced Risk application is installed. You don't need to install the Advanced Risk application separately if you're using AI Control Tower.

If the **Migrate to Advanced Risk Assessments** property is already enabled, AI Control Tower uses the same configuration, and no further setup is required.

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin

## About this task

Advanced Risk Assessments \(ARA\) is a system-level configuration in AI Risk and Compliance that enables modern, risk-based assessment capabilities, including aggregated risk scoring across AI assets. This setting determines whether the platform uses legacy risk calculations or the Advanced Risk Assessments framework, which is required for risk score roll-up and risk aggregation in dashboards. Enabling this property is a one-way action and should be planned carefully during initial setup.

**Important:**

After you enable the **Migrate to Advanced Risk Assessments** property, you can't revert to legacy risk calculation. This property is set to **No** by default.

To confirm risk-based assessments on AI assets and risk roll-up function correctly in AI Risk and Compliance, the **Migrate to Advanced Risk Assessments** property must be enabled. If the property is set to **No**, AI Risk and Compliance doesn't consider risk score roll-up.

When **Migrate to Advanced Risk Assessments** is set to **Yes**:

-   Supports risk‑based assessments for AI assets.
-   Publish default Risk Assessment Methodologies \(RAMs\) and create and use custom RAMs.
-   Calculates aggregated risk scores by rolling up risk scores across AI assets.
-   Includes aggregated risk scores on the Risk and Compliance dashboards.

When **Migrate to Advanced Risk Assessments** is set to **No**:

-   Supports risk‑based assessments for AI assets.
-   Risk score roll-up isn't supported for risk-based assessments on AI assets. As a result, rolled-up risk scores aren't displayed in the AI Risk and Compliance dashboards.

For descriptions of all available Advanced Risk properties, see [Advanced Risk properties reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/advanced-risk-properties-ref.md).

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments** &gt; **Properties**.

2.  Set the **Migrate to Advanced Risk Assessments** property to **Yes**.

    \[Omitted image "ara-property-airc.png"\] Alt text: Migrate to Advanced Risk Assessments property.

3.  Select **Save**.


**Related topics**  


[Risk score rollup in Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-rollup-ara-concept.md)

[Advanced Risk properties reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/advanced-risk-properties-ref.md)


---
title: Set up Advanced Risk assessments properties
description: Enable Advanced Risk Assessments \(ARA\) to confirm that risk‑based assessments and risk score roll‑up function correctly in the AI Risk and Compliance application.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-02-09"
reading_time_minutes: 3
breadcrumb: [Configure, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Set up Advanced Risk assessments properties

Enable Advanced Risk Assessments \(ARA\) to confirm that risk‑based assessments and risk score roll‑up function correctly in the AI Risk and Compliance application.

## Before you begin

Make sure that the Advanced Risk application is installed. You don't need to install the Advanced Risk application separately if you’re using AI Control Tower.

If the **Migrate to Advanced Risk Assessments** property is already enabled, AI Control Tower uses the same configuration, and no further setup is required.

Role required: AI Risk and Compliance Admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\]

## About this task

Advanced Risk Assessments \(ARA\) is a system-level configuration in AI Risk and Compliance that enables modern, risk-based assessment capabilities, including aggregated risk scoring across AI assets. This setting determines whether the platform uses legacy risk calculations or the Advanced Risk Assessments framework, which is required for risk score roll-up and risk aggregation in dashboards. Enabling this property is a one-way action and should be planned carefully during initial setup.

**Important:**

After you enable the **Migrate to Advanced Risk Assessments** property, you can’t revert to legacy risk calculation. This property is set to **No** by default.

To confirm risk-based assessments on AI assets and risk roll-up function correctly in AI Risk and Compliance, the **Migrate to Advanced Risk Assessments** property must be enabled. If the property is set to **No**, AI Risk and Compliance doesn't consider risk score roll-up.

When **Migrate to Advanced Risk Assessments** is set to **Yes**:

-   Supports risk‑based assessments for AI assets.
-   Publish default Risk Assessment Methodologies \(RAMs\) and create and use custom RAMs.
-   Calculates aggregated risk scores by rolling up risk scores across AI assets.
-   Includes aggregated risk scores on the Risk and Compliance dashboards.

When **Migrate to Advanced Risk Assessments** is set to **No**:

-   Supports risk‑based assessments for AI assets.
-   Risk score roll-up isn’t supported for risk-based assessments on AI assets. As a result, rolled-up risk scores aren’t displayed in the AI Risk and Compliance dashboards.

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments** &gt; **Properties**.

2.  On the Advanced Risk Properties form, fill in the fields:

<table id="table-create-metric"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Migrate to Advanced Risk Assessments

 \[sn\_risk\_advanced.hide\_risk\_legacy\_lifecycle\]

</td><td>

Enables the Advanced Risk Assessment \(ARA\) framework in the instance. When enabled, all risk assessments use Risk Assessment Methodologies \(RAMs\), advanced scoring, and rollups.

</td></tr><tr><td>

Define risk appetite

 \[sn\_risk\_advanced.risk\_appetite\_scale\]

</td><td>

Specifies how risk appetite is evaluated during assessments.

</td></tr><tr><td>

Express risk appetite limits in

 \[sn\_risk\_advanced.risk\_appetite\_analysis\]

</td><td>

Determines how appetite thresholds are expressed. Whether limits are qualitative, quantitative, or both.

</td></tr><tr><td>

Enable Advanced Risk PPM Integration

 \[sn\_risk\_advanced.enable\_advanced\_risk\_ppm\_integration\]

</td><td>

Enables integration between Advanced Risk and Project Portfolio Management \(PPM\).

</td></tr><tr><td>

Number of days before which an email should be sent to review risk appetite

 \[sn\_risk\_advanced.risk\_appetite\_review\_notifcation\]

</td><td>

Defines advance notification timing for risk appetite reviews. Number of days before the review date that reminder emails are sent.

</td></tr><tr><td>

Field from the risk table that will be displayed as the header for each risk in the focus mode of the risk assessment project

 \[sn\_risk\_advanced.assessment\_heading\_risk\_field\_name\]

</td><td>

Controls which risk attribute is shown as the header in Focus Mode.

</td></tr><tr><td>

This string contains the default column details for individual control assessments. The listed columns can be customized or modified as needed. The default columns include classification, weighting, status, and key\_control.

 \[sn\_risk\_advanced.grid\_individual\_control\_assessment\_columns\]

</td><td>

Defines the default columns shown when assessing individual controls.

</td></tr></tbody>
</table>3.  Set the **Migrate to Advanced Risk Assessments** property to **Yes**.

    ![Migrate to Advanced Risk Assessments property.](../image/ara-property-airc.png)

4.  Select **Save**.


**Related topics**  


[Risk score rollup in Advanced Risk Assessment](../../grc-risk/concept/risk-rollup-ara-concept.md)


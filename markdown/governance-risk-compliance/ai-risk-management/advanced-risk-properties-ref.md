---
title: Advanced Risk properties reference
description: Reference for the Advanced Risk system properties available in the AI Risk and Compliance application, including the properties that control risk assessment methodology behavior, risk score roll-up, and risk appetite configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/advanced-risk-properties-ref.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-05-14"
reading_time_minutes: 2
keywords: [Advanced Risk, risk assessment properties, migrate to advanced risk assessments, risk appetite, AI Risk and Compliance, system properties]
breadcrumb: [Reference, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Advanced Risk properties reference

Reference for the Advanced Risk system properties available in the AI Risk and Compliance application, including the properties that control risk assessment methodology behavior, risk score roll-up, and risk appetite configuration.

The following table describes the Advanced Risk properties available in AI Risk and Compliance. These properties are configured by navigating to **All** &gt; **AI Risk and Compliance** &gt; **Risk Assessments** &gt; **Properties**. For the procedure to enable Advanced Risk Assessments, see [Set up Advanced Risk assessments properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/advanced-risk-assessments-properties-airc.md).

**Important:** The **Migrate to Advanced Risk Assessments** property is a one-way configuration change. After it is set to **Yes**, it cannot be reverted to legacy risk calculation.

<table id="table_ara_properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Migrate to Advanced Risk Assessments

 \[sn\_risk\_advanced.hide\_risk\_legacy\_lifecycle\]

</td><td>

Enables the Advanced Risk Assessment \(ARA\) framework in the instance. When enabled, all risk assessments use Risk Assessment Methodologies \(RAMs\), advanced scoring, and roll-ups. This is a one-way change and cannot be reverted.

</td></tr><tr><td>

Define risk appetite

 \[sn\_risk\_advanced.risk\_appetite\_scale\]

</td><td>

Specifies how risk appetite is evaluated during assessments.

</td></tr><tr><td>

Express risk appetite limits in

 \[sn\_risk\_advanced.risk\_appetite\_analysis\]

</td><td>

Determines how appetite thresholds are expressed — whether limits are qualitative, quantitative, or both.

</td></tr><tr><td>

Number of days before which an email should be sent to review risk appetite

 \[sn\_risk\_advanced.risk\_appetite\_review\_notifcation\]

</td><td>

Defines advance notification timing for risk appetite reviews. Sets the number of days before the review date that reminder emails are sent.

</td></tr><tr><td>

Field from the risk table that will be displayed as the header for each risk in the focus mode of the risk assessment project

 \[sn\_risk\_advanced.assessment\_heading\_risk\_field\_name\]

</td><td>

Controls which risk attribute is shown as the header in Focus Mode during bulk risk assessments.

</td></tr><tr><td>

Default column details for individual control assessments

 \[sn\_risk\_advanced.grid\_individual\_control\_assessment\_columns\]

</td><td>

Defines the default columns shown when assessing individual controls in the grid view. The default columns include classification, weighting, status, and key\_control. These columns can be customized or modified as needed.

</td></tr></tbody>
</table>**Parent Topic:**[AI Risk and Compliance reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-reference.md)

**Related topics**  


[Set up Advanced Risk assessments properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/advanced-risk-assessments-properties-airc.md)


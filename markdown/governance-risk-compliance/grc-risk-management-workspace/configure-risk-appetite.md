---
title: Configure a risk appetite and tolerance in Advanced Risk
description: Set up the advanced risk assessment properties so that you can configure and customize the risk appetite and tolerance in the Advanced Risk application.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Risk appetite setup, Configure, Risk Management, Governance, Risk, and Compliance]
---

# Configure a risk appetite and tolerance in Advanced Risk

Set up the advanced risk assessment properties so that you can configure and customize the risk appetite and tolerance in the Advanced Risk application.

## Before you begin

Role required: sn\_risk.admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties**.

2.  Set the property values that are described in the following table.

<table id="table_aqy_k2x_rvb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Migrate to Advanced Risk Assessmentssn\_risk\_advanced.hide\_risk\_legacy\_lifecycle

</td><td>

Option to migrate to the advanced risk assessments. Select **Yes** to use the risk appetite feature.

</td></tr><tr><td>

Define risk appetite assn\_risk\_advanced.risk\_appetite\_scale

</td><td>

Option to select the risk appetite type:-   **Risk appetite only \(1-point scale\)**: Uses only the risk appetite. The risk appetite field is available on the risk statement, risk, and entity form. The risk appetite status is calculated based on this property selection.
-   **Risk appetite and risk tolerance \(2-point scale\)**:Uses both the risk appetite and tolerance. The risk appetite and risk tolerance fields are available on the risk statement, risk, and entity form. The risk appetite status is calculated based on this property selection.
-   **None**: Don't want to use the risk appetite.
 **Note:** Only one property between the **Define risk appetite as** and **Express risk appetite in** can be configured at a time. Configure a property first, save it, and then configure the other property.

</td></tr><tr><td>

Express risk appetite limits insn\_risk\_advanced.risk\_appetite\_analysis

</td><td>

Option to select risk appetite scale:-   **Qualitative terms only**: Defines the risk appetite in qualitative terms only. Your risk appetite is based on the appetite scale such as low, medium, or high. The risk ratings are compared with the qualitative appetite and tolerance to calculate the qualitative appetite status.
-   **Quantitative terms only**: Defines the risk appetite in quantitative terms only. A quantitative risk appetite can be measured and expressed using numerical values. For example, an organization decides to have $1000 \(US dollars\) as a target non-performing asset \(NPA\) for this year. The organization can define $1000 \(US dollars\) as a quantitative risk appetite. The annual loss expectancy values are compared with the quantitative appetite and tolerance to calculate the quantitative appetite status.
-   **Both**: Defines the risk appetite in both qualitative and quantitative terms.
 **Note:** Only one property between **Define risk appetite as** and **Express risk appetite in** can be configured at a time. Configure a property first, save it, and then configure the other property.

</td></tr><tr><td>

Number of days before which an email should be sent to review risk appetitesn\_risk\_advanced.risk\_appetite\_review\_notifcation

</td><td>

Notification email scheduler to send an automated email notification to the risk statement owner before the next review date.

</td></tr></tbody>
</table>3.  Select **Save**.


**Parent Topic:**[Risk appetite setup](../concept/risk-appetite-setup.md)


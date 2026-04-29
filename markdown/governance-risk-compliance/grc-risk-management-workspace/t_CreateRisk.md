---
title: Create a risk manually
description: Risk administrators can create risk records when they see a potential for a gain or loss of value.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk manually

Risk administrators can create risk records when they see a potential for a gain or loss of value.

## Before you begin

Role required: sn\_risk.user

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Register** &gt; **Create New**.

2.  On the form, fill in the fields.

<table id="table_k3p_wk3_tt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number. This field automatically populated.

</td></tr><tr><td>

Inherit from risk statement

</td><td>

Option to create a risk independent of risk statement.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the risk is active.

</td></tr><tr><td>

Name

</td><td>

Name for the risk. Field is auto-populated if the risk is generated from a risk statement, but can be changed without affecting the relationship between the risk and risk statement.

</td></tr><tr><td>

Description

</td><td>

Description of the risk and how it is a threat to the organization.

</td></tr><tr><td>

Risk Statement

</td><td>

Risk statement this risk is associated with.

</td></tr><tr><td>

Category

</td><td>

Category of risk which applies to the profile. -   Legal
-   Financial
-   Operational
-   Reputational
-   Legal/Regulatory
-   Credit
-   Market
-   IT
If the risk is generated from a risk statement, the field is automatically populated/

</td></tr><tr><td>

Entity

</td><td>

Entity related to the risk. **Note:** Only active entities are shown.

</td></tr><tr><td>

Sync with entity owner

</td><td>

Option to assign the entity owner as the owner of this risk record. When selected, if the entity owner changes, the risk owner is updated automatically. This option is set to **True** by default.

</td></tr><tr><td>

Owning group

</td><td>

Owning group for the risk.

</td></tr><tr><td>

Risk relevance

</td><td>

Explanation of how this risk applies to you. **Note:** This field only appears when the **Inherit from risk statement** option is selected.

</td></tr><tr><td>

Owner

</td><td>

Owner for the risk.**Note:** The owner is always added as a respondent.

</td></tr></tbody>
</table>3.  Select the **Assessment Summary** tab.

    This tab is only visible if you have the Advanced Risk plugin activated. The scores of the risk assessment methodology selected as the primary are displayed in the risk scoring section. If the Advanced Risk plugin is not activated, then the following sections for classic risk appear.

4.  To fill in the fields for the risk appetite section, see [Define the risk appetite for a risk](../../grc-workspace-risk/task/define-risk-appetite-on-risk.md).

5.  On the form, fill in the fields.

<table id="table_g4j_lyc_rw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Note:** These fields appear for classic risk.

</td></tr><tr><td>

Assessment

</td><td>

Assessment to attach to this risk.

</td></tr><tr><td>

Assessment respondents

</td><td>

Users assigned to the assessment of this risk.**Note:** Only a user with the sn\_grc.user role can be added as a respondent.

</td></tr></tbody>
</table>    When both the **Assessment** and **Assessment respondents** fields are set, assessments are created when you select **Assess**.

6.  Select the **Scoring** tab.

7.  On the form, fill in the fields.

<table id="table_itw_f3k_kv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Note:** These fields appear for classic risk.

</td></tr><tr><td>

Inherent SLE

</td><td>

Monetary value of a risk if it occurs before any mitigation strategies are in place.

</td></tr><tr><td>

Residual SLE

</td><td>

Monetary value of a risk if it occurs after all mitigation strategies are in place.

</td></tr><tr><td>

Inherent ARO

</td><td>

Probability that a risk occurs in any given year before any mitigation strategies are in place.

</td></tr><tr><td>

Residual ARO

</td><td>

Probability that a risk will occur in any given year after all mitigation strategies are in place.

</td></tr><tr><td>

Inherent ALE

</td><td>

Annualized loss expectancy `ALE = SLE x ARO` before any mitigation strategies are in place.

</td></tr><tr><td>

Residual ALE

</td><td>

Annualized loss expectancy `ALE = SLE x ARO` after all mitigation strategies are in place.

</td></tr><tr><td>

Inherent score

</td><td>

The score of the risk before any mitigation strategies are in place.

</td></tr><tr><td>

Residual score

</td><td>

The score of the risk after all mitigation strategies are in place.

</td></tr><tr><td>

Calculated ALE

</td><td>

Annualized loss expectancy based off all calculations.

</td></tr><tr><td>

Calculated score

</td><td>

The corresponding score for the calculated ALE.

</td></tr></tbody>
</table>8.  Select the **Response** tab.

9.  On the form, fill in the fields.

<table id="table_xq2_t3k_kv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response

</td><td>

-   Accept
-   Avoid
-   Mitigate
-   Transfer


</td></tr><tr><td>

Justification

</td><td>

Enter a reasonable justification for the selected response

</td></tr></tbody>
</table>10. Select the **Monitoring** tab.

    |Field|Description|
    |-----|-----------|
    |Control compliance percentage|Percentage of compliant controls|
    |Control non-compliance percentage|Percentage of non-compliant controls|
    |Control failure factor|Sum of failed controls weighting divided by total controls weighting|
    |Indicator failure factor|Uses the last result of each associated indicator. Number of last results failed divided by total number of indicators associated.|
    |Calculated risk factor|This value is calculated from `(Indicator failure factor + Control failure factor) / 2`.|

11. Select the **Activity Journal** tab.

12. Enter additional comments, as necessary.

13. Select **Submit**.


**Parent Topic:**[Using Risk Management](../concept/using-risk-mgmt.md)


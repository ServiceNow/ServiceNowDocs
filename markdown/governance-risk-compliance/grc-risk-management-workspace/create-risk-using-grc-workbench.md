---
title: Create a risk using the GRC: Workbench
description: Risk managers can create risks directly from the GRC: Workbench.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use entity and risk dependencies using the GRC: Workbench, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk using the GRC: Workbench

Risk managers can create risks directly from the GRC: Workbench.

## Before you begin

Role required: sn.\_risk.admin or sn.risk.manager

## Procedure

1.  Navigate to `https://myCompany.service-now.com/$grc_workbench.do`.

2.  Select the **Risk Dependencies** tab at the top, then select the **Relationships** tab below it.

3.  On the left, in the Risks section, click **Create Risk**.

4.  On the form, fill in the fields.

<table id="table_k3p_wk3_tt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the risk. Field is auto-populated if the risk is generated from a risk statement, but can be changed without affecting the relationship between the risk and risk statement.

</td></tr><tr><td>

Number

</td><td>

Unique identification number. This field is automatically populated.

</td></tr><tr><td>

State

</td><td>

Risk state. Possible choices are: -   **Draft** In this state, all risk users can modify the risk. Only available when creating a one-off control. One-off controls are possible but not recommended.
-   **Attest** When the risk is created from a risk statement, controls are in this state.

**Note:** When a risk is set back to draft, the assessment is canceled.

-   **Review** Risks are automatically moved to review from the assessment phase.
-   **Monitor** In this state, all risk managers can move the risk from review to monitor.
-   **Retired** Risk managers or administrators can move a risk from Monitor to Retired. Indicators do not run when the risk is in this state.

**Note:** When a risk is retired, any assessment associated with it is canceled.

</td></tr><tr><td>

Owning group

</td><td>

Owning group for the risk.

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
Field is auto-populated if risk is generated from a risk statement.

</td></tr><tr><td>

Owner

</td><td>

Owner for the risk.**Note:** The owner is always added as a respondent.

</td></tr><tr><td>

Statement

</td><td>

Statement this risk is associated with.

</td></tr><tr><td>

Entity

</td><td>

Entity related to the risk. **Note:** Only active entities are shown.

</td></tr><tr><td>

Description

</td><td>

Description of the risk and how it is a threat to the organization.

</td></tr><tr><td>

Additional Information

</td><td>

More details that help others understand the risk record.

</td></tr></tbody>
</table>5.  Click the **Assessment** tab.

6.  On the form, fill in the fields.

<table id="table_g4j_lyc_rw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment

</td><td>

Assessment to attach to this risk.

</td></tr><tr><td>

Assessment respondents

</td><td>

Users assigned to the assessment of this risk.**Note:** Only a user with the sn\_grc.user role can be added as a respondent.

</td></tr></tbody>
</table>    When both the **Assessment** and **Assessment respondents** fields are set, assessments are created when you click **Assess**.

7.  Click the **Scoring** tab.

8.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Inherent SLE|Monetary value of a risk if it occurs before any mitigation strategies are in place.|
    |Residual SLE|Monetary value of a risk if it occurs after all mitigation strategies are in place.|
    |Inherent ARO|Probability that a risk occurs in any given year before any mitigation strategies are in place.|
    |Residual ARO|Probability that a risk will occur in any given year after all mitigation strategies are in place.|
    |Inherent ALE|Annualized loss expectancy `ALE = SLE x ARO` before any mitigation strategies are in place.|
    |Residual ALE|Annualized loss expectancy `ALE = SLE x ARO` after all mitigation strategies are in place.|
    |Inherent score|The score of the risk before any mitigation strategies are in place.|
    |Residual score|The score of the risk after all mitigation strategies are in place.|
    |Calculated ALE|Annualized loss expectancy based off all calculations.|
    |Calculated score|The corresponding score for the calculated ALE.|

9.  Click the **Response** tab.

10. On the form, fill in the fields.

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
</table>11. Click the **Monitoring** tab.

    |Field|Description|
    |-----|-----------|
    |Control compliance|Percentage of compliant controls|
    |Control non-compliance|Percentage of non-compliant controls|
    |Control failure factor|Sum of failed controls weighting divided by total controls weighting|
    |Indicator failure factor|Uses the last result of each associated indicator. Number of last results failed divided by total number of indicators associated.|
    |Calculated risk factor|This value is calculated from `(Indicator failure factor + Control failure factor) / 2`.|

12. Click the **Activity Journal** tab.

13. Enter additional comments, as necessary.

14. Click **Submit**.

    The risk is created and centered in the middle of the page. Also, the risk is selected on the right.


**Parent Topic:**[Use entity and risk dependencies using the GRC: Workbench](../concept/grc-workbench.md)


---
title: Define risk statement hierarchy
description: Risk managers establish parent and child relationships on the risk statement form.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Risk Management, Governance, Risk, and Compliance]
---

# Define risk statement hierarchy

Risk managers establish parent and child relationships on the risk statement form.

## Before you begin

Role required: sn\_risk.manager

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Library** &gt; **Risk Statements**.

2.  Click **New**.

3.  On the form, fill in the fields.

    **Note:** When any of the following statement fields changes: Name, Description, Reference, Category, Type, Classification, and Attestation, all the associated controls and risks are updated, and their state is set back to Draft.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk statement.

</td></tr><tr><td>

Parent \* this field is visible only when Advanced Risk has been downloaded.

</td><td>

Parent risk statement to this risk statement.

-   Users select the appropriate parent from the taxonomy structure.
-   If no parent is specified, the risk statement becomes the root of the tree.
-   It is possible to have several of these root-type risk statements within the organization.
-   A risk statement cannot be both a parent and a child of another risk statement.


</td></tr><tr><td>

Framework

</td><td>

Framework this risk statement is associated with.

</td></tr><tr><td>

Category

</td><td>

Choose a category. -   Legal
-   Financial
-   Operational
-   Reputational
-   Legal/Regulatory
-   Credit
-   Market
-   IT


</td></tr><tr><td>

Assessment

</td><td>

Assessment associated with this risk statement.

</td></tr><tr><td>

Issue group rule

</td><td>

Issue group rule assigned to this risk statement for reporting and dashboard.

</td></tr><tr><td>

Description

</td><td>

Description of the risk statement.

</td></tr><tr><td>

Additional information

</td><td>

Additional information for this risk statement.

</td></tr><tr><td colspan="2">

Default Scores

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

</td></tr><tr><td colspan="2">

Risk Rollup and Tolerance \* this tab is visible only when Advanced Risk has been downloaded.

</td></tr><tr><td>

Expected ALE

</td><td>

Enter currency and amount for the expected ALE.**Note:** This value must be less than or equal to the **Maximum acceptable ALE**.

</td></tr><tr><td>

Maximum acceptable ALE

</td><td>

Enter currency and amount for the maximum acceptable ALE.**Note:** This value must be greater than or equal to the**Expected ALE**.

</td></tr><tr><td>

Sum of calculated ALE

</td><td>

This is a calculation based on all the underlying risks or risk statements.

</td></tr><tr><td>

Average calculated ALE

</td><td>

This is a calculation based on all the underlying risks or risk statements.

</td></tr><tr><td>

Maximum calculated ALE

</td><td>

This is a calculation based on all the underlying risks or risk statements.

</td></tr><tr><td>

Minimum calculated ALE

</td><td>

This is a calculation based on all the underlying risks or risk statements.

</td></tr><tr><td>

Tolerance Status

</td><td>

Automatically calculated based on tolerance values. -   If the **Calculated ALE** is less than or equal to the **Expected ALE** = Acceptable in green
-   If the **Calculated ALE** is greater than the **Expected ALE**, but less than or equal to the **Max acceptable ALE** = Needs Attention in orange
-   If the **Calculated ALE** is greater than the **Maximum acceptable ALE** = Unacceptable in red


</td></tr><tr><td>

Calculated Score

</td><td>

The corresponding score for the calculated ALE:-   Low
-   Med
-   High


</td></tr></tbody>
</table>4.  Click **Submit**.

5.  To add children risk statements, click the **Risk Statements** related list, and click **New**.

6.  Fill in the fields on the form, as appropriate and click **Submit**.

7.  Repeat until you have added all the children risk statements related to this risk statement.


**Parent Topic:**[Using Risk Management](../concept/using-risk-mgmt.md)


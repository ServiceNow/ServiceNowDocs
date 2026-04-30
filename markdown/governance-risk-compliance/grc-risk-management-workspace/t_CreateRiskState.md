---
title: Create a risk statement
description: Risk managers create risk statements to group risks into manageable categories.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk statement

Risk managers create risk statements to group risks into manageable categories.

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

Parent

</td><td>

Parent risk statement.

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

Risk assessment template to be assigned to this risk statement. An assessment template is a questionnaire that is used for assessing a risk.

</td></tr><tr><td>

Description

</td><td>

Description of the risk statement.

</td></tr><tr><td>

Additional information

</td><td>

Additional information for this risk statement.

</td></tr></tbody>
</table>    **Note:** Accurate default scoring selections are important for normalizing risk across the organization.

4.  To fill in the fields for the risk appetite section, see [Define the risk appetite for a risk statement](../../grc-workspace-risk/task/define-risk-appetite-on-risk-statement.md).

5.  Click the **Default Scores** related list and fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Inherent SLE|Impact that the event has on the organization if there are no controls to check the event.|
    |Residual SLE|Impact that the event has on the organization if there are controls to check the event.|
    |Inherent ARO|Likelihood of the event occurring if there are no controls to check the event.|
    |Residual ARO|Likelihood of the event occurring if there are controls to check the event.|

6.  Click the **Risk Rollup and Tolerance** related list and on the form, fill in the fields.

<table id="table_kyp_gs3_f3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expected ALE

</td><td>

Annual Loss of Expectancy \(ALE\) refers to the product of the annual rate of occurrence \(ARO\) and the single loss expectancy \(SLE\). Expected ALE is the expected value of the ALE for the risk statement. Enter currency and amount for the expected ALE.**Note:** This value must be less than or equal to the **Maximum acceptable ALE**.

</td></tr><tr><td>

Sum of calculated ALE

</td><td>

This calculation is based on the sum of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Maximum calculated ALE

</td><td>

This calculation is based on the maximum of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Maximum acceptable ALE

</td><td>

Threshold value for the ALE for the risk statement.**Note:** This value must be greater than or equal to the**Expected ALE**. This value has an impact on the Tolerance status field.

</td></tr><tr><td>

Average calculated ALE

</td><td>

This calculation is based on the average of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Minimum calculated ALE

</td><td>

This calculation is based on the minimum of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Calculated Score

</td><td>

The corresponding score for the calculated ALE:-   Low
-   Med
-   High


</td></tr></tbody>
</table>7.  Click the **Basel Categorization** related list and select the Basel Categories Hierarchy.

    The Basel categories are as follows:

    -   Internal Fraud: misappropriation of assets, tax evasion, intentional mismarking of positions, bribery.
    -   External Fraud: theft of information, hacking damage, third-party theft and forgery.
    -   Employment Practices and Workplace Safety: discrimination, workers compensation, employee health and safety.
    -   Clients, Products, and Business Practice: market manipulation, antitrust, improper trade, product defects, breaches, account churning.
    -   Damage to Physical Assets: natural disasters, terrorism, vandalism.
    -   Business Disruption and Systems Failures: utility disruptions, software failures, hardware failures.
    -   Execution, Delivery, and Process Management: data entry errors, accounting errors, failed mandatory reporting, negligent loss of client assets.
8.  Click **Submit**.


**Parent Topic:**[Using Risk Management](../concept/using-risk-mgmt.md)


---
title: Create a risk statement in the Risk Workspace
description: Create risk statements to group risks into manageable categories.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Create a risk framework in the Risk Workspace, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk statement in the Risk Workspace

Create risk statements to group risks into manageable categories.

## Before you begin

Role required: sn\_risk.admin

## About this task

When you create a risk statement, you can associate entity types or add additional entities to generate risks.

**Note:** When any of the following risk statement fields changes: Name, Description, Reference, Category, Type, Classification, and Attestation, all the associated controls and risks are updated, and their state is set back to Draft. All the associated risk assessments also get canceled.

## Procedure

1.  Navigate to **All** &gt; **Risk Workspace** &gt; **Library** &gt; **Risk statements**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk statement.

</td></tr><tr><td>

Description

</td><td>

Description of the risk statement.

</td></tr><tr><td>

Parent

</td><td>

Parent risk statement. You can define the hierarchy using this field.

</td></tr><tr><td>

Framework

</td><td>

Framework this risk statement is associated with.**Note:** This field only appears if the **Migrate to Advanced Risk Assessment** property is enabled. For more information, see [Risk score rollup in Advanced Risk Assessment](../../grc-risk/concept/risk-rollup-ara-concept.md)

</td></tr><tr><td>

Category

</td><td>

Category of the risk statement. The choices are as follows:-   Legal
-   Financial
-   Operational
-   Reputational
-   Legal/Regulatory
-   Credit
-   Market
-   IT
-   Project


</td></tr><tr><td>

Level

</td><td>

Level at which the risk statement is created. For example, if the risk statement has a parent and a grandparent, then the level of this new risk statement will be 3.

</td></tr><tr><td>

Assessment

</td><td>

Risk assessment template to be assigned to this risk statement. An assessment template is a questionnaire that is used for assessing a risk.**Note:** This field appears when you use classic risk with enabling the advanced risk property.

</td></tr><tr><td>

Issue group rule

</td><td>

Issue group rule assigned to this risk statement for reporting. The purpose of the issue group rule is to group similar issues together into a parent issue based on conditions defined in the rule. This feature enables you to work on the similar issues at once and close out the parent issue once resolved, which will close out all the child issues.

</td></tr><tr><td>

Additional information

</td><td>

Additional information for this risk statement.

</td></tr></tbody>
</table>4.  To fill in the fields for the risk appetite section, see [Define the risk appetite for a risk statement](define-risk-appetite-on-risk-statement.md).

5.  If you're using classic risk, in the Default Scores section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Inherent SLE|Single-loss expectancy \(SLE\) is the monetary value expected from the occurrence of a risk on an asset if there are no controls to check the event.|
    |Residual SLE|Monetary value expected from the occurrence of a risk on an asset if there are controls to check the event.|
    |Inherent ARO|Annualized rate of occurrence \(ARO\) is an estimated frequency of the threat occurring in one year. ARO is used to calculate annualized loss expectancy \(ALE\). The value in this field indicates the likelihood of the event occurring if there are no controls to check the event.|
    |Residual ARO|The value in this field indicates the likelihood of the event occurring if there are controls to check the event.|

6.  If you're using classic risk with the advanced risk plugin activated, in the **Risk Rollup and Tolerance** section, fill in the fields.

<table id="table_kyp_gs3_f3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expected ALE

</td><td>

ALE refers to the product of the ARO and the SLE. Expected ALE is the expected value of the ALE for the risk statement. Enter currency and amount for the expected ALE.**Note:** This value must be less than or equal to the **Maximum acceptable ALE**.

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

Threshold value for the ALE for the risk statement.**Note:** This value must be greater than or equal to the **Expected ALE**. This value has an impact on the **Tolerance status** field.

</td></tr><tr><td>

Average calculated ALE

</td><td>

This calculation is based on the average of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Minimum calculated ALE

</td><td>

This calculation is based on the minimum of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Tolerance Status

</td><td>

Overall risk status. This field appears when the other ALE fields are populated.

</td></tr><tr><td>

Calculated Score

</td><td>

The corresponding score for the calculated ALE:-   Low
-   Med
-   High


</td></tr></tbody>
</table>7.  In the Basel Categorization section, select the Basel Categories Hierarchy.

    The Basel categories are as follows:

    -   Internal Fraud: misappropriation of assets, tax evasion, intentional mismarking of positions, bribery.
    -   External Fraud: theft of information, hacking damage, third-party theft, and forgery.
    -   Employment Practices and Workplace Safety: discrimination, workers' compensation, employee health, and safety.
    -   Clients, Products, and Business Practice: market manipulation, antitrust, improper trade, product defects, breaches, account churning.
    -   Damage to Physical Assets: natural disasters, terrorism, vandalism.
    -   Business Disruption and Systems Failures: utility disruptions, software failures, hardware failures.
    -   Execution, Delivery, and Process Management: data entry errors, accounting errors, failed required reporting, negligent loss of client assets.
8.  Click **Save**.

9.  To add entity types, click the Entity types related list.

    1.  Click **Add**.

    2.  Select the entity types to add.

    3.  Click **Add**.

10. To add additional entities, click the **Additional entities** related list.

    1.  Click **Add**.

    2.  Select the entities to add.

    3.  Click **Add**.

11. Click **Save**.


## Result

The risk statement is created.

## What to do next

You can continue to add control objectives, indicator templates, and information objects to the risk statement. You can also now assess the risks that are generated in the Risks tab. You can also view the hierarchy of the risks statement on the risk statement side bar. To view the complete risk profile at a glance, click the **Overview** tab.

**Parent Topic:**[Create a risk framework in the Risk Workspace](create-risk-framework.md)


---
title: Define fields and weights for the risk rule
description: Customize the parameters and weights for the risk rule so that you can generate risk scores that use the test and asset data that are unique to your organization. By selecting the fields that are included in the risk rule, you can define an effective risk scoring framework.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuration Compliance calculators and calculator rules, Create a Configuration Compliance calculator group, Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Define fields and weights for the risk rule

Customize the parameters and weights for the risk rule so that you can generate risk scores that use the test and asset data that are unique to your organization. By selecting the fields that are included in the risk rule, you can define an effective risk scoring framework.

## Before you begin

Role required: sn\_vulc.admin

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Risk Calculators**.

2.  Click **Default Risk Calculator**.

3.  Select the target field as **Risk Score**.

    The **New Risk Rule** button displays on the Calculator Rule table.

4.  Click the **New Risk Rule** button to navigate to the **Configuration Compliance Risk Rule** form.

5.  In the Risk Calculator Criteria section, set the weight for each criterion according to its importance in the overall risk score calculation.

6.  Clear the **Active** check box, to deactivate the rule.

7.  Click **Add Criteria** to add risk rule fields to the Risk Calculator Criteria.

8.  On the form, fill in the fields.

<table id="table_djj_sls_ssb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choose reference table

</td><td>

The table that you use to define the risk score weightage.Select from the following options:

-   Test Result: Add fields that are you can directly dot walk to from the Test Result \(TR\).
-   Test Result - Configuration Item: Add dot walkable fields that are part of the base table extensions, such as the Hardware table.

These fields are not part of the base cmdb\_ci table.

-   Test Result - Test: Add dot-walkable fields that are part of the tables that extend the base table, for example, Third-party Entry. These fields are not part of the Configuration Test base table.
-   Test Result Reference Table: Add fields that are a part of the Related tables \(m2m\) or tables that have a reference to the test result. These fields are not directly dot-walkable from the Test Result.
-   Configuration Item Reference Table: Add fields that are a part of the Related tables \(m2m\) of cmdb\_ci or tables that have a reference to cmdb\_ci. These fields are not directly dot-walkable from the TR.
-   Test Reference Table: Add fields that are a part of the Related tables \(m2m\) of sn\_vulc\_test or tables that have a reference to sn\_vulc\_test. These fields are not directly dot-walkable from the TR.
-   Custom Conditions: Use this option to assign weights to the rule by evaluating the condition. For example, the Internet-facing filter determines if a configuration item \(CI\) is external or internal.


</td></tr><tr><td>

Field

</td><td>

The field used for risk score calculation for this rule.

</td></tr><tr><td>

Weight

</td><td>

Weightage of this field within the risk rule. The value must be an integer from 0 through 100.

</td></tr><tr><td>

Table

</td><td>

-   Test Result &gt; Configuration Item
-   Test Result &gt; Test
-   Test Result Reference Table
-   Configuration Item Reference Table
-   Test Reference Table
 This field appears only when any of the listed options is selected from the Choose reference table field.

</td></tr><tr><td>

Aggregation

</td><td>

Select the minimum or maximum value to be considered for calculations when field is selected from the Related tables \(m2m\).This field appears only when a reference table is selected from the Choose reference table field.

</td></tr><tr><td>

Define value weightage

</td><td>

Component to assign weights to each field value. For numeric fields, define field values as a range \(for example, 1–5\). The value must be an integer between 0–100. This field does not appear if the Custom Conditions option is selected from the Choose reference table field.

</td></tr><tr><td>

Condition table

</td><td>

Select a condition from the list.This field appears only when Custom conditions option is selected from the Choose reference table field.

</td></tr><tr><td>

Field name

</td><td>

Enter a name for the risk criteria.This field appears only when Custom conditions is selected from the Choose reference table field.

</td></tr><tr><td>

Condition

</td><td>

Preview the items in this table that match the defined conditions. This field appears only when Custom conditions is selected from the Choose reference table field.

</td></tr></tbody>
</table>9.  Click **Submit**.


## What to do next

In the Rule page, activate and reapply the rule to reevaluate the risk score on the active test result.


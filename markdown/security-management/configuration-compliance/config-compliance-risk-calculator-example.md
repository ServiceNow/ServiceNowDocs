---
title: Examples for Configuration Compliance risk score calculation
description: Starting with v13.0 of Configuration Compliance, you can customize the criteria for the default risk rule. Use risk scores provided by third-party vendors like Qualys and Tenable for risk score calculations.Use scores based on criticality provided by third-party vendors to compute risk scores.Specify a criticality value to business services and use the business criticality to compute the risk scores.Use custom conditions to the risk rule for risk score calculation.Determine the risk score calculators to generate risk scores that use the test and asset data specific to your organization.The following example demonstrates how scores for risk rollup calculators are determined.The following example demonstrates how scores for risk rollup calculators are determined.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Configuration Compliance calculators and calculator rules, Create a Configuration Compliance calculator group, Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Examples for Configuration Compliance risk score calculation

Starting with v13.0 of Configuration Compliance, you can customize the criteria for the default risk rule. Use risk scores provided by third-party vendors like Qualys and Tenable for risk score calculations.

Third-party vendors, like Qualys and Tenable, provide their own scores. These scores are populated in the Criticality field on the sn\_vulc\_test table. Use this field for risk score calculations. To use this score to compute the risk score, follow the procedure:

## Add source criticality as a criterion for a risk rule

Use scores based on criticality provided by third-party vendors to compute risk scores.

### Before you begin

Role required: sn\_vulc.admin

### About this task

Third-party vendors, like Qualys and Tenable, provide their own risk scores. These scores are populated in the Criticality field on the sn\_vulc\_test table. Use this field for risk score calculations and computing the risk score.

### Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Risk Calculators**.

2.  Navigate to the Risk rule form.

3.  Clear the **Active** check box, to deactivate the rule.

4.  Click **Add Criteria**.

5.  From the **Choose reference table** list, select **Test Result**.

6.  From the **Field** list, select **Test.Criticality**.

7.  In the **Weight** field, specify the relative importance of this field.

    The value must be an integer from 0 through 100.

8.  In the **Define Value Weightages** section, add field values, and assign a weightage percentage to the fields.

    ![Source Criticality for risk calculation](../image/source-criticality-cc-risk-calculator.png)

9.  Click **Submit**.


## Add business criticality as a criterion for a risk rule

Specify a criticality value to business services and use the business criticality to compute the risk scores.

### Before you begin

Role required: sn\_vulc.admin

### About this task

Assuming your organization has many business services and a configuration item \(CI\) is being used by the following services:

<table id="table_rsq_jy4_5sb"><thead><tr><th>

Business Service

</th><th>

Criticality

</th></tr></thead><tbody><tr><td>

Cloud Management

</td><td>

1 - Most critical

</td></tr><tr><td>

E-commerce

</td><td>

2 - Somewhat critical

</td></tr><tr><td>

Client services

</td><td>

3 - Less critical

</td></tr><tr><td>

Travel and Expense

</td><td>

4 - Not critical

</td></tr></tbody>
</table>The mapping between the CI and services is stored in the Services \[cmdb\_ci\_services\] table. When a CI does not pass a Configuration Test, a Test Result \(TR\) is created. You can use the value of the business criticality from the affected services to compute the risk score for this TR. Follow the procedure to use the criticality value of these services to compute the risk score.

### Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Risk Calculators**.

2.  Navigate to the Risk rule form from the **Calculator Rules** section.

3.  Clear the **Active** check box, to deactivate the rule.

4.  Click **Add Criteria**.

5.  From the **Choose reference table** list, select **Configuration Item Reference Table**.

6.  From the **Table** list, select **Service \[cmdb\_ci\_service\]**.

7.  From the **Field** list, select **Business Criticality**.

8.  In the **Aggregation** field, select **Minimum** to retrieve the most critical service for this use case \(1- Most critical value\) or **Maximum** to retrieve the least critical service for this use case \(4 – Not critical value\).

9.  In the **Weight** field, specify the relative importance of this field.

    The value must be an integer from 0 through 100.

10. In the **Define Value Weightages** section, add field values and assign weightages.

    ![Custom business criticality risk rule weightage](../image/custom-business-crit-risk-rule-weight.png "Custom business criticality risk rule weightage")

11. Click **Submit**.


## Add conditional criterion to the risk calculator

Use custom conditions to the risk rule for risk score calculation.

### Before you begin

Role required: sn\_vulc.admin

### About this task

Assuming that your organization has multiple configuration items \(CIs\), of which only a few can be accessed by an external user. Users can add risk score weightages for these outward-facing CIs.

**Note:** You can identify these CIs by their name. The names start with 'external'.

### Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Risk Calculators**.

2.  Navigate to the Risk rule form.

3.  Clear the **Active** check box, to deactivate the rule.

4.  Click **Add Criteria**.

5.  From the **Choose reference table** list, select **Custom Conditions**.

6.  From the **Condition table** list, select **Configuration Item**.

7.  In the **Field Name** field, enter `CI Exposure`.

8.  In the **Weight** field, specify the relative importance of this field.

    The value must be an integer from 0 through 100.

9.  In the **Condition** field, select **Name &gt; starts with**, specify the value as `external`.

    ![Custom conditions for new risk rule](../image/custom-conditions-new-risk-rule.png "Custom conditions for new risk rule")

10. Click **Submit**.


**Related topics**  


[Configuration Compliance calculator groups](../concept/vuln-config-compl-calc-groups.md)

## Risk score calculation example for Configuration Compliance

Determine the risk score calculators to generate risk scores that use the test and asset data specific to your organization.

### Example of determining risk rule calculators scores

The following example demonstrates how scores for risk rule calculators are determined. Assume that a risk rule calculator is configured with the fields in this table.

<table id="table_hhf_cgp_5sb"><thead><tr><th>

Field

</th><th>

Weightage

</th><th>

Weight breakdown

</th></tr></thead><tbody><tr><td>

Control.Criticality

</td><td>

50

</td><td>

Default: 0

 Minor: 20

 Low: 30

 Moderate: 50

 High: 70

 Critical: 100

</td></tr><tr><td>

Business\_Criticality

</td><td>

50

</td><td>

Default: 0

 Minor: 20

 Low: 30

 Moderate: 50

 Hight: 70

 Critical: 100

</td></tr></tbody>
</table>Assume that the Test Results that are shown in this table are present in the system.

|ID|Business Criticality|Control Criticality|
|---|--------------------|-------------------|
|CTR0000001|1 – Most Critical|Minor|
|CTR0000002|1 – Most Critical|Low|
|CTR0000003|2 – Somewhat Critical|Minor|
|CTR0000004|2 – Somewhat Critical|Moderate|
|CTR0000005|3 – Less Critical|Low|

The risk score calculation for the test result is calculated based on the formula:

Risk Score = \(W\(control.criticality\) \* FV \(control.criticality\). + W\(business\_criticality\) \* FV\(business\_criticality\)\) / 100 where W is the weight and FV is the weight percentage of the field value.

The resulting risk score for these test results is as described in this table:

|ID|Business Criticality \(50%\)|Control Criticality \(50%\)|Resultant risk score|
|---|----------------------------|---------------------------|--------------------|
|CTR0000001|1 – Most Critical \(50% x100\)|Minor \(50% x 20\)|60|
|CTR0000002|1 – Most Critical \(50% x 100\)|Low \(50% x 30\)|65|
|CTR0000003|2 – Somewhat Critical \(50% x 70\)|Minor \(50% x 30\)|45|
|CTR0000004|2 – Somewhat Critical \(50% x 70\)|Moderate \(50% x 50\)|60|
|CTR0000005|3 – Less Critical \(50% x 50\)|Low \(50% x 30\)|40|

If the weightage percentage is changed for one of the field values, see this table for the results:

<table id="table_hzt_jhp_5sb"><thead><tr><th>

Field

</th><th>

Weightage

</th><th>

Weight breakdown

</th></tr></thead><tbody><tr><td>

Control.Criticality

</td><td>

50

</td><td>

Default: 0

 Minor: 20

 Low: 30

 Moderate: 60

 Hight: 70

 Critical: 100

</td></tr><tr><td>

Business\_Criticality

</td><td>

50

</td><td>

Default: 50

 1 – Most Critical: 100

 2 – Somewhat Critical: 70

 3 – Less Critical: 20

 4 – Not Critical: 30

</td></tr></tbody>
</table>The risk score for the test results after reapplying the calculator is shown in this table:

<table id="table_h5p_rhp_5sb"><thead><tr><th>

ID

</th><th>

Business Criticality \(50%\)

</th><th>

Control Criticality \(50%\)

</th><th>

Resultant risk score

</th></tr></thead><tbody><tr><td>

CTR0000001

</td><td>

1 – Most Critical \(50% x 100\)

</td><td>

Minor \(50% x 20\)

</td><td>

60

</td></tr><tr><td>

CTR0000002

</td><td>

1 – Most Critical \(50% x 100\)

</td><td>

Low \(50% x 30\)

</td><td>

65

</td></tr><tr><td>

CTR0000003

</td><td>

2 – Somewhat Critical \(50% x 70\)

</td><td>

Minor \(50% x 30\)

</td><td>

45

</td></tr><tr><td>

CTR0000004

</td><td>

2 – Somewhat Critical \(50% x 70\)

</td><td>

Moderate \(50% x 60\) \*Revised value

</td><td>

65 \*Revised value

</td></tr><tr><td>

CTR0000005

</td><td>

3 – Less Critical \(50% x 20\)

 \*Revised value

</td><td>

Low \(50% x 30\)

</td><td>

25 \*Revised value

</td></tr></tbody>
</table>## Risk rollup calculation example for Configuration Compliance \(prior to v15.0\)

The following example demonstrates how scores for risk rollup calculators are determined.

For the following remediation task rollup calculator, the formula for calculating the Remediation Task Risk Score is:

\(Maximum risk score/100\) \* 85 + \(factor \* 15\).

The factor in the previous equation is determined by the number of test results as shown in the following table.

|Test result count|Factor|
|-----------------|------|
|&lt;10|0.2|
|10-99|0.4|
|100-1000|0.6|
|1001-9999|0.8|
|&gt;10000|1|

For the following Remediation Task, TRG0003066, with three test results Risk scores, the maximum score is 90.

|Number|Risk score|Remediation task|Result|Status|
|------|----------|----------------|------|------|
|CTR000123|90|TRG0003066|Failed|Open|
|CTR000124|70|TRG0003066|Failed|Open|
|CTR000125|40|TRG0003066|Failed|Open|

For the Remediation Task, TRG0003066:

The Risk Score is 79, \(90/100\) \* 85 + 0.2 \* 15 = Math.floor \(76.5 +3\) =79.

The historical risk score is null, because the Remediation Task is still 'Open'.

After the data ingestion, the test results are 'Passed', and the Remediation Task transitions to 'Closed' as shown in the following table.

|Number|Risk score\(Prior to v15.0\)|Remediation task|Result|Status|
|------|----------------------------|----------------|------|------|
|CTR000123|0|TRG0003066|Passed|Closed|
|CTR000124|0|TRG0003066|Passed|Closed|
|CTR000125|0|TRG0003066|Passed|Closed|

Test results History is displayed in the following table.

|Number|Risk score|Latest result|Result|
|------|----------|-------------|------|
|CTRH000111|90|CTR000123|Failed|
|CTRH000112|70|CTR000124|Failed|
|CTRH000113|40|CTR000125|Failed|

The Risk Score is zero, because there are no active test results in the Remediation Task.

For the Remediation Task, TRG0003066:

The Historical Risk Score is 79: \(90/100\) \* 85 + 0.2 \* 15 = Math.floor \(76.5 +3\) =79.

## Risk rollup calculation example for Configuration Compliance \(v15.0 and later\)

The following example demonstrates how scores for risk rollup calculators are determined.

For the following remediation task rollup calculator, the formula for calculating the Remediation Task Risk Score is:

\(Maximum risk score\* 80/100\) + \(Average risk score\* 5/100\) + \(Factor \* 15\)

Where, the weights are as follows:

-   Maximum risk score: 80
-   Average risk score: 5
-   Factor: 15

The default weight of the Average risk score is 0. For more information on how to set the weights, see [Edit risk rollup calculators for Configuration Compliance](../task/v11create-rollup-calc.md).

The factor in the previous equation is determined by the number of test results as shown in the following table.

|Test result count|Factor|
|-----------------|------|
|&lt;10|0.2|
|10-99|0.4|
|100-1000|0.6|
|1001-9999|0.8|
|&gt;10000|1|

For the following Remediation Task, TRG0003066, with three test results Risk scores, the maximum risk score is 90 and the average risk score is 66.67.

|Number|Risk score|Remediation task|Result|Status|
|------|----------|----------------|------|------|
|CTR000123|90|TRG0003066|Failed|Open|
|CTR000124|70|TRG0003066|Failed|Open|
|CTR000125|40|TRG0003066|Failed|Open|

For the Remediation Task, TRG0003066:

The Risk Score is 81, \(90\* 80/100\) + \(66.67\* 5/100\) + \(0.2 \* 15\) = Math.floor \(78.3 +3\) = 81.

The historical risk score is null, because the remediation task is still 'Open'.

After the data ingestion, the test results are 'Passed', and the Remediation Task transitions to 'Closed' as shown in the following table. Starting with v15.0 of Configuration Compliance, the Risk Score of a passed test result is populated to determine the risk mitigated.

|Number|Risk score|Remediation task|Result|Status|
|------|----------|----------------|------|------|
|CTR000123|90|TRG0003066|Passed|Closed|
|CTR000124|70|TRG0003066|Passed|Closed|
|CTR000125|40|TRG0003066|Passed|Closed|

Test results History is displayed in the following table.

|Number|Risk score|Latest result|Result|
|------|----------|-------------|------|
|CTRH000111|90|CTR000123|Failed|
|CTRH000112|70|CTR000124|Failed|
|CTRH000113|40|CTR000125|Failed|

The Risk Score of the Remediation Task is zero, because there are no active test results in the Remediation Task.

For the Remediation Task, TRG0003066:

The Historical Risk Score is 81: \(90\* 80/100\) + \(66.67\* 5/100\) + \(0.2 \* 15\) = Math.floor \(78.3 +3\) = 81.


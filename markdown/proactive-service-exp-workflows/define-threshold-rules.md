---
title: Define threshold rules for a test measure definition
description: Set rules or criteria to evaluate the results of test measures. These rules establish thresholds that determine the acceptable performance and quality metrics for a service under evaluation. If test measure results exceed or fall below these thresholds, it indicates a deviation from expected performance levels.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up test definitions, Configure, Customer Service Problem Management]
---

# Define threshold rules for a test measure definition

Set rules or criteria to evaluate the results of test measures. These rules establish thresholds that determine the acceptable performance and quality metrics for a service under evaluation. If test measure results exceed or fall below these thresholds, it indicates a deviation from expected performance levels.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the test definition that you want to open.

3.  In the Threshold Rules related list, define a threshold rule for a test measure by selecting **New**.

4.  On the form, fill in the fields.

5.  <table id="table_ajh_hqy_jbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated ID for the test measure definition.

</td></tr><tr><td>

Name

</td><td>

Name of the threshold rule.

</td></tr><tr><td>

Test measure definition

</td><td>

Name of the test measure definition for which you’re defining threshold rules.

</td></tr><tr><td>

Conformance comparator exact

</td><td>

Option to determine if the service under testing meets the defined criteria.

</td></tr><tr><td>

Conformance target exact

</td><td>

Option to determine if the service or system behaves as expected under specified conditions.This field appears only if the **Conformance comparator exact** option is selected.

</td></tr><tr><td>

Conformance comparator lower

</td><td>

Lower range of the threshold for comparing the test measure results.

</td></tr><tr><td>

Conformance comparator upper

</td><td>

Upper range of the threshold for comparing the test measure results.

</td></tr><tr><td>

Severity

</td><td>

Severity of this rule.

</td></tr><tr><td>

Tolerance period

</td><td>

Specified time interval during which crossing occurrences are enabled without triggering any immediate consequences or actions.

</td></tr><tr><td>

Number of allowed crossing

</td><td>

Number of occurrences of a threshold crossing that are allowed within a certain time frame before any consequences are triggered.

</td></tr><tr><td>

Conformance target lower

</td><td>

Lower boundary that determines if a specific limit is crossed or no longer crossed.**Note:** This value must be greater than the upper limit defined in the **Conformance target upper**.

</td></tr><tr><td>

Conformance target upper

</td><td>

Upper limit that determines if the threshold is crossed or no longer crossed.**Note:** This value must be less than the lower limit defined in the Conformance target lower.

</td></tr><tr><td>

Description

</td><td>

Description of the threshold rule.

</td></tr></tbody>
</table>6.  Select **Submit**.



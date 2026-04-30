---
title: Test Results fields
description: Test results are automatically created during third-part vulnerability integration imports.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuration Compliance reference information, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Test Results fields

Test results are automatically created during third-part vulnerability integration imports.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

Configuration Compliance does not create or update the test results, but imports them as part of a third-party integration. Once they are viewable in Configuration Compliance, they are remediated using **Test Result Groups**.

## Test results fields

<table id="table_t4d_4bd_5x"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number assigned to the test result during the import process.

</td></tr><tr><td>

Source

</td><td>

System name of the third-party integration application, or the name entered in the application for the API that is used to communicate with Configuration Compliance.

</td></tr><tr><td>

Source ID

</td><td>

Identifier assigned to the test result by the third-party integration.

</td></tr><tr><td>

Risk Score

</td><td>

Score based on the **Criticality** value of the test. If you do not have installed and configured, a middle value of 50 is used.

</td></tr><tr><td>

Resolution

</td><td>

Resolution of the test result, calculated from associated groups.

</td></tr><tr><td>

Result

</td><td>

Status of the scan. Pass or Fail. If this test belongs to multiple remediation tasks, then its state is determined following an [order of precedence](../concept/vuln-config-compl-correlation.md#TRGOrderPrecedence).

</td></tr><tr><td>

State

</td><td>

State of the test result, calculated from associated groups.

</td></tr><tr><td>

Assignment group

</td><td>

Group selected to work on this test result.

</td></tr><tr><td>

Assigned to

</td><td>

Individual from the selected assignment group to work on this test result.

</td></tr><tr><td>

Assignment type

</td><td>

Type of assignment. Choices are:-   Rule
-   Manual
-   None

</td></tr><tr><td>

Assignment rule

</td><td>

Which assignment rule was used with this test result, when applicable.

</td></tr><tr><td>

First seen

</td><td>

Time and date the test result was first seen.

</td></tr><tr><td>

Last seen

</td><td>

Time and date the test result was last seen.

</td></tr><tr><td>

Test

</td><td>

The control that this result belongs to.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item associated with this test result.

</td></tr><tr><td>

Technology

</td><td>

Technology associated with this test result.

</td></tr><tr><td colspan="2">

**Description**

</td></tr><tr><td>

Description

</td><td>

Detailed description of the test result as defined in the third-party scanner application.

</td></tr><tr><td colspan="2">

**Expected Values**

</td></tr><tr><td>

Expected values

</td><td>

Description and expected values as defined in the third-party scanner application.

</td></tr><tr><td colspan="2">

**Actual Values**

</td></tr><tr><td>

Actual values

</td><td>

Description and actual values as defined in the third-party scanner application.

</td></tr><tr><td colspan="2">

**Remediation**

</td></tr><tr><td>

Remediation

</td><td>

Remediation action as defined in the third-party scanner application.

</td></tr></tbody>
</table>The following are the vulnerable items related lists.

|Related List|Description|
|------------|-----------|
|Remediation Tasks|Remediation tasks associated with this test result.|
|Test Result History|List of past records containing different results.|

**Parent Topic:**[Configuration Compliance reference information](cc-reference-info.md)


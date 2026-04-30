---
title: View Configuration Compliance tests
description: Use this module to research detailed information about these tests. Included are the expert source citations that were used when creating them, the third-party configuration policies in which they are used, and the results obtained from the scan.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuration Compliance reference information, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# View Configuration Compliance tests

Use this module to research detailed information about these tests. Included are the expert source citations that were used when creating them, the third-party configuration policies in which they are used, and the results obtained from the scan.

## Before you begin

Role required:

-   sn\_vulc.admin to update
-   sn\_vulc.remediation\_owner to view

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Controls**.

2.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Tests**

3.  From the list, open the control \(compliance test\) you want to view.

    Starting with version 12.0, to update these values on-demand, below the Remediation status tab, click the **Update Status** Related link. A message is displayed that indicates the data is being refreshed. Click the **View status** link to view progress on the update. After a few moments, any data that has changed or been updated since the last scheduled job are refreshed on the record. Field values such as the**Risk Score**, **Risk Rating**, **Remediation target date**, **State**, and the fields on the **Remediation Status** tab are refreshed.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number assigned to the control during the import process.

</td></tr><tr><td>

Result

</td><td>

Status of the scan. Pass or Fail. If this test belongs to multiple remediation tasks, then its state is determined following an [order of precedence](../concept/vuln-config-compl-correlation.md#TRGOrderPrecedence).

</td></tr><tr><td>

Source

</td><td>

System name of the third-party integration application, or the name entered in the plugin for the API that is used to communicate with Configuration Compliance.

</td></tr><tr><td>

Criticality

</td><td>

Severity of the configuration issue or issues associated with the control as defined in the third-party integration. The level of criticality is adjusted to match the granularity of similar vulnerability indicators available in Vulnerability Response. The possible levels are: -   **Critical**

The configuration issue associated with the control is causing a disruption to one or more business-critical CIs.

-   **High**

The configuration issue associated with the control is a threat, but is not causing a shutdown of critical network resources.

-   **Moderate**

The configuration issue associated with the control is a risk, but is not an immediate threat.

-   **Low**

The configuration issue associated with the control is a low-level threat and can be ignored in favor of CIs that are at greater risk.

-   **Minor**

The configuration issue associated with the control is a minor risk and can be ignored if necessary.

</td></tr><tr><td>

Source ID

</td><td>

Identifier assigned to the control by the third-party integration.

</td></tr><tr><td>

Category

</td><td>

Major classification category given to this type of control by the third-party vendor.

</td></tr><tr><td>

Risk score

</td><td>

This is a rollup risk score. This risk score is weighted, with 85% of the score from the max risk score across all Test Results not 'Closed' \(Open, Under Investigation, Awaiting Implementation, Deferred, Resolved\), and 15% of the score from the number of test results that are not 'Closed'.Value calculated by risk score calculators that is based on the business criticality and test criticality values of test results.

</td></tr><tr><td>

Sub-category

</td><td>

Sub-category assigned to this class of test by the third-party vendor.

</td></tr><tr><td>

Risk rating

</td><td>

Based on a range of risk scores on a 1-5 numeric scale that rates overall risk based on a range of risk scores as 1 - Critical to 5 - None. This field replaces the Priority field in previous versions.

</td></tr><tr><td>

Technologies

</td><td>

List of technologies covered by this test.

</td></tr><tr><td>

Source created

</td><td>

Date the test was first defined in the third-party integration.

</td></tr><tr><td>

Source updated

</td><td>

Date the test was last updated in the third-party integration.

</td></tr><tr><td>

Short description

</td><td>

Summary description or title entered or assigned to the test in the third-party integration.

</td></tr><tr><td colspan="2">

**Remediation Status \(v 12.0\)**

</td></tr><tr><td>

Excludes Deferred

</td><td>

These values do not include deferred test results.

 -   **Open test results**: The number \(count\) of active \(any state other than **Closed**\) test results for this configuration test.
-   **% Test results remediated**: The percent of remediated test results for this remediation task.
-   **Total test results**: The total number of test results for this remediation task.


</td></tr><tr><td>

Includes Deferred

</td><td>

These values include deferred test results.

 -   **Open test results**: The number \(count\) of all active \(any state other than **Closed**\) test results for this remediation task.
-   **% Test results remediated**: The percent of remediated test results for this remediation task.
-   **Total test results**: The total number of test results for this remediation task.


</td></tr><tr><td>

Description

</td><td>

Long description of the test. For the Qualys Vulnerability Integration, this field defaults to the contents of the Qualys Cloud Platform cover page.

</td></tr><tr><td>

Remediation

</td><td>

Steps instructions describing how to remediate the non-compliance.

</td></tr><tr><td class="sub-head" colspan="2">

**Related Tabs**

</td></tr><tr><td>

Citations

</td><td>

List of citations entered for each authoritative source associated with the test.

</td></tr><tr><td>

Test Groups

</td><td>

List of Configuration Compliance test groups that use this test.

</td></tr><tr><td>

Test Results

</td><td>

List of CIs affected by the configuration issue or issues associated with this test. You can access individual tests, ServiceNow configuration items, or the list of affected technologies, if necessary.

</td></tr><tr><td>

GRC Policy Statements

</td><td>

If the GRC Policy and Compliance Management plugin is installed, this tab contains the related GRC policy. You can edit this list to add or remove policy statements.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuration Compliance reference information](../reference/cc-reference-info.md)


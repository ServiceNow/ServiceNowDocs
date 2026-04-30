---
title: View Configuration Compliance test groups
description: Once you have imported the results of a third-party scan into your instance, you can see your test compliance at the test group level. Use this view before an audit of that test group and any associated test records.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-08-05"
reading_time_minutes: 3
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# View Configuration Compliance test groups

Once you have imported the results of a third-party scan into your instance, you can see your test compliance at the test group level. Use this view before an audit of that test group and any associated test records.

## Before you begin

Role required: sn\_vulc.read and sn\_vulc.remediation\_owner to view

## About this task

Test groups are imported records and uneditable inside Configuration Compliance.

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Test Groups**.

    The list of Test results display. Starting with v15.0 of Configuration Compliance, the **% Test Result Compliance** column displays the percentage of test results that are compliant with the tests in a test group.

    % Test Result Compliance = \(No. of Test results closed in a test group/Total no. of test results associated with a test group\) \* 100

2.  Click the **Short description** of the Test Group you want to view.

<table id="table_j1g_qpc_m1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

System name of the third-party scanner, or the name entered in the ServiceNow plugin for the API that is used to communicate with Configuration Compliance.

</td></tr><tr><td>

Technologies

</td><td>

List of technologies associated with the test group in the third-party scanner application.

</td></tr><tr><td>

Source ID

</td><td>

Identifier assigned to this test group by the third-party scanner.

</td></tr><tr><td>

Source created

</td><td>

Date and time the test group was defined in the third-party scanner application.

</td></tr><tr><td>

Source updated

</td><td>

Date and time the test group was last modified in the third-policy scanner application.

</td></tr><tr><td>

Short description

</td><td>

Summary description or title assigned to the test group in the third-party scanner application.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the test group as defined in the third-party scanner application.

</td></tr><tr><td>

Tests

</td><td>

List of tests that reference this test group. Imported from the third-party scanner. You can navigate the list to detailed information about a specific test, if necessary.

</td></tr><tr><td colspan="2">

**Remediation Status \(Version 12.0\)**

</td></tr><tr><td>

Excludes Deferred

</td><td>

These values do not include CIs from deferred test results.

 -   **Remaining CIs**: The number \(count\) of configuration items \(CIs\) with active test results \(any state other than **Closed**\) for this policy.
-   **% CIs remediated**: Percent of compliant CIs for this test group. This number excludes CIs with deferred test results.
-   **Total CIs**: The total number of CIs impacted by this test group. This count excludes deferred test results.


</td></tr><tr><td>

Includes Deferred

</td><td>

The values represent CIs from all active test results \(any state other than **Closed**\).

-   **Remaining CIs**: The number of unique CIs associated with one or more test results not closed to which this test group has been applied.
-   **% CIs remediated**: The percent of compliant CIs for this test group.
-   **Total CIs**: Total number of CIs impacted by this test group.


</td></tr></tbody>
</table>    Starting with version 12.0, to update these values on-demand, below the Remediation status tab, click the **Update Status** related link. A message is displayed that indicates the data is being refreshed. Click the **View status** link to view progress on the update. After a few moments, any data that has changed or been updated since the last scheduled job are refreshed on the record. Updated field values are refreshed.

3.  Disable the import of test results for a test group by selecting the **Disable import** button.

    The value in the **Is import disabled** column changes to true. The test results for the test group are not imported from the upcoming ingestion.

    **Note:** The **Disable import** button is available for the test results obtained from the Qualys scanner only.

    Starting with v23.0 of Vulnerability Response:

    -   You can enable or disable the import of test results for a Qualys test group in the Vulnerability Manager Workspace. For more information, see [Enable or disable the import of test results for a Qualys test group](enable-disable-imports-qualys.md).
    -   The **Mark deprecated** button is renamed to **Disable import**.
    -   The **Is deprecated** column is renamed to **Is import disabled**.


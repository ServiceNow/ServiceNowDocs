---
title: View Configuration Compliance test results
description: View Configuration Compliance test results for auditing and remediation. The test results are automatically created during third-party vulnerability integration imports.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# View Configuration Compliance test results

View Configuration Compliance test results for auditing and remediation. The test results are automatically created during third-party vulnerability integration imports.

**Important:** You can view the test results created during the third-party vulnerability integration imports in the Vulnerability Manager Workspace. For more information, see [List page in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/concept/vmws-list-page.md).

## Before you begin

Role required:

-   sn\_vulc.read to view
-   sn\_vulc.remediation\_owner to view and update
-   sn\_vulc.delete to delete

## About this task

Configuration Compliance does not create or update the test results, but imports them as part of a third-party integration. Once they are viewable in Configuration Compliance, they are remediated using **Test Result Groups**.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Test Results**.

    Starting with v15.0 of Configuration Compliance, the following columns appear in the Test Results list.

<table id="table_agk_gpj_bcc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Indicates if a test result is active. A test result is marked:-   True: If the State isn’t Closed.
-   False: If the State is Closed.


</td></tr><tr><td>

Age

</td><td>

Time period for which a test result is active since it was last open.This field is empty for a closed test result.

Format: Days HH:MM: SS

For more information on how to customize the Age calculation, see the [KB1703270](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1703270) article.

</td></tr><tr><td>

Age closed

</td><td>

Time period for which a test result was active before it transitioned to ‘Closed'. When the test result transitions to ‘Closed', the value from the Age column is displayed in the Aged closed field. This field is empty for an active test result.

Format: Days HH:MM: SS

For more information on how to customize the Age closed calculation, see the [KB1703270](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1703270) article.

</td></tr><tr><td>

Closed

</td><td>

Timestamp at which a test result is closed.Format: YYYY-MM-DD HH:MM: SS

</td></tr><tr><td>

Last opened

</td><td>

Timestamp at which a test result is opened, that is, when the **Active** field value changes to true.

</td></tr></tbody>
</table>2.  Open the control that you want to view.

<table id="table_vs3_mgq_jbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The number assigned to the test during the import process.

</td></tr><tr><td>

Source

</td><td>

The system name of the third-party SCA application, or the name entered in the application plugin for the API that is used to communicate with Configuration Compliance.

</td></tr><tr><td>

Source ID

</td><td>

The identifier assigned to the control by the SCA application.

</td></tr><tr><td>

Result

</td><td>

Passed, Failed, Error, or Unknown. Imported from Qualys.

</td></tr><tr><td>

Risk score

</td><td>

Calculator result for this test.Prior to v15.0 of Configuration Compliance, the risk score of a passed test result is set to '0'. Starting with v15.0 of Configuration Compliance, the risk score of the passed test result isn’t changed to '0' so that you can estimate the risk mitigated. The risk score of the passed test result isn’t included in calculating the risk score of a remediation task.

</td></tr><tr><td>

Risk rating

</td><td>

Based on a range of risk scores on a 1-5 numeric scale that rates overall risk based on a range of risk scores as 1 - Critical to 5 - None. This field replaces the Priority field in previous versions.

</td></tr><tr><td>

State

</td><td>

Calculated from the remediation tasks that the test result belongs to. If the test result belongs to multiple groups, an [order of precedence](../concept/vuln-config-compl-correlation.md#TRGOrderPrecedence) is applied to determine state.

</td></tr><tr><td>

Resolution

</td><td>

Calculated from the remediation tasks that the test result belongs to. If the test result belongs to multiple groups, an [order of precedence](../concept/vuln-config-compl-correlation.md#TRGOrderPrecedence) is applied to determine resolution.

</td></tr><tr><td>

First seen

</td><td>

Date first imported into Configuration Compliance.Starting with v13.1.1, the **First seen** field displays the date provided by the scanner. Otherwise, it displays the date first imported into Configuration Compliance.

</td></tr><tr><td>

Last seen

</td><td>

Date last imported into Configuration Compliance.Starting with v13.1.1, the **Last seen** field displays the date provided by the scanner. Otherwise, it displays the date last imported into Configuration Compliance.

</td></tr><tr><td>

Last pass

</td><td>

Latest date on which the test result is passed.

</td></tr><tr><td>

Test

</td><td>

Name of the test.

</td></tr><tr><td>

Configuration item

</td><td>

Name of the CI attached to the test.

</td></tr><tr><td>

Technology

</td><td>

Software version running on the CI.

</td></tr><tr><td>

Description

</td><td>

Description of the test

</td></tr><tr><td>

Expected Values

</td><td>

Expected values configured in Qualys and imported by Configuration Compliance. This value is a Boolean expression that when evaluated to true makes the test result **Passed**. The expression can be a combination of logical, set, or regular expression operators.

</td></tr><tr><td>

Actual Values

</td><td>

Values returned by the test. These values are plugged into the expected values Boolean expression to determine if the result should pass or fail. They’re imported from Qualys.Starting with version 14.9 of Configuration Compliance, the Extended Evidence and Cause of Failure values are added in the Actual Values column.

</td></tr><tr><td>

Remediation

</td><td>

Remediation instructions.

</td></tr><tr><td class="sub-head" colspan="2">

**Related Tabs**

</td></tr><tr><td>

Remediation Tasks

</td><td>

Remediation tasks associated with this test result.

</td></tr><tr><td>

Test Result History

</td><td>

Related list of test results that show the history of pass/fail results for the same CI/technology/test.

</td></tr></tbody>
</table>

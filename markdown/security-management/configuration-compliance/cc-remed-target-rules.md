---
title: Configuration Compliance remediation target rules
description: With remediation target rules, you can set the expected time frames for remediating test results. You can send notifications to users and groups when target dates are approaching and when they are past due.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance remediation target rules

With remediation target rules, you can set the expected time frames for remediating test results. You can send notifications to users and groups when target dates are approaching and when they are past due.

**Important:** As an Configuration Compliance admin or analyst, you can obtain the latest remediation target date for a specific set of test results in the Vulnerability Manager Workspace. This method is more efficient than running the Remediation Target Rules for all test results in the classic UI, which is a time-consuming process. For more information, see [Re-evaluate the remediation properties of the records in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/task/vmws-reevaluate-remediation-parameters.md).

Roles required: Configuration Compliance administrator \(sn\_vulc\_admin\), or a manager with the sn\_vulc.manage\_remediation\_target\_rules role.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Remediation target rules

A scheduled job, **Evaluate and notify remediation targets**, runs daily and uses active remediation target rules to evaluate active test result records. Whenever test result records associated with remediation tasks are updated or changed, the modified values are evaluated by the target rules, and changes are rolled up and displayed on associated remediation tasks.

You can edit, disable, or delete existing remediation target rules and create new ones. When you change, disable, or create a new rule, you have the option to click **Apply Changes** from the Remediation Target Rules list view and manually apply the changes you introduced before the next scheduled job. With this option, you can reevaluate your test result records without having to wait. If you do not choose to apply your changes manually, the next daily scheduled job picks up your changes and applies them.

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Remediation Target Rules** to view remediation target rules.

    ![Remediation Target Rules view: Apply changes form button.](../image/cc-target-rules-list-view.png "Apply Changes on Remediation Target Rules list view")

2.  Click a rule in the Name column to open its record.
3.  Select the **Active** check box on the Remediation Target Rule record to enable \(`true`\) any disabled rules \(`false`\).

Whenever you change or add a target rule, regardless of whether you choose to apply the changes manually or wait for the next scheduled job, your changes are used to evaluate all active test results along with any other target rules that are affected by your changes. When you choose to manually apply the changes, this evaluation may take some time if you have a large volume of active test results, because all the rules impacted by your changes are used for an evaluation.

For example, the default value for targeted remediation days is 30. If you create a new rule that also has 30 for Targeted remediation days, this rule, and any target rules with 30 days or greater as target dates are each applied to your test results.

## Deactivated and deleted target rules

When a rule is active, `true` is displayed in the Active column on the Remediation Target rules list view. After a rule is deactivated \(`false`\), it is no longer applied to new test results. However, the scheduled job continues tracking any existing test results the rule was applied to. If the deactivated rule or rules are subsequently reactivated, any test result with an empty **Remediation Target Date** field is evaluated against the reactivated rules. This includes test results created while the rules were deactivated.

When rules are deleted, the **Remediation Target Date** and related fields on closed test results are preserved. The **Remediation Target Date** and related fields on non-closed test results are cleared, and any dependent rules are reapplied.

To deactivate a rule, from the remediation target rule record, disable the active check box and click **Update**. `False` is displayed in the Active column on the Remediation Target Rules list view.

To delete a rule, click **Delete** on the form, or, alternatively, from the list view, select the rule or rules, and click **Delete** from the **Actions on rows** list. The rule is no longer displayed on the list and the next rule in the order of operation replaces the deleted rule.

If you deactivate or delete a rule and choose to apply your changes prior to the next scheduled job, the rule reference is cleared from the field, but the remediation date and status data are preserved. If you do not apply your changes manually, the rule reference is cleared from the field with the next scheduled job.

## About Target rules and the Evaluate and notify remediation targets scheduled job

The **Evaluate and notify remediation targets** scheduled job runs once at 4:30:00 daily. It picks up any active remediation target rules and evaluates all active test results starting with the test results with the earliest remediation target date. It evaluates all test results that meet the following criteria:

-   Are not in a **Closed** state.
-   Have no remediation target date.
-   Have remediation target dates that are later than the dates in the remediation target rules.
-   Are created after a scanner import is completed. The scheduled job picks up and evaluates any new test results that are created as a result of an import.

After a target rule is defined, remediation target dates are calculated by the **Evaluate and notify remediation targets** scheduled job. The scheduled job adds a remediation target date, if one does not exist, or, if this rule contains an earlier date than the one in the record, it updates the existing target date.

Any expired records and reminder dates that match the target rules are picked up by the job and notifications are sent. For disabled rules, the job clears the remediation fields on test result records and stops sending notifications.

The sn\_sec\_cmn.evaluate\_targetmissed\_records property, when enabled, prevents the **Evaluate and notify remediation targets** scheduled job from evaluating Target missed Test Results. This property is enabled by default.

## Viewing target dates and status on the list and form views

Configuration Compliance managers can see the remediation target date from both the test result form and list views. Remediation target rules are also run after a scanner import and rerun if a test result is reopened.

The scheduled job updates the **Remediation target** and **Remediation status** in the test result list view, and the **Remediation target rule**, **Remediation target**, and **Remediation status** fields on test result form.

**Note:** By default, the **Remediation target** and **Remediation status** columns are not displayed on the Test Results list view. To display these columns, you also must add them to the list view. Similarly, add the **Remediation target rule**, **Remediation target**, and **Remediation status** fields to the test result form.

Use the slushbuckets in the Settings and Additional action menus, respectively, as shown in the following images to display these columns and fields. For the Additional action menu on the test result record, click the menu icon, followed by **Configure** and **Form layout** to view the slushbucket and move the fields from **Available** to **Selected**.

The Remediation target date is coded on the Test Results list view as colored dots:

-   Test results that have not reached their notification date are shown in green.
-   Test results approaching the remediation target date are shown in orange.
-   Test results past the remediation target date are shown in red.

![Remediation target and Remediation status columns](../image/cc-target-rule-columns-listview.png "Remediation target and status columns on the Test Results list view")

-   `Target Missed`: the target date is past due
-   `In-flight`: the test result is in progress

![Fields on Test Result form](../image/cc-target-rule-ctr-fields.png "Target rule, target, and status fields on the test result record")

Test result records are also displayed visually on the Configuration Compliance Dashboard. Navigate to **All** &gt; **Configuration Compliance** &gt; **Overview** and check the dashboard for status. The Overview includes existing widgets and remediation status. The colors of the graphs match the colors displayed in the Test Results list view and Test Result record.

## Remediation target rule scenario

When multiple remediation target rules are applied to the same test result, the most restrictive rule is applied.

For example, if a test result first identified on 03/01/2018 meets the conditions for two remediation target rules:

-   Remediation target rule 1: Defined on 03/07/2018; remediation target is 15 days since first seen; calculated remediation target date is 03/16/2018 10:00:00.
-   Remediation target rule 2: Defined on 03/10/2018; remediation target is 10 days since first seen; calculated remediation target date is 03/11/2018 10:00:00.

**Note:**

Remediation targets are calculated from the **Last seen** date plus the number of days \(measured as 24-hour increments\).

Starting from V14.5, remediation targets are calculated from the **Target from \(date\)**. The default value remains **Last Seen**. Starting from v14.12, the default value is **Last pass**.

In this scenario, Remediation target rule 2 applies to the test result, because it has the more restrictive date: 10 days since the test result was first identified versus 15 days.

## Create or modify target rules and reapply changes

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Remediation Target Rules** to view, edit, and create new remediation target rules.
2.  In the Name column, click a rule to open a target rule and edit the record, or, alternatively, click **New** to create a new target rule.
3.  Fill out the form to define the expected remediation time frame, specify which test results this rule to applies to with conditions, and determine when to send reminders to users or groups, or both.

<table id="simpletable_olj_yzr_cnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your rule.

</td></tr><tr><td>

Active

</td><td>

Enable or disable the rule. The rule is automatically enabled \(true\) by default and will be applied to your test results if you choose to apply changes manually or after the next scheduled job.

</td></tr><tr><td>

Target \(days\)

</td><td>

Set the targeted deadline date for remediation in number of days. The default value for targeted remediation days is 30. For example, if you create a new rule that also has 30 for a Target value, your new rule and any other existing rules that also have 30 days or greater as target dates will be applied to your test results.

</td></tr><tr><td>

Target from \(date\)

</td><td>

Date from when the target dates are computed. You can specify only the date or the date and time type fields. Starting from v14.12, the default value is Last pass. Select one of the following:-   Last seen
-   First seen
-   Created
-   Last pass

If the last pass is empty, the Created date is considered for the calculation of remediation target.

-   Last Opened
To customize the values for this field, see [KB1642413](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642413).

</td></tr><tr><td>

Notify \(days before due\)

</td><td>

Set a number of days before the deadline date to remind users and groups.

</td></tr><tr><td>

Description

</td><td>

Short description of the rule.

</td></tr><tr><td>

Condition

</td><td>

Use the condition builder to specify the test results this rule applies to. For example, set a remediation target date of 30 days for all test results with risk scores greater than 70. Send reminders to users or groups, or both, seven days prior to the remediation date.Case sensitivity for the search text you enter in the condition builder is not supported on this record or form. Prior to v 12.0, case sensitivity is supported for the search text you enter in the condition builder.

</td></tr><tr><td>

User and user groups or both

</td><td>

Select users or groups, or both to send notifications about the approaching and past due target dates you have set.

</td></tr></tbody>
</table>4.  Click **Submit**. Alternatively, to save edited rules, click **Update**.

    The list view is displayed with your updated or new rule. Rules in the list are ordered and run starting with the rule with the lowest remediation target date. If you disable or delete a rule, the next rule in the order sequence replaces the inactive or deleted rule.

5.  To apply your new changes now, click **Apply Changes**.


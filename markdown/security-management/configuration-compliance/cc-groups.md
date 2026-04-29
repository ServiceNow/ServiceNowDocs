---
title: Configuration Compliance remediation tasks and remediation task rules overview
description: Automatically create remediation tasks \(RTs\) to analyze results in bulk using remediation task rules. The criteria by which tasks are formed is configured so that you do not have to manually assign test results into remediation tasks.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance remediation tasks and remediation task rules overview

Automatically create remediation tasks \(RTs\) to analyze results in bulk using remediation task rules. The criteria by which tasks are formed is configured so that you do not have to manually assign test results into remediation tasks.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Understanding remediation tasks

Remediation tasks represent a set of test results to remediate. Grouping test results has many advantages. You can move test results through the remediation states, mark them under investigation, defer them, mark them resolved in bulk by using groups. You can create conditions to automatically group all results with specified results, technologies, risk scores, and any other data related to the test results. Test results can belong to more than one remediation task giving you the flexibility to actively work with one remediation task and monitor another. It all depends on your organizational needs. For example, you could group by assignment, and also create a group containing technologies.

Remediation tasks are created as follows.

-   Manually, using one of two options, to add test results to the group.

    -   **Manual**: creates a remediation task with no entries. Test results must be added manually.
    -   **Filter**: creates a remediation task and uses conditions to automatically add test results to that remediation task.
    **Note:** Manually added test results are not automatically removed from remediation tasks by remediation task rules or remediation task conditions.

-   Automatically, using remediation task rules. This option is the easiest option, once configured, remediation task rules create all desired remediation tasks.

From a remediation task, the group of test results may be assigned to a user, deferred until later, used to create a **Change Request**, and so on.

**Note:**

With the sn\_vulc.remediation\_owner role, you can view and update test results and remediation tasks that are assigned to you or to your assignment groups. To view the modules, navigate to **All** &gt; **Configuration Compliance** &gt; **Test Results** &gt; **My Open Test Results**, or **Configuration Compliance** &gt; **Remediation Tasks** &gt; **My Open Tasks**.

When it is determined that a new test result can be added to a remediation task, the test result is included in the **Test Results** related list of the remediation task.

When updating the state of a remediation task, associated test results can have their state updated to match this remediation task. For more information on state changes, see [Configuration Compliance states](vuln-config-compl-states.md).

## Understanding remediation task rules

Remediation task rules allow you to define how test results are automatically grouped and assigned. A default rule, **Assignment group, Test**, is included in the base system grouping test results based on a test result **Assignment group** and the **Test** field. This rule is disabled, by default. You can group by any other set of values in columns accessible from the test result. You can use up to six keys and any number of conditions. For more information, see [Create or edit Configuration Compliance remediation task rules](../task/create-cc-group-rules.md).

**Important:** As an admin and analyst, you can evaluate the remediation task rules for selected test results in the Vulnerability Manager Workspace. This method is more efficient than reapplying the remediation task rules in the classic UI, which is a time-consuming process. For more information, see [Re-evaluate the remediation properties of the records in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/task/vmws-reevaluate-remediation-parameters.md).

For example, you can group your test results by assignment group or technology and configuration item \(CI\). A different set of rules can be used for test results that expose the company to more risk. You can have one remediation task rule for low severity or low risk CIs. See [View Configuration Compliance test results](../task/view-vuln-config-compl-test-results.md) for more information on available fields.

When a new test result is imported, or reopened after being closed, the remediation task rules are evaluated against it. A test result is only evaluated once, unless it is reopened after being closed.

Remediation task rules are evaluated after CI matching, risk score calculations, and assignment rules.

The following process is used for each new or reopened test result:

-   For each remediation task rule, the test result is compared to the condition filter.
-   For each rule where the rule condition matches, it pulls the data from the group key columns on the test result. The rule checks to see if there is a matching **Open** remediation task that is assigned to the same assignment group as the test result.

    If the remediation task is found, the test result is added to the existing remediation task in the **Open** state.

-   If no remediation task in the **Open** state is found, the rule creates a remediation task, assigns it based on the **User Group** or **Key** value in the rule, and places the test result in it.


More than one test result rule can be defined, to group different kinds of results. Since each result is compared with the rule conditions before putting it in a remediation task, too many rules may have a performance impact.

When a remediation task rule is deleted, you have the option to delete all open tasks created by the rule. This applies to both the rule form view and list view.

When a remediation task assignment is made or changed, the **Assignment group** and the **Assigned to** fields roll down to all test results, except for those where the test result has a different assignment group than the RT. For more information on assignment rules, see [Configuration Compliance assignment rules overview](cc-assignment-rules.md). These assignments are used automatically for this group on the next import.

## Track deferral counts for test results and remediation tasks

Starting with v14.3, track the number of times a test result or a remediation task is deferred in the Multiple deferrals module. A scheduled job, **set deferral counts**, runs daily to post counts for records that are deferred more than once in the Deferral count column in the records that are listed in the Multiple deferrals module.


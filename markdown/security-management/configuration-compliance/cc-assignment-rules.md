---
title: Configuration Compliance assignment rules overview
description: Define the criteria by which test results are automatically assigned to an assignment group for remediation.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance assignment rules overview

Define the criteria by which test results are automatically assigned to an assignment group for remediation.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

A default assignment rule, **Assign to CI support group**, is included in the base system assigning test results to the **CI Support Group**. Inactive by default.

The Assignment groups set by the Assignment Rules are used by **Remediation Task Rules** to assign owners to remediation tasks \(RTs\).

## Assigning test results automatically

There are three different ways to assign test results using **Assign using**:

-   Assignment group: This option allows you to select any of the existing ServiceNow AI Platform® user groups.
-   Assignment Group Field: This option allows you to choose any assignment group field available using the cmdb\_ci table. By default you see the following three group fields:
    -   None: Indicates no default value for this mandatory field
    -   Configuration Item: Approval Group
    -   Configuration Item: Assignment Group
    -   Configuration Item: Support Group
-   Script: This option allows you to define the conditions using a script. This option requires coding or advanced ServiceNow® expertise.

See [Create or edit Configuration Compliance assignment rules](../task/create-cc-assign-rules.md) for more information on creating assignment rules.

With the sn\_vulc.remediation\_owner role, you can view and update test results and remediation tasks that are assigned to them or to their assignment groups. To view the modules, navigate to **All** &gt; **Configuration Compliance** &gt; **Test Results** &gt; **My Open Test Results**, or **Configuration Compliance** &gt; **Remediation Tasks** &gt; **My Open Tasks**.

The sn\_vulc.remediation\_owner role can be assigned directly to a user, or, it is automatically assigned when you assign a user the itil role.

## Assignment rule evaluation process

When a new test result is imported, or reopened after being closed, the assignment rules are evaluated against it. The assignment rules are evaluated after CI matching, and Risk Score calculations. A test result is only automatically evaluated upon initial import and when a rule is changed, unless it is reopened after being closed. You can manually reapply rules after changes.

The following process is used for each new or reopened test result:

-   For each test result assignment rule, the test result is compared to the assignment filter, lowest order rule first.
-   Where the condition matches, the test result is assigned an assignment group. The lookup stops.
-   Where the conditions do not find a match among all the rules, the test result remains unassigned.

## Reapplying assignment rules

When you change an assignment rule, use the **Apply Changes** button on the Assignment Rules list page to rerun all the changed rules on all active Open test results, except those that were manually assigned.

**Note:** The assignment rules do not reevaluate manually created assignments.

The scheduled job \[**Reapply all assignment rules**\] is inactive, by default. When activated, it evaluates all the open test results against all active rules except those manually assigned. It can run Daily, Weekly, Monthly, Periodically, Once or On Demand.

**Important:** As an admin and analyst, you can obtain the latest assignments for selected test results in the Vulnerability Manager Workspace. This method is more efficient than reapplying the Assignment Rules for all test results in the classic UI, which is a time-consuming process. For more information, see [Re-evaluate the remediation properties of the records in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/task/vmws-reevaluate-remediation-parameters.md).

## Assignment rules and remediation task assignment

Usually, you would assign your remediation task \(RT\) to the same assignment group as the test results in it. That is what the remediation task rules do, by default.

For example, if your RT groups by configuration item class, the remediation task created can be broken apart by the different assignment groups. An Oracle Database TRG can be assigned to Group 1, and an Oracle Database TRG assigned to Group 2.

When the assignment group is changed at the remediation task level, all the test results in that remediation task which have same assignment group are updated to the new assignment group. The test results are marked as manually assigned and are not eligible for further rule evaluation.


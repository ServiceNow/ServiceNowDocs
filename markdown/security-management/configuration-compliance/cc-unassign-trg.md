---
title: Remove assignments from remediation tasks for you or your groups
description: Reassign the test result records in the Configuration Compliance application if the records have been incorrectly assigned to you or your group.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-05-29"
reading_time_minutes: 2
breadcrumb: [Configuration Compliance remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Remove assignments from remediation tasks for you or your groups

Reassign the test result records in the Configuration Compliance application if the records have been incorrectly assigned to you or your group.

## Before you begin

Role required: sn\_vulc.remediation\_owner

## About this task

Starting with v14.3 of the Configuration Compliance application,If you determine that remediation tasks \(RTs\) and their associated test results aren't within your scope for remediation, or if you think that records have been incorrectly assigned to you or to your groups, you can remove yourself or your groups from the Assigned to and Assignment group fields on RT records.

The **Unassign** button is displayed on remediation task records in any state other than the Closed or Resolved states.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to a remediation task record that is assigned to you that is in any state other than Closed or Resolved.

2.  To clear the **Assigned to** and **Assignment group** fields, at the top of the record, select **Unassign**.

3.  In the **Unassign** dialog, provide work notes and select **Submit**.

    -   The work notes that you provided are displayed in the Notes section.
    -   On the **State Change Approval** tab, the state change approval record \(CA\#\) displays the In Review state, which helps you to track the approval workflow.
    -   On the **Requested Approvals** tab, your request for the removal of you or your assignment group is displayed as the Requested state.

## Result

The request is approved by using a default, one-level approval workflow. For more information, see [Approve an unassign request in Configuration Compliance](approve-an-unassign-request-in-configuration-compliance.md).

-   If your request is approved, the state change approval record and the requested approval record transition to **Approved**. You and your groups are removed from the **Assigned to** and **Assignment group** fields. `Unassigned` is displayed in the **Assignment type** field, and the remediation task is displayed on the list of the Unassigned module for the Configuration Compliance application.

    Notifications that records are unassigned are sent automatically to vulnerability managers or analysts in the Unassign notification group. For more information about the notifications and the properties for this feature, see [Removing assignments from Configuration Compliance test result groups](../concept/cc-unassigninng-trg.md).

-   If your request is rejected, the state change approval record and the requested approval record transition to Rejected.

**Note:** As a vulnerability administrator, you can set the **sn\_vulc.unassign\_test\_result\_group.approval\_required** system property to **false** to disable the approval process.

## What to do next

Navigate to the Unassigned module for the Configuration Compliance application monitor any unassigned records for items that might fall under your scope, and then reassign them to yourself.

**Parent Topic:**[Configuration Compliance remediation](../concept/vuln-config-compl-remediation.md)


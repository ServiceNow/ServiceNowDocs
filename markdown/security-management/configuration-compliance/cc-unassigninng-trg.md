---
title: Removing assignments from Configuration Compliance remediation tasks
description: You can clear the Assigned to and Assignment group fields on remediation tasks and their associated test results directly from the test result records and remediation tasks that you determine might be incorrectly assigned to you or your groups.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Assignment rules, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Removing assignments from Configuration Compliance remediation tasks

You can clear the **Assigned to** and **Assignment group** fields on remediation tasks and their associated test results directly from the test result records and remediation tasks that you determine might be incorrectly assigned to you or your groups.

## Overview of the workflow

Remediation owners can update records for reassignment with the **Unassign** button.

## Use case for sn\_vulc.remediation\_owner

If you determine that RTs and their associated test results aren't within your scope for remediation, or if you think that records have been incorrectly assigned to you or to your groups, you can remove yourself or your groups from the **Assigned to** and **Assignment group** fields on those remediation task records.

## Unassign module

The **Unassign** button is displayed on the remediation task and test result records in any state other than the Closed or Resolved states.

If you select **Unassign**, you are prompted that all the associated test results with the remediation task are reassigned and transition to the **Unassigned** assignment type.

**Note:** If any test result on a remediation task has a different assignment group than its remediation task, it is not unassigned. In most cases, these test results have been manually assigned.

Any records that you update with either the UI button or manually, are displayed on the Unassigned module under Configuration Compliance.

For the steps to reassign records using the **Unassigned** UI action, see [Remove assignments from remediation tasks for you or your groups](../task/cc-unassign-trg.md).

## System property and notifications

If you are an administrator with the sn\_vulc.vulnerability\_admin role, when you select **Unassign** on a record, by default, the system property, **sn\_vulc.unassign\_test\_result\_group.approval\_required** triggers the State Change Approval record and Requested Approval record. Also, the request displays in the My Approvals list of the approver.

**Note:** As a vulnerability administrator, you can set the **sn\_vulc.unassign\_test\_result\_group.approval\_required** system property to **false** to disable the approval process.

-   If the approver approves your request, by default, the system property, **sn\_vulc.default\_assignment\_group** clears the Assigned to and Assignment group fields, and populates the Assignment type field with **Unassigned**. As a vulnerability administrator, you can change the value in the **sn\_vulc.default\_assignment\_group** system property so that the assignment fields are cleared and a specific group is then assigned. For example, if a user selects **Unassign** on a record and you want to redirect it to a specific group for review, you can add a system ID for the group of your choice in the value field of the system property.
-   If the approver rejects your request, the reason for rejection displays in the **Notes** tab.

Alternatively, if **sn\_vulc.default\_assignment\_group** is not configured for a specific group, by default, users that you add to the Unassign notification user group are alerted when records are unassigned. The system property, **sn\_vulc.default\_notification\_group** determines the notifications to this group.

The assignment type, whether it's **Manual**, **Rule**, or **Unassigned**, is available from the RT records and the list view. The **Unassigned** assignment type is displayed after the **Assigned to** and **Assignment group** fields are cleared by the system property of the feature.

## Monitoring your assignment rules with the scheduled job for this feature

A daily scheduled job counts the records when they transition to the **Unassigned** assignment type. With this count, vulnerability analysts can monitor and adjust any assignment rules that might not be performing well based on any assignment rules that have higher counts of unassigned RTs.

The **Reassignment count for assignment rules** scheduled job runs daily and posts the total number of RTs that are unassigned by this feature for a particular assignment rule.

The job also counts any records that are manually unassigned. Both the manual counts and the counts that are gathered by this feature are posted on the Vulnerability Assignment Rules list in two columns: **Reassignment count - manual items** and **Reassignment count - unassigned items**.

![Reassignment count for an assignment rule for remediation task.](../image/cc-unassigned-count.png)

1.  As a vulnerability administrator, you can view these counts by navigating to **Configuration Compliance** &gt; **Administration** &gt; **Assignment Rules**.
2.  Select the gear icon in the upper right of the list and select the **Reassignment count - manual items**, and **Reassignment count - unassigned items** for display.
3.  Any RT that was originally assigned by a rule but later was automatically or manually reassigned, contains a reference to the original rule in the list view.


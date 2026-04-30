---
title: Removing assignments from findings and remediation tasks
description: You can remove yourself or your group from the Assigned to and Assignment group fields on findings and remediation tasks if you believe they were incorrectly assigned.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Assigning findings to remediation teams using assignment rules, Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Removing assignments from findings and remediation tasks

You can remove yourself or your group from the **Assigned to** and **Assignment group** fields on findings and remediation tasks if you believe they were incorrectly assigned.

## Overview of the workflow

Remediation owners and vulnerability analysts can unassign records using the **Unassign** UI action. This helps route records that are outside their scope to the appropriate owners.

## Use case

Use the **Unassign** option when a finding or remediation task is not relevant to your scope or was mistakenly assigned to you or your group.

## Unassigning from findings and remediation tasks

You can unassign records in any state except Closed or Resolved, using the **Unassign** button or the More options menu \(![Vertical dots](../../secops-analyst-workspace/image/more-actions-icon.png)\).

**Supported Records**:

-   **Remediation tasks**: When a remediation task is unassigned, all associated findings with the same assignment group are also unassigned.

    **Note:** Items with a different assignment group than their remediation task are not unassigned, as they are likely manually assigned.

-   **Findings**: Records unassigned manually or via UI appear under the **Unassigned** module.

Any records that you update assignments for with the UI action or manually are displayed on the Unassigned module.

## Approval workflow and system properties

By default, unassigning a record triggers an approval workflow if the system property **sn\_vul.unassign\_vr.approval\_required** is set to **true**. This generates an approval request that appears under **My Approvals**. If approved:

-   The Assigned to and Assignment group fields are cleared.
-   The Assignment type is set to Unassigned.
-   The record can be optionally reassigned to a group defined in **sn\_vul.default\_assignment\_group**.
-   Notifications are sent to the new group.
-   If rejected, the reason appears in the **Notes** tab.


As a vulnerability administrator, you can:

-   Disable approvals by setting **sn\_vul.unassign\_vr.approval\_required** to **false**.
-   Redirect unassigned records to a specific group by setting its sys\_id in **sn\_vul.default\_assignment\_group**.
-   Manage notifications using the **Unassign notification user group** if no default group is set.

The Assignment type \(Manual, Rule, or Unassigned\) helps identify how a record was last assigned. When unassigned, this field is set to Unassigned and is visible on both the record and list views.

## Monitoring unassignments with scheduled jobs

A daily **Reassignment count for assignment rules** scheduled job tracks unassigned records to assess assignment rule effectiveness. This job counts:

-   Findings reassigned to Unassigned.
-   Manually unassigned records.
-   System-unassigned records

These counts appear in the Assignment Rules list under the following columns:

-   Manual items count
-   Unassigned items count

To view reassignment counts:

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.
2.  Select **Administration** in the navigation pane.
3.  Select **Review** on the **Assignment rules** tile.
4.  On the **Rules** page, select **Assignment** in the navigation pane.
5.  Use the gear icon to add both reassignment columns to the list view.

Each reassigned record retains a reference to its original assignment rule. The list view displays reassignment counts for each assignment rule, helping you identify rules that may need adjustment.

The following example shows reassignment counts for two assignment rules.

![Reassignment counts for two assignment rules for Vulnerability Response VITs.](../../vulnerability-response/image/vr-reassignment-counts.png)

**Parent Topic:**[Assigning findings to remediation teams using assignment rules](sem-assigning-findings-to-remediation-teams.md)

**Related topics**  


[Remove assignments from findings and remediation tasks](sem-configure-assignment-rules.md#)

[Approve or reject an unassign request](../task/sem-approve-unassign-requests.md)


---
title: Configuring assignment rules
description: By configuring assignment rules, you can automate the process of routing findings to the appropriate teams or individuals. By defining assignment criteria based on vulnerability attributes or affected assets, you can ensure timely and accurate ownership for remediation efforts.Create rules to assign findings automatically based on specific filter conditions. These rules apply to items as they’re imported or manually created.Reapply assignment rules to rerun assignment logic on existing findings or groups after they’ve already been created.Delete assignment rules after careful consideration of potential impacts on the assignment logic and operational workflows.Clear the Assigned to and Assignment group fields on vulnerable item records in the Vulnerability Response, Application Vulnerability Response, and Container Vulnerability Response applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [assign findings to remediation teams automatically, assign vulnerable items to remediation teams automatically, assign application vulnerable items to remediation teams automatically, assign container vulnerable items to remediation teams automatically, configuring assignment rules]
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring assignment rules

By configuring assignment rules, you can automate the process of routing findings to the appropriate teams or individuals. By defining assignment criteria based on vulnerability attributes or affected assets, you can ensure timely and accurate ownership for remediation efforts.

Assignment rules help streamline vulnerability management by automatically assigning ownership to the correct team, reducing manual triage and accelerating response times.

In the Security Exposure Management Workspace, you can set up a single assignment rule that applies to all types of findings, including vulnerable items \(VITs\), application vulnerabilities \(AVITs\), container vulnerabilities \(CVITs\), and configuration test results \(CTRs\). This rule can then be applied to all the findings or a specific combination of findings.

Configuration of assignment rules includes the following steps.

**Parent Topic:**[Configure rules to manage findings](../task/sem-configure-rules-manage-findings.md)

**Related topics**  


[Assigning findings to remediation teams using assignment rules](sem-assigning-findings-to-remediation-teams.md)

## Create or edit assignment rules

Create rules to assign findings automatically based on specific filter conditions. These rules apply to items as they’re imported or manually created.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### About this task

With assignment rules, you define the conditions for assignment and the order in which they’re executed. Once a finding matches a rule condition, the assignment process stops.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Assignment rules** tile.

4.  On the Rules page, select **Assignment** in the navigation pane.

5.  Select **New** and fill in the fields on the form:

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Details

</td></tr><tr><td>

Name

</td><td>

Name of the assignment rule.

</td></tr><tr><td>

Applies to

</td><td>

Finding types the assignment rule applies to.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the assignment rule is active.

</td></tr><tr><td>

Description

</td><td>

Description of the assignment rule.

</td></tr><tr><td colspan="2">

If this condition is met

</td></tr><tr><td>

Condition fields

</td><td>

Conditions that must be met.

</td></tr><tr><td>

New condition set

</td><td>

Adds more condition filter fields to choose from.

</td></tr><tr><td colspan="2">

Then set this value

</td></tr><tr><td>

Assign using

</td><td>

To automate the assignment of groups created based on this rule, choose one of the options available.

-   User group: Select a user group from the lookup table.
-   User group field: Select a user group field from the list.
-   Script: Create or edit a script.

**Note:** Creating or editing a script requires ServiceNow expertise.

</td></tr></tbody>
</table>6.  Select **Save**.

    New or updated rules are evaluated on the next import.

7.  To edit the rule, select the rule and update the details as required.


## Reapply assignment rules

Reapply assignment rules to rerun assignment logic on existing findings or groups after they’ve already been created.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### About this task

Reapplying assignment rules is useful when:

-   Assignment rules are updated or newly created.
-   Findings were previously unassigned or incorrectly assigned.
-   You must reassign ownership based on updated business logic or CI ownership changes.

**Note:** You can reapply assignment rules for deferred items and manually assigned items basis system properties:**\(sn\_sec\_wf.enable\_deferred\_item\_reassignment**, **sn\_sec\_wf.enable\_manually\_assigned\_item\_reassignment**, that are set to false by default. Now, reassign items through the Re-evaluate action in the list view.

Normally, assignment rules are applied only once, when a finding is first created. If rules are changed or added later, existing findings don’t automatically update their assignment. Reapplying the rules enables you to bring all vulnerability findings into alignment with current rule logic. To reapply all vulnerability assignment rules, activate the **Reapply all vulnerability assignment rules** scheduled job. Set the **Run** field appropriately to prevent performance impacts, especially after the initial run.

**Note:** To reapply rules to a specific subset of findings, use the 'Evaluate rules' feature. This approach ensures efficient rule re-evaluation for targeted findings.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Assignment rules** tile.

4.  On the Rules page, select **Assignment** in the navigation.

5.  In the **Filter by** list, select the finding type for which you want to reapply the rules.

    **Note:** To reapply the rule to all the finding types, select **All**.

6.  Select **Reapply**.

    **Note:**

    -   Use the **Reapply** button on the Assignment Rules form if you haven't run the scheduled job.
    -   Reapplication overwrites existing assignment values based on the first matching rule.
    -   Reapplication does not regroup the findings.
    -   Test the rule logic thoroughly before applying it in bulk.

## Delete assignment rules

Delete assignment rules after careful consideration of potential impacts on the assignment logic and operational workflows.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### About this task

When you delete an assignment rule:

-   It’s removed from the rule table.
-   It doesn’t affect already-assigned records. Deletion helps prevent the rule from applying to new or updated records going forward.
-   Rules are evaluated in order. If a rule is deleted, the system evaluates the next matching rule.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Assignment rules** tile.

4.  On the Rules page, select **Assignment** in the navigation.

5.  Select the rule that you want to delete.

6.  In the assignment rules form, select the ellipses next to the **Update** button.

7.  Select **Delete**.


## Remove assignments from findings and remediation tasks

Clear the **Assigned to** and **Assignment group** fields on vulnerable item records in the Vulnerability Response, Application Vulnerability Response, and Container Vulnerability Response applications.

### Before you begin

Roles required:

-   sn\_vul.remediation\_owner or sn\_vul.vulnerability\_analyst for vulnerable items \(VITs\) and remediation tasks \(VULs\).
-   sn\_vul.app\_sec\_manager for Application Vulnerability Response vulnerable items \(AVITs\) and remediation tasks \(AVULs\).
-   sn\_vul\_container.remediation\_owner or sn\_vul\_container.vulnerability\_analyst for container vulnerable items \(CVITs\) and remediation tasks \(CVULs\).

### About this task

The **Unassign** UI action is supported in both the classic environment and the workspaces for the following records in any state other than Closed or Resolved:

-   Remediation tasks \(VULs, AVULs, and CVULs\). If a remediation task is updated with this feature, the **Assigned to** and **Assignment group** fields on all of its associated VITs that have the same assignment group are also cleared.
-   Vulnerable items \(VITs\).
-   Application vulnerable items \(AVITs\).
-   Container vulnerable items \(CVITs\).

**Important:** You can unassign host vulnerable items in bulk in the Vulnerability Manager Workspace. For more information, see [Using bulk edit in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/concept/vmws-using-bulk-edit.md).

### Procedure

1.  In either the classic environment, or in the IT Remediation Owner Workspace, navigate to a vulnerable item \(VIT\) record that is assigned to you that is in any state other than Closed or Resolved.

2.  To clear the **Assigned to** and **Assignment group** fields in the classic view, at the top of the record, select **Unassign**.

3.  Alternatively, navigate to a vulnerable item \(VIT, AVIT, or CVIT\) record in the IT Remediation workspace that is assigned to you or your groups and click **Unassign** in the More options menu \(![The three dots of the More options menu](../../security-incident-response/image/more-actions-icon.png)\) to clear the assignment fields.

4.  For remediation task records in the workspace that are assigned to you or your groups, open a record select **Unassign** in the More options menu \(![The three dots of the More options menu](../../security-incident-response/image/more-actions-icon.png)\) to clear the assignment fields.

5.  In the Unassign dialog for both vulnerable items and remediation tasks, provide work notes and select **Submit**.

    The state change approval request is submitted for approval.

    **Note:** For remediation tasks, you are notified that the **Assigned to** and **Assignment group** fields on all of a remediation task's associated VITs are also cleared.

    After the request to clear the fields is approved for a remediation task, all the **Assigned to** and **Assignment group** fields on its vulnerable items that have the same assignment group are also unassigned. If any vulnerable item has a different assignment group than its associated remediation task, it is not unassigned. In most cases these vulnerable items have been manually assigned.

6.  View the following information:

    -   The work notes that you provided is displayed in the Notes section.
    -   On the **State Change Approval** tab, the state change approval record displays with the In Review state, which helps to track the approval workflow.
    -   On the **Requested Approvals** tab, your request for the removal of you or your assignment group is displayed in the Requested state.

### Result

The request is approved by using a default, one-level approval workflow.

-   If your request is approved, the state change approval record and the requested approval record transition to the Approved state. You and your groups are removed from the **Assigned to** and **Assignment group** fields. `Unassigned` is displayed in the **Assignment type** field, and the remediation task and VITs are displayed in the list of the Unassigned module for each product.

    Notifications that records are unassigned are sent automatically to vulnerability managers or analysts in the Unassign notification group. To configure the approval flag, notifications, and default assignment group, see [Remove assignments from findings and remediation tasks](sem-configure-assignment-rules.md#).

-   If your request is rejected, the state of the change approval record and requested approval record transition to the Rejected state.

**Note:** As a vulnerability administrator, you can set the **sn\_vul.unassign\_vr.approval\_required** system property to **false** to disable the approval process.

### What to do next

Navigate to the Unassigned modules for the Vulnerability Response and Application Vulnerability Response Container Vulnerability Response applications, monitor any unassigned records for items that might fall under your scope, and reassign them to yourself.


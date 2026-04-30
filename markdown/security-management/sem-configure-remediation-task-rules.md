---
title: Configuring remediation task rules
description: By configuring remediation task rules, you can automatically group findings based on filter conditions.Create remediation task rules to automatically group findings based on filter conditions. These rules automatically group findings as they’re imported or manually created. Use the filter to limit the findings grouped by this rule, such as selecting all findings with exploits.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring remediation task rules

By configuring remediation task rules, you can automatically group findings based on filter conditions.

In the Security Exposure Management Workspace, you can set up a single assignment rule that applies to all types of findings, including vulnerable items \(VITs\), application vulnerabilities \(AVITs\), container vulnerabilities \(CVITs\), and configuration test results \(CTRs\). This rule can then be applied to all the findings or a specific combination of findings.

You can also configure the remediation task rule execution mode to control whether the system evaluates all matching rules \(Match All\) or stops at the first match \(Match First\).

**Related topics**  


[Grouping multiple findings as remediation tasks for easy processing using remediation task rules](sem-grouping-multiple-findings-remediation-tasks-processing.md)

## Create remediation task rules

Create remediation task rules to automatically group findings based on filter conditions. These rules automatically group findings as they’re imported or manually created. Use the filter to limit the findings grouped by this rule, such as selecting all findings with exploits.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### About this task

The base system ships with one remediation task rule, **Vulnerability**, which groups vulnerable items by vulnerability and assignment group \(from Assignment rules\). You can reapply the rules from the form or list view. For some sample entries, see Vulnerability Response remediation task rule examples.

This rule can be modified by using filter conditions and Group by choices. By default, remediation tasks use Assignment Rules, when available, as part of their filter criteria.

**Note:** If no assignment rules exist, you can select a group using the User group field.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Remediation task rules** tile.

4.  On the Rules page, select **Remediation task** in the navigation pane.

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

Name of the remediation task rule.

</td></tr><tr><td>

Applies to

</td><td>

Tables the remediation task rule applies to.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the remediation task rule is active.

</td></tr><tr><td>

Description

</td><td>

Description of the remediation task rule.

</td></tr><tr><td colspan="2">

If this condition is met

</td></tr><tr><td>

Case sensitive

</td><td>

Determines whether a condition is case sensitive or not.**Note:** The default value is case insensitive.

</td></tr><tr><td>

Condition fields

</td><td>

Conditions that must be met.

 By default, searches in the condition builder on task rule records and forms aren’t case-sensitive \(the Case sensitive check box is inactive\). If needed, you can enable case-sensitive searches by selecting the Case sensitive check box on the relevant task records and forms.

</td></tr><tr><td>

New condition set

</td><td>

Adds more condition filter fields to choose from.

</td></tr><tr><td colspan="2">

Group by

</td></tr><tr><td>

Group findings from

</td><td>

The table the rule uses to group the findings. Choices are:-   Finding \[sn\_vul\_vulnerable\_item\]
-   Finding &gt; Configuration Item \[cmdb\_ci\]
-   Finding &gt; Vulnerability
**Note:**

-   The **Group findings from** field updates based on the number of tables selected in the **Applies to** field. If one table is chosen, it shows the corresponding item. If multiple tables are chosen, it displays Findings.
-   You can add up to six grouping criteria.


</td></tr><tr><td>

Using field

</td><td>

Field on the table that the rule uses to group findings.

</td></tr><tr><td colspan="2">

Assignment

</td></tr><tr><td>

Assign remediation tasks by

</td><td>

When automatically assigning remediation tasks, the Assignment choice is used in addition to the Group By choices to group the findings. New tasks are created, as needed, to ensure that each finding is placed in a task with a matching assignment group set.

To automate the assignment of tasks created based on this rule, choose one of the options available.-   Group by field: If you selected any user group field from the Using field values in the Group by section, they appear in the drop-down menu.
-   User Group: Use the lookup list to select a static user group.


</td></tr></tbody>
</table>6.  Select **Save**.



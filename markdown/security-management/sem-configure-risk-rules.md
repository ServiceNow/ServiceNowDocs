---
title: Configuring roll-up calculator rules
description: Configure roll-up calculator rules to compute the cumulative risk score for remediation tasks and imported vulnerabilities.Create rules to roll-up risk scores on imported findings and remediation tasks.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring roll-up calculator rules

Configure roll-up calculator rules to compute the cumulative risk score for remediation tasks and imported vulnerabilities.

**Related topics**  


[Prioritizing vulnerabilities and other findings using roll-up calculators](sem-prioritizing-vulnerabilities-other-findings.md)

## Create or edit roll-up calculator rules

Create rules to roll-up risk scores on imported findings and remediation tasks.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Roll-up calculator rules** tile.

4.  On the Rules page, select **Roll-up calculator** in the navigation pane.

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

Name of the rule.

</td></tr><tr><td>

Target table

</td><td>

Name of the table from which the risk score must be rolled-up.

</td></tr><tr><td>

Target field

</td><td>

Name of the field from the table that must be considered for risk roll-up.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the rule is active.

</td></tr><tr><td>

Description

</td><td>

Description of the rule.

</td></tr><tr><td colspan="2">

Source selection

</td></tr><tr><td>

Applies to

</td><td>

The finding table to which the risk score roll-up applies to.

 The **Applies to** field is dependent on the selected target table, and its options are updated accordingly. For instance, choosing the Container remediation task \[sn\_vul\_container\_vulnerability\] limits the **Applies to** field options to Container vulnerable item. This dynamic update ensures that only relevant options are available based on the target table selected.

</td></tr><tr><td>

Include

</td><td>

Defines the conditions for roll-up on the finding table.

</td></tr><tr><td colspan="2">

Roll-up calculations

</td></tr><tr><td>

Basic

</td><td>

Assign weightage to specify the relative impact of each of the following factors on the rolled-up risk score:-   **Maximum risk score**: Maximum risk score of the findings considered.
-   **Average score**: Aggregate of the risk scores of all the findings.
-   **Count of records**: Number of findings. A larger number of findings increases the overall score, while a smaller number lowers it.


</td></tr><tr><td>

Script \(Advanced option\)

</td><td>

The scripting feature is an advanced feature to build a custom script that should return the risk score, which is an integer value ranging from 0 to 100.

</td></tr></tbody>
</table>6.  Select **Save**.



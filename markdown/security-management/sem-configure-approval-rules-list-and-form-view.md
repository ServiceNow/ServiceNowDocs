---
title: Create or edit approval rules
description: Create and activate an approval rule by selecting a rule type, choosing the target tables, defining conditions, and configuring approval levels.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Create or edit approval rules

Create and activate an approval rule by selecting a rule type, choosing the target tables, defining conditions, and configuring approval levels.

## Before you begin

Role required: sn\_vul\_container.vulnerability\_admin, sn\_vul\_cmn.vulnerability\_admin, sn\_vul.remediation\_owner, sn\_vulc.remediation\_owner, sn\_vul\_container.remediation\_owner

## Procedure

1.  Navigate to **All** &gt; **Security Exposure Management** &gt; **Administration** &gt; **Approval Rules**.

2.  Select **New** to create a rule.

    You’re required to have the necessary admin access to view the New button in the Approval Rules screen.

3.  On the form, fill/update the fields as per requirement.

<table id="table_vym_zlx_yhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule type

</td><td>

Determines the purpose of the approval \(e.g., false positive, exception\). The available types depend on the selected target tables.

</td></tr><tr><td>

Applies to

</td><td>

One or more tables where the approval rule is evaluated. Multi-table selection limits condition fields to common \(intersection\) fields only.

</td></tr><tr><td>

Condition

</td><td>

Defines when the approval is triggered. Available fields depend on selected tables.

</td></tr><tr><td>

Order

</td><td>

Execution order of various configurations within a rule. For example, a configuration with an order entry of 100 runs before a configuration with an order entry of 200.

</td></tr><tr><td>

Approval expiry

</td><td>

Maximum time allowed for approvers to take action. Must be greater than 0 and must not be less than Notify expiry.

</td></tr><tr><td>

Notify expiry

</td><td>

Number of days after which the approver notification expires. Cannot exceed approval expiry.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the rule can be used. Activation requires at least one approval level.

</td></tr></tbody>
</table>    -   Rules remain inactive until approval levels are configured.
    -   Only intersection fields appear for multi-table conditions.
    -   At least one valid approver is required for each table included in the rule.
    -   Notify expiry cannot exceed approval expiry.
    -   Negative expiry values are not accepted.
    -   Adding new approvers after a request is created does not change existing approval tasks.
4.  Select a **Rule type**.

5.  Select one or more tables in **Applies to**.

    Only fields common to all selected tables appear in the Condition builder when defining the rule conditions.

6.  Define the rule **Condition**.

7.  Enter **Approval expiry \(days\)** and **Notify expiry \(days\)**.

    Notify expiry must not exceed approval expiry. Negative values aren’t enabled.

8.  Enable the **Active** flag.

    The rule can’t be activated without approval levels. Approval rules remain inactive until you add at least one approval level. Multi-table rules enable only common fields while defining conditions.

9.  Select **Save** to create the rule record.

    The rule is active and routed based on the defined levels, tables, and conditions.



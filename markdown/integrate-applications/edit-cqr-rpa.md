---
title: Update a code quality rules form in RPA Hub
description: Update few fields in the code quality rule form to set the code quality check standard.Use the Code quality rule form to view a rule along with description and type.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Code quality check, Use, RPA Hub, Workflow Data Fabric]
---

# Update a code quality rules form in RPA Hub

Update few fields in the code quality rule form to set the code quality check standard.

## Before you begin

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Code Quality Rules**.

4.  Open a rule that you want to modify.

5.  Update the following fields as appropriate:

    -   **Severity**
    -   **Regular Expression** or **Value**
    -   **Active**
6.  Select **Save**.


**Parent Topic:**[Code quality check in RPA Hub](../concept/code-quality-check-rpa.md)

## Code quality rule form in RPA Hub

Use the Code quality rule form to view a rule along with description and type.

<table id="table_ucf_k2x_2rb"><thead><tr><th>

Name of the rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Code

</td><td>

Unique number of the rule.

</td></tr><tr><td>

Name

</td><td>

Short description of the rule.

</td></tr><tr><td>

Type

</td><td>

Type of the rule.-   Regular Expression
-   Integer
-   None

</td></tr><tr><td>

Active

</td><td>

Sets the rule as active or inactive.On clearing this option, the **Code Quality Check** feature in RPA Desktop Design Studio will not consider this rule while inspecting an automation or an activity for a code quality check.

</td></tr><tr><td>

Severity

</td><td>

Severity type of the rule.-   Error
-   Warning
-   Information

</td></tr><tr><td>

Regular Expression

</td><td>

Expression to define naming conventions.This field appears only when the type is **Regular Expression**.

</td></tr><tr><td>

Value

</td><td>

Value based on the type of the rule and description.This field appears when the type is **Integer**.

</td></tr><tr><td>

Description

</td><td>

Brief description of the rule.

</td></tr></tbody>
</table>**Related topics**  


[Code quality check in RPA Hub](../concept/code-quality-check-rpa.md)

[View the code quality rules list in RPA Hub](view-cqr-rpa.md)

[Code quality rules list in RPA Hub](../reference/cqr-list-rpa.md)


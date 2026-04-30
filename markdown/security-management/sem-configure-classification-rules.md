---
title: Configuring classification rules
description: By configuring classification rules, you can ensure consistent categorization and processing of vulnerabilities, discovered items and other finding related entities based on key attributes. This helps the system route findings to the correct tables, apply the appropriate grouping, assignment, and remediation rules, enhance reporting accuracy, and determine which business logic to use \(such as prioritization and remediation targets\).Create groups so that the underlying rules of this group can classify the entities or records in a specified table based on the conditions. The rules can be used to select any field in the corresponding table.Create rules to classify entities or records in the specified table into choice of classifications for use in downstream process or rules. .Rerun all active rules on all the findings when you modify a classification rule. You can also update existing vulnerabilities by applying the new classification rules.Deactivate or delete a classification rule if it is no longer needed or relevant.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [configure classification rules]
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring classification rules

By configuring classification rules, you can ensure consistent categorization and processing of vulnerabilities, discovered items and other finding related entities based on key attributes. This helps the system route findings to the correct tables, apply the appropriate grouping, assignment, and remediation rules, enhance reporting accuracy, and determine which business logic to use \(such as prioritization and remediation targets\).

Configuration of classification rules includes the following steps.

**Related topics**  


[Categorizing findings and discovered items using classification rules](sem-categorizing-findings-discovered-items.md)

## Create and edit a classification group

Create groups so that the underlying rules of this group can classify the entities or records in a specified table based on the conditions. The rules can be used to select any field in the corresponding table.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Review** on the **Classification rules** tile.

3.  On the Rules page, select **Classification** in the navigation pane.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_z5k_bwb_glb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Details

</td></tr><tr><td>

Name

</td><td>

Name of the new classification group.

</td></tr><tr><td>

Table

</td><td>

Table based on which the rules are executed.**Note:** The base system includes classification groups for discovered items and vulnerability entries.

</td></tr><tr><td>

Active

</td><td>

Option to activate the group.

</td></tr><tr><td>

Description

</td><td>

Description of the new classification group.

</td></tr></tbody>
</table>6.  Select **Save**.


## Create or edit classification rules

Create rules to classify entities or records in the specified table into choice of classifications for use in downstream process or rules. .

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Classification rules** tile.

4.  On the Rules page, select **Classification** in the navigation pane.

5.  Select a classification group.

6.  Select **New rule** and fill in the fields on the form:

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Details

</td></tr><tr><td>

Name

</td><td>

Name of the new classification rule.

</td></tr><tr><td>

Active

</td><td>

Option to activate the rule.

</td></tr><tr><td>

Classification group

</td><td>

Classification group for which the rule is being created. This field is auto-populated.

</td></tr><tr><td>

Description

</td><td>

Description of the new classification rule.

</td></tr><tr><td colspan="2">

If this condition is met

</td></tr><tr><td>

Condition type

</td><td>

Type of condition for the rule. Choices are as follows:-   **Filter**: Basic filter conditions for determining whether to use the rule or not.
-   **Filter group**: Set of multiple conditions that are used together. The rule is evaluated based on the conditions defined in the filter group.
-   **Script**: Scripted condition used to determine when to apply this rule.
This field appears only when the **Advanced view** option is selected.

</td></tr><tr><td>

Condition

</td><td>

Condition for the rule. Define conditions based on the column selected on the required vulnerability entry column. You can add multiple conditions to refine the rule. This field appears only when **Filter** is selected from the **Condition type** field.**Note:** When defining multiple conditions or templates, you can select only from a parent and a child table. You can’t select from two or more child tables.

</td></tr><tr><td>

Filter group

</td><td>

Group of filters. The group is defined when a set of conditions is used repeatedly in multiple places. Select the lookup using the list icon \(![Lookup list icon](../../vulnerability-response/image/lookup_list_icon.png)\) to select the filter group. For more information, see [Create and define filter groups in Security Operations](https://www.servicenow.com/docs/bundle/yokohama-security-management/page/product/security-operations-common/task/create-filter-group.html). This field appears only when **Filter group** is selected from the **Condition type** field.

</td></tr><tr><td>

Script

</td><td>

Script that is evaluated to determine when to apply this rule. You can write your code and set the response as either true or false. This field appears only when **Script** is selected from the **Condition type** field

</td></tr><tr><td colspan="2">

Set these values

</td></tr><tr><td>

Classification

</td><td>

Classification of the rule. The list includes the following options:-   Platform
-   Application
-   Service
-   Business Application
 Alternatively, you can enter your own classification that is not in the list.

</td></tr><tr><td>

Classification type

</td><td>

Type of classification. This field shows the filtered list of classification types based on your selected value for the **Classification** field.

</td></tr><tr><td>

Value type

</td><td>

Type of the value that is assigned by using this rule. Choices are as follows:-   **Template**: Select a template. You can use a required template.
-   **Script**: Select a pre-existing script, or write your own custom script.
This field appears only when the **Advanced view** option is selected.

</td></tr><tr><td>

Field

</td><td>

Option to select another field for the rule apart from the **Classification** and **Classification type** fields. Select a combination of fields and values that you want to set when the rule is evaluated.

</td></tr><tr><td>

Script value

</td><td>

Script to set values on the current record. This field defines what values to set on the fields in vulnerability entries. This field appears only when **Script** is selected from the **Value type** field.

</td></tr></tbody>
</table>7.  Select **Save**.


## Reapply a classification rule to existing records in the table

Rerun all active rules on all the findings when you modify a classification rule. You can also update existing vulnerabilities by applying the new classification rules.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Classification rules** tile.

4.  On the Rules page, select **Classification** in the navigation.

5.  Select the classification group or rule you want to reapply.

6.  Select **Reapply**.


## Deactivate or delete a classification rule

Deactivate or delete a classification rule if it is no longer needed or relevant.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### About this task

When a classification rule is deactivated or deleted, the data that was populated in the **Classification** and **Classification\_type** fields by that deleted rule remains in their respective tables.

If you want to clear this data, create a rule with empty values in the **Classification** and **Classification\_type** fields and reapply the group. Once this new rule is reapplied, the changes are reflected on all the records that this rule is applicable for, based on the conditions of the rule.

If a classification rule is deleted or deactivated, it’s no longer applied to the specified table and the data in the **Classification** and **Classification\_type** fields get cleared.

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Classification rules** tile.

4.  On the Rules page, select **Classification** in the navigation.

5.  Select the rule that you want to delete.

6.  In the classification rules form, select the ellipses next to the **Update** button.

7.  Select **Delete**.

    **Note:** If you don't click this button, the rule continues to reside in the system. Findings referenced by the rule continue to reference them.



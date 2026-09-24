---
title: Create a business rule
description: You can create any type of business rule to run when a record is displayed, inserted, updated, or deleted, or when a table is queried.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/t\_CreatingABusinessRule.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Classic Business rules, Build workflows]
---

# Create a business rule

You can create any type of business rule to run when a record is displayed, inserted, updated, or deleted, or when a table is queried.

## About this task

**Note:** These instructions and examples provide general guidance for how to implement this functionality. For help with unique use cases, refer to the [Developer Community Forum](https://community.servicenow.com/community?id=community_forum&sys_id=75291a2ddbd897c068c1fb651f9619f3), where you can ask questions, interact with other developers, and search for existing solutions.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

    **Note:** You might need to configure the form to see all fields.

<table id="table_bb2_yq3_bp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the business rule.

</td></tr><tr><td>

Table

</td><td>

Select the table that the business rule runs on.**Note:** The list shows only tables and database views that meet the scope protections for business rules. Business rules defined for a database view can run only on **Query**. A business rule for a database view cannot run on insert, update, or delete.

</td></tr><tr><td>

Application

</td><td>

Application that contains this business rule.

</td></tr><tr><td>

Accessible from

</td><td>

Scope protection for a global business rule. **Note:** This field is visible only when the **Table** field is set to **Global**. It does not apply to rules that run on specific tables.

</td></tr><tr><td>

Active

</td><td>

Select this check box to enable the business rule.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to see the advanced version of the form.

</td></tr><tr><td colspan="2">

When to run

</td></tr><tr><td>

When

</td><td>

\[Advanced\] Select when this business rule should execute: **display**, **before**, **async**, or **after** the database operation is complete.

 **Note:** Consider setting the **Order** for **async** business rules as the system uses this value when creating the associated scheduled job.

Newly created **async** business rules run automatically on upgrade.

Existing **async** business rules can be migrated to use the new async behavior.

</td></tr><tr><td>

Order

</td><td>

\[Advanced\] Enter a number indicating the sequence in which this business rule should run. If there are multiple rules on a particular activity, the rules run in the order specified here, from lowest to highest.

</td></tr><tr><td>

Insert

</td><td>

Select this check box to execute the business rule when a record is inserted into the database.

</td></tr><tr><td>

Update

</td><td>

Select this check box to execute the business rule when a record is update.

</td></tr><tr><td>

Delete

</td><td>

\[Advanced\] Select this check box to execute the business rule when a record is deleted from the database.

</td></tr><tr><td>

Query

</td><td>

\[Advanced\] Select this check box to execute the business rule when a table is queried.

</td></tr><tr><td>

Filter Conditions

</td><td>

Use the condition builder to determine when the business rule should run based on the field values in the selected Table.If you select the **Advanced** option, you can also use the **Condition** field to build a condition with a script. Conditions defined with the **Filter Conditions** field and advanced **Conditions** field are evaluated at the same time.

**Note:** Filters based on string compares are case-sensitive.

</td></tr><tr><td>

Role Conditions

</td><td>

Select the roles that users who are modifying records in the table must have for this business rule to run.

</td></tr><tr><td colspan="2">

Actions

</td></tr><tr><td>

Set field values

</td><td>

Set values for fields in the selected Table using the choice lists:-   The field
-   The assignment operator:
    -   **To:** An exact value
    -   **Same as:** The value of another field
    -   **To \(dynamic\):** A value relative to the user configuring the business rule or a user with a specific role
-   The value


</td></tr><tr><td>

Add message

</td><td>

Select this check box and enter a message that appears when this business rule is run

</td></tr><tr><td>

Abort action

</td><td>

Select this check box to abort the current database transaction. For example, on a before insert business rule, if the conditions are met, do not insert the record into the database.

 If you select this option, you cannot perform additional actions on the record, such as setting field values and running scripts. You can still display a message to users by selecting the **Add message** check box and composing the message.

</td></tr><tr><td colspan="2">

Advanced

</td></tr><tr><td>

Condition

</td><td>

Create a JavaScript conditional statement to specify when the business rule should run. By adding the condition statement to this field, you tell the system to evaluate the condition separately and run the business rule only if the condition is true. If you decide to include the condition statement in the **Script** field or the **Filter Conditions** field, leave this field blank. Conditions defined with the **Filter Conditions** field and advanced **Conditions** field are evaluated at the same time.

To have the instance reevaluate the condition statement a second time before running an async business rule, add the system property **glide.businessrule.async\_condition\_check** and set the value to true.

</td></tr><tr><td>

Script

</td><td>

\[Advanced\] Create a script that runs when the defined condition is true.

-   onAfter
-   onAsync
-   onBefore
-   onDisplay
 For more information and examples, see [Example business rule scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/business-rule-examples.md).

</td></tr><tr><td colspan="2">

Related list: Versions

</td></tr><tr><td>

Versions

</td><td>

Shows all versions of the business rule. Use this list to compare versions or to revert to a previous version.

</td></tr></tbody>
</table>4.  Click **Submit**.


If you run into issues with your business rule, see the [Business Rule FAQ \[KB0965707\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0965707) article in the Now Support Knowledge Base.

**Parent Topic:**[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRules.md)


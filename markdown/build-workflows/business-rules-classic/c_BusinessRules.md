---
title: Classic Business rules
description: A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/c\_BusinessRules.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Build workflows]
---

# Classic Business rules

A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.

Business rules are scripts that run when certain server-side conditions are met. Business rule conditions include when to run a business rule in relation to a database operation, and what record operations the business rule applies to. There are other scripting options available on the platform for client-side conditions, such as client scripts and UI actions.

**Note:** Business rules are a classic automation solution that rely on scripting. Use Workflow Studio for any new process automation to create automations that are easier to extend, reuse, understand, and upgrade. As many organizations have business rules in production, use this documentation to learn how to work with existing business rules.

To configure business rules, you first need to determine when the business rule should run and what action it should take.

## When business rules run

To configure business rules, you first need to determine when the business rule should run and what action it should take.

Business rules run based on two sets of criteria.

-   When to run the business rule in relation to a database operation.
-   What record operation the business rule applies to.

The following options are provided to determine when the business rule should run.

<table id="table_w2s_1k3_bp"><thead><tr><th>

Option

</th><th>

When the rule runs

</th></tr></thead><tbody><tr><td>

Before

</td><td>

After the user submits the form but before any action is taken on the record in the database.

</td></tr><tr><td>

After

</td><td>

After the user submits the form and after any action is taken on the record in the database.

</td></tr><tr><td>

Async

</td><td>

After the user submits the form and after the scheduler runs the scheduled job created from the business rule. The system creates a scheduled job from the business rule after the user submits the form but before any action is taken on the record in the database. **Note:** Newly created business rules will run during upgrades.

If a record has an asynchronous business rule that makes decisions based on the data in the record, multiple updates to the record in quick succession can cause the business rule to execute out of order or incorrectly.

If multiple async business rules update the same record, the updates performed by one script could be overwritten by another script or made in an unexpected sequence because the order of execution isn't guaranteed. You can use the After option for business rules or [System Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/system-events/events.md) as an alternative in these situations.

</td></tr><tr><td>

Display

</td><td>

Before the form is presented to the user, just after the data is read from the database.

</td></tr></tbody>
</table>**Note:**

-   Asynchronous business rules do not have access to the previous version of a record. Therefore, the changes\(\), changesTo\(\), and changesFrom\(\) GlideElement methods do not work with async rule script. However, the condition builder and condition field \(advanced view\) both support the changes\(\), changesTo\(\), and changesFrom\(\) methods.
-   Business rules do not honor ACLs until you want them to be honored. For more information, see [Relationship between Business Rules and Access Control Rules \(ACLs\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0656366)

The following options are provided to determine what record operations the business rule applies to.

|Option|When the rule runs|
|------|------------------|
|Insert|When the user creates a new record and the system inserts it into the database.|
|Update|When the user modifies an existing record.|
|Query|When the user queries for a record or list of records. Typically you should use the query operation for before business rules. Only query business rules on the table queried are executed—not query business rules on the tables of reference fields.|
|Delete|When the user deletes a record.|

**Note:** Business rules only run record operations when called from the GlideRecord API. Some applications intentionally bypass business rule processing to perform record operations directly. In addition, business rules ignore API calls run with the setWorkflow\(\) method set to false.

This image shows when different types of business rules run:

\[Omitted image "BusinessRuleProcessingFlow.png"\] Alt text:

**Note:** Business rules apply consistently to records regardless of whether they are accessed through forms, lists, or web services. This is one major difference between business rules and client scripts, which apply only when the form is edited.

## Business rule actions

Business rules can perform a variety of actions. Common types of actions are:

-   Changing field values on a form that the user is updating. Field values can be set to specific values available for that field, values copied from other fields, and relative values determined by the user's role.
-   Displaying information messages to the user.
-   Changing values of child tasks based on changes to parent tasks.
-   Preventing users from accessing or modifying certain fields on a form.
-   Aborting the current database transaction. For example, if certain conditions are met, prevent the user from saving the record in the database.

Administrators can set field values, create information messages, and abort transactions without writing a script.

## Prevent recursive business rules

Avoid using current.update\(\) in a business rule script. The update\(\) method triggers business rules to run on the same table for insert and update operations, leading to a business rule calling itself over and over. Changes made in before business rules are automatically saved when all before business rules are complete, and after business rules are best used for updating related, not current, objects. When a recursive business rule is detected, the system stops it and logs the error in the system log. However, current.update\(\) causes system performance issues and is never necessary.

You can prevent recursive business rules by using the setWorkflow\(\) method with the false parameter. The combination of the update\(\) and setWorkflow\(\) methods is only recommended in special circumstances where the normal before and after guidelines mentioned above don't meet your requirements.

-   **[Business rules in scoped applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRulesInScopedApps.md)**  
Every business rule is assigned to either a private application scope or to the global scope.
-   **[Create a business rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/t_CreatingABusinessRule.md)**  
You can create any type of business rule to run when a record is displayed, inserted, updated, or deleted, or when a table is queried.
-   **[Global variables in business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_UsingPredefinedGlobalVariables.md)**  
Predefined global variables are available for use in business rules.
-   **[Control field values using business rules and client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/r_BsnsRlClntScptsCntrlFldVl.md)**  
Implement both business rules and client scripts for a field to enable users to set record values properly using both forms and lists, and to see immediate changes to the values in forms as edits are made.
-   **[Display business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_ScriptingWithDisplayBusinessRules.md)**  
Display business rules are processed when a user requests a record form.
-   **[Task Active State Management business rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_TaskActiveStateMgmtBusRule.md)**  
The Task Active State Management business rule determines whether the active field value needs to change based on changes to the **State** field.
-   **[Installation settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_InstallationSettings.md)**  
Installation settings are global business rules with calculated names. Installation settings are calculated just before a record is displayed and facilitate dynamic determination of access and roles. Installation Settings permit the programmatic determination of a setting.
-   **[Example business rule scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/business-rule-examples.md)**  
Find an example business rule script that helps you with a requirement of your organization.

**Parent Topic:**[Build workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/build-workflows.md)


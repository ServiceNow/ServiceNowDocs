---
title: Classic Business rules
description: A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.To configure business rules, you first need to determine when the business rule should run and what action it should take.Every business rule is assigned to either a private application scope or to the global scope.You can create any type of business rule to run when a record is displayed, inserted, updated, or deleted, or when a table is queried.Predefined global variables are available for use in business rules.Implement both business rules and client scripts for a field to enable users to set record values properly using both forms and lists, and to see immediate changes to the values in forms as edits are made.The string NULL has a particular role in scripts and is a reserved word.Display rules are processed when a user requests a record form.This business rule determines whether the active field value needs to change based on changes to the State field.Find an example business rule script that helps you with a requirement of your organization.It is possible to compare two date fields or two date and time fields in a business rule, and abort a record insert or update if they are not correct.Fields in XML format can be parsed with the system's getXMLText function.In a before business rule script, you can cancel or abort the current database action using the setAbortAction\(\) method.You can write a script for a business rule that is triggered on more than one database action.An OR condition can be added to any query part within a business rule.A field defined as a glide list is an array of values stored in a single field.Use indexOf\("searchString"\) to return the location of the string passed into the method if the glide list field, such as a Watch list, has at least one value in it.You can lock user accounts if the user is not active.You can use a query business rule that executes before a database query is made.
locale: en-US
release: australia
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 29
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Classic Business rules

A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.

Business rules are scripts that run when certain server-side conditions are met. Business rule conditions include when to run a business rule in relation to a database operation, and what record operations the business rule applies to. There are other scripting options available on the platform for client-side conditions, such as client scripts and UI actions.

**Note:** Business rules are a classic automation solution that rely on scripting. Use Workflow Studio for any new process automation to create automations that are easier to extend, reuse, understand, and upgrade. As many organizations have business rules in production, use this documentation to learn how to work with existing business rules.

**Parent Topic:**[Server-side scripting](../../server-scripting/concept/c_ServerScripting.md)

## How business rules work

To configure business rules, you first need to determine when the business rule should run and what action it should take.

### When business rules run

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

If multiple async business rules update the same record, the updates performed by one script could be overwritten by another script or made in an unexpected sequence because the order of execution isn't guaranteed. You can use the After option for business rules or System Events as an alternative in these situations.

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

![](../image/BusinessRuleProcessingFlow.png "Business rule processing flow")

**Note:** Business rules apply consistently to records regardless of whether they are accessed through forms, lists, or web services. This is one major difference between business rules and client scripts, which apply only when the form is edited.

### Business rule actions

Business rules can perform a variety of actions. Common types of actions are:

-   Changing field values on a form that the user is updating. Field values can be set to specific values available for that field, values copied from other fields, and relative values determined by the user's role.
-   Displaying information messages to the user.
-   Changing values of child tasks based on changes to parent tasks.
-   Preventing users from accessing or modifying certain fields on a form.
-   Aborting the current database transaction. For example, if certain conditions are met, prevent the user from saving the record in the database.

Administrators can set field values, create information messages, and abort transactions without writing a script.

### Prevent recursive business rules

Avoid using current.update\(\) in a business rule script. The update\(\) method triggers business rules to run on the same table for insert and update operations, leading to a business rule calling itself over and over. Changes made in before business rules are automatically saved when all before business rules are complete, and after business rules are best used for updating related, not current, objects. When a recursive business rule is detected, the system stops it and logs the error in the system log. However, current.update\(\) causes system performance issues and is never necessary.

You can prevent recursive business rules by using the setWorkflow\(\) method with the false parameter. The combination of the update\(\) and setWorkflow\(\) methods is only recommended in special circumstances where the normal before and after guidelines mentioned above don't meet your requirements.

**Related topics**  


[Create a business rule](c_BusinessRules.md#)

## Business rules in scoped applications

Every business rule is assigned to either a private application scope or to the global scope.

The types of business rules you can create and how you can access those rules varies depending on the scope of the business rule and the scope of the table it runs on.

**Note:** The term global can refer to two different aspects of a business rule: the table it runs on and the scope it runs in. Business rules can either run on specific tables or be global. In addition, they can be in the global scope or in a private application scope.

### Business rules on specific tables

Most business rules run on a specific table, which is defined in the **Table** field. You can create business rules on tables in the same scope and on tables that allow configuration records from another application scope.

For tables that are in a different scope than the business rule record, the types of rules are limited.

-   You can create a rule where **When is async** with any of the following options:
    -   **Insert**, **Update**, and **Delete** database operations. You cannot select **Query**.
    -   **Set field values** actions and scripts \(the **Script** field\).
-   You can create a rule where When is before with any of the following options:
    -   **Insert**, **Update**, and **Delete** database operations. You cannot select **Query**.
    -   **Set field values** actions only. You cannot write scripts and you cannot abort the database transaction.
-   You cannot create any other types of business rules on tables in a different scope.

Business rules on specific tables cannot be accessed by other business rules or scripts.

### Global business rules

**Warning:** Consider using script includes instead of global business rules. Script includes load only on request while global business rules load on every page in the system.

Global business rules are business rules where the **Table** field is set to **Global**. Global business rules may be accessible on multiple tables and from other scripts, depending on their scope protection. For a global business rule, define the scope protection by setting the **Accessible from** field:

-   **This application scope only**: prevents applications in a different scope than the business rule from calling this business rule.
-   **All application scopes**: allows any application to call this business rule.

    **Note:** Global business rules do not support domain separation.


### Scripts in scoped business rules

When you write a script in a business rule, you can access:

-   Any script includes and global business rules in the same scope as the business rule.
-   Script includes and global business rules that allow applications in a different scope to call them. To call functions from another scope, you must specify the scope of the function.
-   For business rules in a unique scope, you can access the scoped system APIs only.

## Create a business rule

You can create any type of business rule to run when a record is displayed, inserted, updated, or deleted, or when a table is queried.

### About this task

**Note:** These instructions and examples provide general guidance for how to implement this functionality. For help with unique use cases, refer to the [Developer Community Forum](https://community.servicenow.com/community?id=community_forum&sys_id=75291a2ddbd897c068c1fb651f9619f3), where you can ask questions, interact with other developers, and search for existing solutions.

### Procedure

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
 For more information and examples, see [Example business rule scripts](c_BusinessRules.md#).

</td></tr><tr><td colspan="2">

Related list: Versions

</td></tr><tr><td>

Versions

</td><td>

Shows all versions of the business rule. Use this list to compare versions or to revert to a previous version.

</td></tr></tbody>
</table>4.  Click **Submit**.


If you run into issues with your business rule, see the [Business Rule FAQ \[KB0965707\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0965707) article in the Now Support Knowledge Base.

**Related topics**  


[How business rules work](c_BusinessRules.md#)

## Global variables in business rules

Predefined global variables are available for use in business rules.

Use the following predefined global variables to reference the system in a business rule script.

|Global variable|Description|
|---------------|-----------|
|*current*|Current state of the record being referenced. See "Prevent null pointer exceptions" below to check for nulls before using this variable.|
|*previous*|State of the referenced record prior to any updates made during the execution context, where the execution context begins with the first update or delete operation and ends after the script and any referenced business rules are executed. If multiple updates are made to the record within one execution context, *previous* will continue to hold the state of the record before the first update or delete operation. Available on update and delete operations only. Not available on async operations. See "Prevent null pointer exceptions" below to check for nulls before using this variable.|
|*g\_scratchpad*|Scratchpad object is available on display rules, and is used to pass information to the client to be accessed from client scripts.|
|*gs*|References to [GlideSystem](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) functions.|

The variables *current*, *previous*, and *g\_scratchpad* are global across all business rules that run for a transaction.

### Prevent null pointer exceptions

In some cases, there may not be a *current* or *previous* state for the record when a business rule runs, which means that the variables will be null. To check for null before using a variable, add the following code to your business rule:

```
if (current == null) // to prevent null pointer exceptions.
return; 
```

### Define variables

User-defined variables are globally scoped by default. If a new variable is declared in an order 100 business rule, the business rule that runs next at order 200 also has access to the variable. This may introduce unexpected behavior.

To prevent such unexpected behavior, always wrap your code in a function. This protects your variables from conflicting with system variables or global variables in other business rules that are not wrapped in a function. Additionally, variables such as *current* must be available when a function is invoked in order to be used.

The following script is vulnerable to conflicts with other code. If the variable *now\_GR* is used in other rules, the value of the variable may unexpectedly change.

```
var now_GR = new GlideRecord('incident');
now_GR.query(); 
while(now_GR.next()) {
 
   //do something
 
}
```

When this script is wrapped in a function, the variable is available only within the function and does not conflict with other functions using a variable named *now\_GR*.

```
myFunction();
 
function myFunction() { 
  var now_GR = new GlideRecord('incident');
  now_GR.query(); 
  while(now_GR.next()) { 
    //do something 
} }
```

## Use business rules and client scripts to control field values

Implement both business rules and client scripts for a field to enable users to set record values properly using both forms and lists, and to see immediate changes to the values in forms as edits are made.

The problem with using only a client script or a business rule to control updates to a field is that fields can be changed on either a form or a list. Client scripts and UI policies run on forms only \(client-side\) and do not apply to list editing. Allowing list editing with client scripts running on fields in a form can result in incorrect data being saved to the record. For systems in which client scripts or UI policies apply to forms, either disable list editing or create appropriate business rules or access control to control the setting of values in the list editor. A side effect of this is that security measures implemented in client scripts are easy to circumvent. The user only needs to edit the field in a list.

Business rules on a form are not dynamic, the user must update the record for the change to be seen. This makes using client scripts the preferred method for controlling field values on forms.

When using both a business rule and client script to control field values, the update behavior is the same across the system. This means that updated values are not different depending on whether a list of form is used to make the change. This means that the same functionality must be implemented twice, once in a client script and once in a business rule or access control.

### Example: Use a business rule to create email addresses during user record import

An organization has a client script that sets the email address for a user to `first.last@company.com`. Administrators do this so they can see the email address immediately when they enter the user's information. The administrator then performs a bulk import of users from a spreadsheet containing the users' first and last names. The expectation is that each user's email address will be set automatically, as they are when they edit the form. Since the client script runs only on the form \(the interface to the record\), it has no effect on data imported into the record from outside that interface, and no email addresses are created. To solve this problem, the administrator implements a business rule that runs when the import occurs and creates the email addresses.

### Example: Prevent list edit for a field that is not editable in the form

An organization wants to hide the **Priority** field on an incident form if the assignment group is **Development**. They create a UI policy on the incident form to do this, but their users can still see and edit the **Priority** field using the list editor. To rectify this, apply an access control to prevent read access to the **Priority** field when the assignment group is **Development**.

### Using NULL as a field value

The string NULL has a particular role in scripts and is a reserved word.

The reserved word is NULL in all capital letters. A field with the value **Null** or **null**, for example, is acceptable. Only use NULL to clear out a particular field.

Any NULL field values obtained from an import set data source are inserted into the staging table as empty field values. You should not use the term NULL as a field value in import set transform maps or anywhere in the **First name** or **Last name** fields. Also, do not use NULL in reference fields as the system interprets the value as a string containing the word NULL, not as a reserved word.

## Display business-rules

Display rules are processed when a user requests a record form.

The data is read from the database, display rules are executed, and the form is presented to the user. The current object is available and represents the record retrieved from the database. Any field changes are temporary since they are not yet submitted to the database. To the client, the form values appear to be the values from the database; there is no indication that the values were modified from a display rule. This is a similar concept to calculated fields.

The primary objective of display rules is to use a shared scratchpad object, *g\_scratchpad*, which is also sent to the client as part of the form. This can be useful when you need to build client scripts that require server data that is not typically part of the record being displayed. In most cases, this would require a client script making a call back to the server. If the data can be determined prior to the form being displayed, it is more efficient to provide the data to the client on the initial load. The form scratchpad object is an empty object by default, and used only to store name:value pairs of data.

To populate the form scratchpad with data from a display rule:

```
// From display business rule
g_scratchpad.someName = "someValue";
g_scratchpad.anotherName = "anotherValue";
 
// If you want the client to have access to record fields not being displayed on the form
g_scratchpad.created_by = current.sys_created_by; 
 
// These are simple examples, in most cases you will probably perform some other 
// queries to test or get data
```

To access the form scratchpad data from a client script:

```
// From client script 
if(g_scratchpad.someName == "someValue") { 
  //do something special 
}
```

## Task Active State Management business rule

This business rule determines whether the active field value needs to change based on changes to the **State** field.

The Task Active State Management business rule is executed when the **State** is changed for a task record. Its execution order is 50, and it runs before most other task business rules.

If the current task table has the **close\_states** attribute defined on its table, or if it is inherited from a higher-level table, then the rule determines whether the active field needs to change. This is done by comparing the previous and current state values.

-   If the state changes from an active state to an inactive state, the **Active** field is set to false.
-   If the state changes from an inactive state to an active state, the **Active** field is set to true, effectively re-activating or re-opening the task.

It is recommended that you leverage the **\(current.active.changesTo\(\[true/false\]\)** action in your business rule, as opposed to creating rules on each task table that mark tasks as inactive or active.

## Example business rule scripts

Find an example business rule script that helps you with a requirement of your organization.

**Note:** These instructions and examples provide general guidance for how to implement this functionality. For help with unique use cases, refer to the [Developer Community Forum](https://community.servicenow.com/community?id=community_forum&sys_id=75291a2ddbd897c068c1fb651f9619f3), where you can ask questions, interact with other developers, and search for existing solutions.

### Compare date fields in a business rule

It is possible to compare two date fields or two date and time fields in a business rule, and abort a record insert or update if they are not correct.

For example, you may want a start date to be before an end date. The following is an example script:

```
if ((!current.u_date1.nil()) && (!current.u_date2.nil())) { 
  var start = current.u_date1.getGlideObject().getNumericValue(); 
  var end = current.u_date2.getGlideObject().getNumericValue(); 
  if (start > end) {
    gs.addInfoMessage('start must be before end');
    current.u_date1.setError('start must be before end') ;
    current.setAbortAction(true);
 } }
```

This example has been tested in global scripts, and may need changes to work in scoped scripts. In addition to possibly needing API changes, security is more strict in scoped scripts.

As a good practice, make the business rule a before rule for insert and update actions. In the example script:

-   *u\_date1* and *u\_date2* are the names of the two date fields. Replace these names with your own field names.
-   The first line checks that both fields actually have a value.
-   The next two lines create variables that have the dates' numerical values.
-   The next two lines create different alert messages for the end user: one at the top of the form and one by the *u\_date1* field in the form.
-   The last line aborts the insert or update if the date fields are not correct.

Here is a more complex example of the above comparison. If you have more than one pair of start and end dates, you can use arrays as shown. Additionally, this script requires the input dates to be within a certain range, in this case, no fewer than 30 days in the past and no more than 365 days in the future.

```
// Enter all start and end date fields you wish to check, as well as the previous values 
// Make sure that you keep the placement in the sequence the same for all pairs 
var startDate = new Array(current.start_date,current.work_start); 
var prevStartDate = new Array(previous.start_date,previous.work_start); 
var endDate = new Array(current.end_date,current.work_end); 
var prevEndDate = new Array(previous.end_date,previous.work_end);

// The text string below is added to the front of ' start must be before end' 
var userAlert = new Array('Planned','Work');
 
// Set the number of Previous Days you want to check 
var pd = 30; 
// Set the number of Future Days you want to check 
var fd = 365;
 
// You shouldn't have to modify anything below this line
 
var nowdt = new GlideDateTime();
nowdt.setDisplayValue(gs.nowDateTime()); 
var nowMs = nowdt.getNumericValue(); 
var pdms = nowMs; 

// Subtract the product of previous days to get value in milliseconds
pdms -= pd * 24 * 60 * 60 * 1000; 
var fdms = nowMs; 

// Add the product of future days to get value in miliseconds
fdms += fd * 24 * 60 * 60 * 1000; 
var badDate = false;
 
 // Iterate through all start and end date / time fields 
for (x = 0; x < startDate.length; x ++) { 
  if ((!startDate[x].nil()) && (!endDate[x].nil())) { 
    var start = startDate[x].getGlideObject().getNumericValue(); 
    var end = endDate[x].getGlideObject().getNumericValue(); 
    if (start > end) {
      gs.addInfoMessage(userAlert[x] + ' start must be before end');
      startDate[x].setError(userAlert[x] + ' start must be before end');
      badDate = true; } 
    else if ((prevStartDate[x]) != (startDate[x])) { 
      if (start < pdms) {
         gs.addInfoMessage(userAlert[x] + ' start must be fewer than ' + pd + ' days ago');
         startDate[x].setError(userAlert[x] + ' start must be fewer than ' + pd  + ' days ago');
         badDate = true; } } 
    else if ((prevEndDate[x]) != (endDate[x])) { 
      if (end > fdms) {
         gs.addInfoMessage(userAlert[x] + ' end must be fewer than ' + fd + ' days ahead');
         endDate[x].setError(userAlert[x] + ' end must be fewer than ' + fd + ' days ahead');
         badDate  = true ; 
} } } } 
if (badDate == true ) {
  current. setAbortAction ( true ) ; }
```

### Parse XML payloads

Fields in XML format can be parsed with the system's getXMLText function.

Fields that get inserted into the database in XML format, such as the payload of an `ecc_event` row, can be parsed with the system's getXMLText function. The getXMLText function takes a string and an XPATH expression. For example:

```
var name = gs.getXMLText("<name>joe</name>", "//name");
```

returns the string 'joe'.

Assuming that the field "payload" contains XML, the function call might look like:

```
var name = gs.getXMLText(current.payload, "//name");
```

For information on XPATH, visit [w3schools](http://www.w3schools.com/xml/xpath_intro.asp).

### Abort a database action in a before business-rule

In a before business rule script, you can cancel or abort the current database action using the setAbortAction\(\) method.

For example, if the before business rule is executed during an insert action, and you have a condition in the script that calls `current.setAbortAction(true)`, the new record stored in current is not created in the database. The business rule continues to run after callingsetAbortAction\(\) and all subsequent business rules will execute normally. Calling this method only prevents the database action on current object from occurring.

You can use the isActionAborted\(\) method to determine if the current database action \(insert, update, delete\) is going to be aborted. isActionAborted\(\) is initialized for new threads and the next\(\) method explicitly sets its value to false.

**Note:** setAbortAction\(\) can only be executed from the same scope as the record whose action is being aborted. `current.setAbortAction` is not honored if executed in a business rule that is defined in a different scope.

### Determine the operation that triggered the business rule

You can write a script for a business rule that is triggered on more than one database action.

If you want the business rule script to dynamically branch depending on the action that triggered the event, you can use the operation\(\) function. For example:

```
if(current.operation() == "update") {
  current.updates ++; } 
  if(current.operation() == "insert") {
    current.updates = 0; }
```

### Use an OR condition in a business rule

An **OR** condition can be added to any query part within a business rule.

An **OR** condition can be added to any query part within a business rule with the addOrCondition\(\) method. The example below shows a query for finding all the incidents that have either a 1 or a 2 priority. The first addQuery\(\) condition is defined as a variable and is used in the **OR** condition.

```
var inc = new GlideRecord('incident'); 
var qc = inc.addQuery('priority','1'); 
qc.addOrCondition('priority','2');
inc.query(); 
while(inc.next()) { 
  // processing for the incident goes here 
}
```

The following script is a more complex example, using two query condition variables doing the equivalent of `(priority = 1 OR priority = 2) AND (impact = 2 OR impact = 3)`. The results of the **OR** condition are run with two variables, *qc1* and *qc2*. This allows you to manipulate the query condition object later in the script, such as inside an `IF` condition or `WHILE` loop.

```
var inc = new GlideRecord('incident'); 
var qc1 = inc.addQuery('priority','1');
qc1.addOrCondition('priority','2'); 
var qc2 = inc.addQuery('impact','2'); 
qc2.addOrCondition('impact','3'); 
inc.query(); 
while(inc.next()) { 
  // processing for the incident goes here  
}
```

### Reference a Glide list from a business rule

A field defined as a glide list is an array of values stored in a single field.

Here are some examples of how to process a glide\_list field when writing business rules. Generally a glide\_list field contains a list of reference values to other tables.

#### Examples

For example, the **Watch list** field within tasks is a glide\_list containing references to user records.

The code below shows how to reference the field.

```
// list will contain a series of reference (sys_id) values separated by a comma
// array will be a javascript array of reference values
var list = current.watch_list.toString();
var array = list.split(",");
for (var i=0; i < array.length; i++) {
   gs.print("Reference value is: " + array[i]);
}
```

Output:

```
*** Script: Reference value is: 62826bf03710200044e0bfc8bcbe5df1
*** Script: Reference value is: c2826bf03710200044e0bfc8bcbe5d45
*** Script: Reference value is: 5f74e421c0a8010e01ec0d74a7ee2cc6
*** Script: Reference value is: 06826bf03710200044e0bfc8bcbe5d57
```

You can also get the display values associated with the reference values by using the getDisplayValue\(\) method as shown below.

```
// list will contain a series of display values separated by a comma
// array will be a javascript array of display values
var list = current.watch_list.getDisplayValue();
var array = list.split(",");
for (var i=0; i < array.length; i++) {
   gs.print("Display value is: " + array[i]);
}
```

Output:

```
*** Script: Display value is: Abel Tuter
*** Script: Display value is:  Ashley Leonesio
*** Script: Display value is:  Charles Beckley
*** Script: Display value is:  Cherie Fuhri
```

### Use indexOf\("searchString"\) to find a string in a Glide list

Use indexOf\("**searchString**"\) to return the location of the string passed into the method if the glide list field, such as a Watch list, has at least one value in it.

If the field is empty, it returns `undefined`. To avoid returning an undefined value, do any of the following:

-   Force the field to a string, such as: watch\_list.toString\(\).indexOf\("**searchString**"\)
-   Check for an empty Glide list field with a condition before using indexOf\(\), such as: if \(watch\_list.nil\(\) \|\| watch\_list.indexOf\("**searchString**"\) == -1\)

### Lock user accounts

You can lock user accounts if the user is not active.

The following business rule script locks user accounts if the user is not active in the LDAP directory or the user does not have self-service, itil, or admin access to the instance.

```
// Lock accounts if bcNetIDStatus != active in LDAP and user does not  
// have self-service, itil or admin role 
var rls = current.accumulated_roles.toString(); 
if(current.u_bcnetidstatus == 'active' && (rls.indexOf(',itil,') > 0 || 
  rls.indexOf(',admin,') > 0 || 
  rls.indexOf(',ess,') > 0 )) { 
  current.locked_out = false; } 
else { 
  current.locked_out = true; } 

var now_GR = new GlideRecord("sys_user"); 
now_GR.query(); 
while(now_GR.next()) { 
  now_GR.update(); 
  gs.info("updating " + gr.getDisplayValue()); 
}
```

### Default before-query business rule

You can use a query business rule that executes before a database query is made.

Use this query business rule to prevent users from accessing certain records. Consider the following example from a default business rule that limits access to incident records.

-   Name: incident query
-   Table: Incident
-   When: before, query
-   Script:

```
if(!gs.hasRole("itil") && gs.isInteractive()) { 
  var u = gs.getUserID(); 
  var qc = current.addQuery("caller_id",u).addOrCondition("opened_by",u).addOrCondition("watch_list","CONTAINS",u);
  gs.print("query restricted to user: " + u); }
```

This example prevents users from accessing incident records unless they have the itil role, or are listed in the **Caller** or **Opened by** field. So, for example, when self-service users open a list of incidents, they can only see the incidents they submitted.

**Note:** You can also use access controls to restrict the records that users can see.


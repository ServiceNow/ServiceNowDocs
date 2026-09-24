---
title: Example business rule scripts
description: Find an example business rule script that helps you with a requirement of your organization.It is possible to compare two date fields or two date and time fields in a business rule, and abort a record insert or update if they are not correct.Fields in XML format can be parsed with the system's getXMLText function.In a before business rule script, you can cancel or abort the current database action using the setAbortAction\(\) method.You can write a script for a business rule that is triggered on more than one database action.An OR condition can be added to any query part within a business rule.A field defined as a glide list is an array of values stored in a single field.Use indexOf\("searchString"\) to return the location of the string passed into the method if the glide list field, such as a Watch list, has at least one value in it.You can lock user accounts if the user is not active.You can use a query business rule that executes before a database query is made.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/business-rule-examples.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Classic Business rules, Build workflows]
---

# Example business rule scripts

Find an example business rule script that helps you with a requirement of your organization.

**Note:** These instructions and examples provide general guidance for how to implement this functionality. For help with unique use cases, refer to the [Developer Community Forum](https://community.servicenow.com/community?id=community_forum&sys_id=75291a2ddbd897c068c1fb651f9619f3), where you can ask questions, interact with other developers, and search for existing solutions.

**Parent Topic:**[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRules.md)

## Compare date fields in a business rule

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

## Parse XML payloads

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

## Abort a database action in a before business-rule

In a before business rule script, you can cancel or abort the current database action using the setAbortAction\(\) method.

For example, if the before business rule is executed during an insert action, and you have a condition in the script that calls `current.setAbortAction(true)`, the new record stored in current is not created in the database. The business rule continues to run after callingsetAbortAction\(\) and all subsequent business rules will execute normally. Calling this method only prevents the database action on current object from occurring.

You can use the isActionAborted\(\) method to determine if the current database action \(insert, update, delete\) is going to be aborted. isActionAborted\(\) is initialized for new threads and the next\(\) method explicitly sets its value to false.

**Note:** setAbortAction\(\) can only be executed from the same scope as the record whose action is being aborted. `current.setAbortAction` is not honored if executed in a business rule that is defined in a different scope.

## Determine the operation that triggered the business rule

You can write a script for a business rule that is triggered on more than one database action.

If you want the business rule script to dynamically branch depending on the action that triggered the event, you can use the operation\(\) function. For example:

```
if(current.operation() == "update") {
  current.updates ++; } 
  if(current.operation() == "insert") {
    current.updates = 0; }
```

## Use an OR condition in a business rule

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

## Reference a Glide list from a business rule

A field defined as a glide list is an array of values stored in a single field.

Here are some examples of how to process a glide\_list field when writing business rules. Generally a glide\_list field contains a list of reference values to other tables.

### Examples

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

## Use indexOf\("searchString"\) to find a string in a Glide list

Use indexOf\("**searchString**"\) to return the location of the string passed into the method if the glide list field, such as a Watch list, has at least one value in it.

If the field is empty, it returns `undefined`. To avoid returning an undefined value, do any of the following:

-   Force the field to a string, such as: watch\_list.toString\(\).indexOf\("**searchString**"\)
-   Check for an empty Glide list field with a condition before using indexOf\(\), such as: if \(watch\_list.nil\(\) \|\| watch\_list.indexOf\("**searchString**"\) == -1\)

## Lock user accounts

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

## Default before-query business rule

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


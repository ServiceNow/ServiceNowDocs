---
title: Business rule use cases
description: Use cases for business rules include aborting a database action and restricting record access.You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.You can use a query business rule that executes before the database query to prevent users from accessing certain records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/useful-business-rules.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Example scripts, Scripting, API implementation, API implementation and reference]
---

# Business rule use cases

Use cases for business rules include aborting a database action and restricting record access.

**Parent Topic:**[Example scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/usefulScripts.md)

## Abort a database action

You can use a before business rule script to cancel or abort the current database action using the current.setAbortAction\(true\) method.

If the before business rule is executed during an insert action, and a condition in the script calls current.setAbortAction\(true\), the new record stored in current is not created in the database.

**Related topics**  


[GlideRecord - setAbortAction\(Boolean b\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideRecordAPI.md)

[Scoped GlideRecord - setAbortAction\(Boolean b\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md)

## Restricting record access

You can use a query business rule that executes before the database query to prevent users from accessing certain records.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

Consider the following example from a default business rule that limits access to incident records.

|Name|Table|When|
|----|-----|----|
|incident query|Incident|before, query|

### Restricting record access

In the following example, users are restricted from accessing incident records unless they have the itil role and are listed in the Caller or Opened by field. When self-service users open a list of incidents, they can only see the incidents they submitted.

```javascript
if (!gs.hasRole("itil")&& gs.isInteractive()) {
  var u = gs.getUserID();
  var qc = current.addQuery("caller_id", u).addOrCondition("opened_by", u).addOrCondition("watch_list","CONTAINS", u);
  gs.print("query restricted to user: " + u);}
```

**Note:** You can also use access controls to restrict the records that users can see. For information, see [Access Control Lists \(ACLs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/access-control-rules.md).

### Schedule script for weekdays

Type: Business Rules/Client Scripts.

This script schedules the script for weekdays. Insert any script where it says "Your Script Here."

```javascript
var go ='false';
var now =new Date(); 
 
// Correct time zone, which is by default GMT -7 
now.setHours(now.getHours()+8);
var day = now.getDay(); 
 
// No go on Saturday or Sunday 
if(day !=0&& day !=6){
 
// (your script here)
 
}
```

### Set date field according to current date

This script sets a date field depending on the current day of the week. In this example, if the day is Monday through Wednesday, it sets the date to this coming Monday; otherwise it sets the date field to next Monday.

```javascript
function setCabDate(){
var today = new Date();
var thisDay = today.getDay();

//returns 0 for Sunday, 1 for Monday, through 6 for Saturday.
var thisMon = new GlideDateTime();
thisMon.setDisplayValue(gs.beginningOfThisWeek());
var nextMon = thisMon.getNumericValue();
nextMon +=(1000*60*60*24*7);
 
if((thisDay <4)&&(thisDay >0))
  //if today is Mon thru Wed (thisDay = 1, 2, or 3), set cab to this coming Monday.
  current.u_req_cab_rev_date.setDateNumericValue(thisMon.getNumericValue());
else if((thisDay >=4)||(thisDay ==0))
  //if today is Thurs thru Sun (thisDay = 4, 5, 6, or 0), set cab to next Monday.
  current.u_req_cab_rev_date.setDateNumericValue(nextMon);
}
```

To validate the input of all date/time fields, you can use the following in a validation script \(**System Definition** &gt; **Validation Scripts**\). Because the date/time format is hard coded in this script, it must match your instance's date/time format. If your instance's date/time format changes, you must update your validation script.

Set the validation script's type to Date/Time. Then, with this validation script, if a user enters an incorrect format in a date/time field, they receive an error message.

```javascript
function validate(value){
// empty fields are still valid dates 
if(!value) 
    return true; 
 
// We "should" have the global date format defined always defined. But there's always that edge case. 
if(typeof g_user_date_time_format !=='undefined')
    return isDate(value, g_user_date_time_format); 
 
// if we don't have that defined, we can always try guessing 
return parseDate(value)!==null;}
```

For more information, see [Validation script use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_ValidateDateAndTime.md).


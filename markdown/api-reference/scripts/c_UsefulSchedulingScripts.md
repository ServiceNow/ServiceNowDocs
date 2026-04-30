---
title: Scheduling script use cases
description: A business rule script specifies the actions that the business rule takes. Scripts commonly include predefined global variables to reference items in your system, such as the current record. Global variables are available to all business rules.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Useful scripts, Scripting, API implementation, API implementation and reference]
---

# Scheduling script use cases

A business rule script specifies the actions that the business rule takes. Scripts commonly include predefined global variables to reference items in your system, such as the current record. Global variables are available to all business rules.

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

## Calculate duration given a schedule

Type: Before update/insert business rule.

Description: A business duration calculates the open to close duration on an incident based on the particular [Creating and using schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). If there is no schedule specified, the script will simply use the first schedule returned by the query.

Script example:

The example below sets the resolved duration when the incident state moves to resolved.

```
var gr_rec = new GlideRecord('incident');
gr_rec.get('ed92e8d173d023002728660c4cf6a7bc');
if (gr_rec.incident_state == 6) {
var dur = calcDurationSchedule(gr_rec.opened_at, gr_rec.sys_updated_on);
}
 
function calcDurationSchedule(start, end){ 
  // Get the user   
  var usr = new GlideRecord('sys_user');
  usr.get(gs.getUserID());
  // Create schedule - pass in the sys_id of your standard work day schedule and pass in the users timezone
  var sched = new GlideSchedule('08fcd0830a0a0b2600079f56b1adb9ae',usr.time_zone);
  // Get duration based on schedule/timezone 
  return(sched.duration(start.getGlideObject(), end.getGlideObject()));
}
```

## Check upcoming termination dates

Type: Scheduled script.

Description: This script checks nightly for termination dates on contracts coming up in 90, 50, or 10 days \(depending on the contract duration field\).

Script example:

```
function contractNoticeDue(){
  var now_GR = new GlideRecord("contract");
  now_GR.addQuery("u_contract_status","Active");
  now_GR.query();
  while(now_GR.next()){
    if((now_GR.u_termination_date<= gs.daysAgo(-90))&&(now_GR.u_contract_duration=="Long")){
      now_GR.u_contract_status="In review";}
    elseif((now_GR.u_termination_date<= gs.daysAgo(-50))&&(now_GR.u_contract_duration=="Medium")){
      now_GR.u_contract_status="In review";}
    elseif((now_GR.u_termination_date <= gs.daysAgo(-10))&&(now_GR.u_contract_duration=="Short")){
      now_GR.u_contract_status="In review";}
    now_GR.update();
  }
}
```

Use scripts in business rules to accomplish common tasks such as:

-   Comparing two date fields.
-   Parsing XML payloads.
-   Aborting a database action in a business rule.

With scripts, you can also:

-   Specify the operation that triggers the business rule.
-   Use the scratchpad with display business rules to change form values just before a user loads the form.
-   Use the OR condition like you would in a condition builder.

You can also utilize the system's scripting functionality available for server-side scripts.

You can use options on the Business Rules form to build conditions, set field values, and display alert messages without needing to write a script.

**Parent Topic:**[Useful scripts](usefulScripts.md)


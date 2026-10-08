---
title: Server-side script use cases
description: Use cases for server-side scripts include logging output, getting user objects, and modifying date/time values.A catalog item has been requested, and the attached workflow contains a run script activity that populates a value in the scratchpad. From a business rule running on the requested item, you want to retrieve or set scratchpad values.Assign a service catalog item to the database group if it uses a delivery plan that has a catalog task that is assigned to the desktop group.Often you may need to provide users with a way to specify when a task or process is due. Using the DurationCalculator script include, you can calculate the due date using either a simple duration or relative duration.How much work is required to complete a task can be expressed as a "relative duration".This business rule and script example demonstrate how to calculate a simple duration.An example of a relative duration calculation script.You can implement a relative duration by creating the cmn\_relative\_duration table and the DurationCalculator script include.The cmn\_relative\_duration table supports the definition of a due date as either a duration of time or a relative duration.The GlideAggregate class is an extension of GlideRecord and allows database aggregation \(COUNT, SUM, MIN, MAX, AVG\) queries to be done. This can be helpful in creating customized reports or in calculations for calculated fields.GlideRecordSecure is a class inherited from GlideRecord that performs the same functions as GlideRecord, and also enforces ACLs.In a business rule or other server script, the gs.getUser\(\) method returns a user object. The user object is an internal representation of the currently logged in user and provides information about the user and various utility functions.GSLog is a script include that simplifies script logging and debugging by implementing levels of log output, selectable by per-caller identified sys\_properties values.The GlideDateTime class provides methods for performing operations on GlideDateTime objects, such as instantiating GlideDateTime objects or working with glide\_date\_time fields.The GlideDate and GlideDateTime APIs are used to manipulate date and time values.Examples of JavaScript that can be used to set the value of a duration field.You can specify a date format with a sequence of specific date and time pattern strings. A pattern string consists of one or more uppercase and lowercase letters from A to Z. Any text within quotation marks is ignored and is instead copied into the date output.You can use custom queues for applications that create a large volume of events or events that take a long time to process. This task shows how to create a custom queue, its monitoring process, and use a script to send events to the queue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/useful-server-side-scripts.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 31
breadcrumb: [Example scripts, Scripting, API implementation, API implementation and reference]
---

# Server-side script use cases

Use cases for server-side scripts include logging output, getting user objects, and modifying date/time values.

**Parent Topic:**[Example scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/usefulScripts.md)

## Accessing the workflow scratchpad from business rules

A catalog item has been requested, and the attached workflow contains a run script activity that populates a value in the scratchpad. From a business rule running on the requested item, you want to retrieve or set scratchpad values.

### Prerequisites

Role required: admin.

Name: Access Workflow Scratchpad from Business Rules.

Type: Business Rule.

Table: sc\_req\_item \(Requested Item\).

Description: A catalog item has been requested, the attached workflow contains a run script activity that populates a value in the scratchpad. From a business rule running on the requested item, you want to retrieve or set scratchpad values.

Parameters: n/a.

Script:

```javascript
//the run script activity sets a value in the scratchpad
workflow.scratchpad.important_msg = "scratch me";
 
//get the workflow script include helper 
var workflow = new Workflow();
 
//get the requested items workflow context 
//this will get all contexts so you will need to get the proper one if you have multiple workflows for a record 
var context = workflow.getContexts(current); 
//make sure we have a valid context 
if (context.next()) { 
  //get a value from the scratchpad 
  var msg = context.scratchpad.important_msg; 
  //msg now equals "scratch me", that was set in the run script activity
 
  //add or modify a scratchpad value
  context.scratchpad.status = "completed"; 
  //we need to save the context record to save the scratchpad
  context.update(); 
}
```

## Assign a catalog item to a group based on a delivery plan task

Assign a service catalog item to the database group if it uses a delivery plan that has a catalog task that is assigned to the desktop group.

**Prerequisites**

Role required: admin

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

Name: Assign Catalog Item to Group Based on Delivery Plan Task.

Type: Assignment Rule.

Description: This assignment rule assigns a service catalog item to the database group if it uses a delivery plan that has a catalog task assigned to the desktop group.

**Script:**

```javascript
//Return catalog items that have no group but do have a delivery plan assigned var ri  = new GlideRecord ( "sc_cat_item" ) ;
ri.addQuery("group", "=", null);
ri.addQuery("delivery_plan", "!=", null);
ri.query(); 
while(ri.next()) {
    gs.log("Found an item"); 
    //Return tasks that point to the same delivery plan as the above item 
    var dptask = new GlideRecord("sc_cat_item_delivery_task");
    dptask.addQuery("delivery_plan", "=", ri. delivery_plan);
    dptask.query(); 
    while(dptask.next()) {
        gs.log("Found a task");
        var gp = dptask.group.getDisplayValue();
        gs.log(gp); 
        //If the task is assigned to desktop, assign the item's group to desktop
        if (dptask.group.getDisplayValue() == "Desktop") {
            ri.group.setDisplayValue("Desktop");
            gs.log("updating " + ri.getDisplayValue());
            ri.update(); 
            break; } } }
```

## Calculating durations

Often you may need to provide users with a way to specify when a task or process is due. Using the DurationCalculator script include, you can calculate the due date using either a simple duration or relative duration.

Typically, setting a due date requires that you calculate work time rather than the total time. Only the part of the day when work is performed is considered when determining the due date. For example, a task is due in 10 hours, but is restricted to a business day schedule. If the work starts at 10am on Monday, it is due on Tuesday at 12pm: 10am-5pm on Monday \(7 hours\) + 8am-12pm on Tuesday \(4 hours\).

For information on schedules, which you can use as inputs to DurationCalculator methods, see [Creating and using schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_UseSchedules.md).

This script demonstrates how to use DurationCalculator to compute a due date.

```javascript
/**
 * Demonstrate the use of DurationCalculator to compute a due date.
 * 
 * You must have a start date and a duration. Then you can compute a
 * due date using the constraints of a schedule.
 */
 
gs.include('DurationCalculator');
executeSample();
 
/**
 * Function to house the sample script.
 */function executeSample(){
 
    // First we need a DurationCalculator 
    object.var dc =new DurationCalculator();
 
    // --------------- No schedule examples ------------------
 
    // Simple computation of a due date without using a schedule. Seconds// are added to the start date continuously to get to a due date.
    dc.setStartDateTime("5/1/2012");if(!dc.calcDuration(2*24*3600)){// 2 days
    	gs.log("*** Error calculating duration");return;}
    gs.log("calcDuration no schedule: "+ dc.getEndDateTime());// "2012-05-03 00:00:00" two days later
 
    // Start in the middle of the night (2:00 am) and compute a due date 1 hour in the future// Without a schedule this yields 3:00 am.
    dc.setStartDateTime("5/3/2012 02:00:00");if(!dc.calcDuration(3600)){
        gs.log("*** Error calculating duration");return;}
    gs.log("Middle of night + 1 hour (no schedule): "+ dc.getEndDateTime());// No scheduled start date, just add 1 hour
 
 
    // -------------- Add a schedule to the date calculator ---------------------
    addSchedule(dc);
 
    // Start in the middle of the night and compute a due date 1 hour in the future.// Since we start at 2:00 am the computation adds the 1 hour from the start// of the day, 8:00am to get to 9:00am
    dc.setStartDateTime("5/3/2012 02:00:00");if(!dc.calcDuration(3600)){// 
        gs.log("*** Error calculating duration");return;}
    gs.log("Middle of night + 1 hour (with 8-5 schedule): "+ dc.getEndDateTime());// 9:00 am
 
    // Start in the afternoon and add hours beyond quiting time. Our schedule says the work day// ends at 5:00pm, if the duration extends beyond that, we roll over to the next work day.// In this example we are adding 4 hours to 3:00pm which gives us 10:00 am the next day.
    dc.setStartDateTime("5/3/2012 15:00:00");if(!dc.calcDuration(4*3600)){// 
        gs.log("*** Error calculating duration");return;}
    gs.log("Afternoon + 4 hour (with 8-5 schedule): "+ dc.getEndDateTime());// 10:00 am.
 
    // This is a demo of adding 2 hours repeatedly and examine the result. This// is a good way to visualize the result of a due date calculation.
    dc.setStartDateTime("5/3/2012 15:00:00");// for(var i=2; i<24; i+=1){if(!dc.calcDuration(i*3600)){// 
            gs.log("*** Error calculating duration");return;}
        gs.log("add "+ i +" hours gives due date: "+ dc.getEndDateTime());}
 
    // Setting the timezone causes the schedule to be interpreted in the specified timezone.// Run the same code as above with different timezone. Note that the 8 to 5 workday is// offset by the two hours as specified in our timezone.
    dc.setTimeZone("GMT-2");
    dc.setStartDateTime("5/3/2012 15:00:00");for(var i=2; i<24; i+=1){if(!dc.calcDuration(i*3600)){// 
            gs.log("*** Error calculating duration");return;}
        gs.log("add "+ i +" hours gives due date (GMT-2): "+ dc.getEndDateTime());}}
 
/** 
 * Add a specific schedule to the DurationCalculator object.
 *  
 * @param durationCalculator An instance of DurationCalculator
 */function addSchedule(durationCalculator){//  Load the "8-5 weekdays excluding holidays" schedule into our duration calculator.var scheduleName ="8-5 weekdays excluding holidays";var grSched =new GlideRecord('cmn_schedule');
    grSched.addQuery('name', scheduleName);
    grSched.query();if(!grSched.next()){
        gs.log('*** Could not find schedule "'+ scheduleName +'"');return;}
    durationCalculator.setSchedule(grSched.getUniqueValue(),"GMT");}
```

### Simple duration vs relative duration

How much work is required to complete a task can be expressed as a "relative duration".

Relative duration determines the expected due date and time relative to the starting time. Examples of relative durations include "Next business day by 4pm", or "2 business days by 10:30am".

To calculate a relative duration, the calendar and time zone must be considered to determine what "next business day" means since it is the calendar that defines which days are valid work days and the time zone will affect the result as well. As an example, consider "Next business day by 4pm":

-   If it is Monday at 12pm: Next business day by 4pm =&gt; Tuesday at 4pm
-   If it is Friday at 2pm: Next business day by 4pm =&gt; the following Monday at 4pm

**Note:** Next business day is often defined by a starting day and time. For example, "next business day at 4pm if before 2pm" indicates that if the current time is after 2pm on a business day, then "Next business day" really means 2 business days since today does not count.

For more information on relative durations, see [Define a relative duration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_DefineARelativeDuration.md).

#### Calculating a simple duration

This business rule and script example demonstrate how to calculate a simple duration.

```javascript
var dur =new DurationCalculator();
dur.setSchedule(current.schedule);
dur.setStartDateTime("");
 
if(current.duration_type==""){
         dur.calcDuration(current.duration.getGlideObject().getNumericValue()/1000);}else{
         dur.calcRelativeDuration(current.duration_type);}
 
    current.end_date_time= dur.getEndDateTime();
    current.work_seconds= dur.getSeconds();
```

This script demonstrates how to use DurationCalculator to calculate a simple duration.

```javascript
/**
 * Sample script demonstrating use of DurationCalculator to compute simple durations
 * 
 */
 
gs.include('DurationCalculator');
executeSample();
 
/**
 * Function to house the sample script.
 */
function executeSample(){
 
    // First we need a DurationCalculator object.
    var dc =new DurationCalculator();
 
    // Compute a simple duration without any schedule. The arguments
    // can also be of type GlideDateTime, such as fields from a GlideRecord.
    var dur = dc.calcScheduleDuration("5/1/2012","5/2/2012");
    gs.log("calcScheduleDuration no schedule: "+ dur);
    // 86400 seconds (24 hours)
 
    // The above sample is useful in limited cases. We almost always want to 
    // use some schedule in a duration computation, let's load a schedule.
    addSchedule(dc);
 
    // Compute a duration using the schedule. The schedule
    // specifies a nine hour work day. The output of this is 32400 seconds, or
    // a nine hour span.
    dur = dc.calcScheduleDuration("5/23/2012 12:00","5/24/2012 12:00");
    gs.log("calcScheduleDuration with schedule: "+ dur);
    // 32400 seconds (9 hours)
 
    // Compute a duration that spans a weekend and holiday. Even though this
    // spans three days, it only spans 9 work hours based on the schedule.
    dur = dc.calcScheduleDuration("5/25/2012 12:00","5/29/2012 12:00");
    gs.log("calcScheduleDuration with schedule spaning holiday: "+ dur);
    // 32400 seconds (9 hours)
 
    // Use the current date time in a calculation. The output of this is
    // dependent on when you run it.
    var now =new Date();
    dur = dc.calcScheduleDuration("5/15/2012",new GlideDateTime());
    gs.log("calcScheduleDuration with schedule to now: "+ dur);
    // Different on every run.}
 
/** 
 * Add a specific schedule to the DurationCalculator object.
 *  
 * @param durationCalculator An instance of DurationCalculator
 */
function addSchedule(durationCalculator){
   //  Load the "8-5 weekdays excluding holidays" schedule into our duration calculator.
   var scheduleName ="8-5 weekdays excluding holidays";
   var grSched =new GlideRecord('cmn_schedule');
   grSched.addQuery('name', scheduleName);
   grSched.query();if(!grSched.next()){
        gs.log('*** Could not find schedule "'+ scheduleName +'"');
        return;}
    durationCalculator.setSchedule(grSched.getUniqueValue());}
```

#### Calculating a relative duration

An example of a relative duration calculation script.

This script calculates the relative duration for "Next day at 4pm if after 10am":

```javascript
// Next day at 4pm if before 10am
var days =1;
if(calculator.isAfter(calculator.startDateTime,"10:00:00")) 
      days++;
 
calculator.calcRelativeDueDate(calculator.startDateTime, days,"16:00:00");
```

This script demonstrates how to use DurationCalculator to calculate a relative duration.

```javascript
/**
 * Sample use of relative duration calculation.
 * 
 */
 
gs.include('DurationCalculator');
executeSample();
 
/**
 * Function to house the sample script.
 */
function executeSample(){
 
    // First we need a DurationCalculator object. We will also use
    // the out-of-box relative duration "2 bus days by 4pm"
    var dc =new DurationCalculator();
    var relDur ="3bf802c20a0a0b52008e2859cd8abcf2";
    // 2 bus days by 4pm if before 10am
    addSchedule(dc);
 
    // Since our start date is before 10:00am our result is two days from
    // now at 4:00pm.
    dc.setStartDateTime("5/1/2012 09:00:00");
    if(!dc.calcRelativeDuration(relDur)){
        gs.log("*** calcRelativeDuration failed");
        return;}
    gs.log("Two days later 4:00pm: "+ dc.getEndDateTime());
 
    // Since our start date is after 10:00am our result is three days from
    // now at 4:00pm.
    dc.setStartDateTime("5/1/2012 11:00:00");
    if(!dc.calcRelativeDuration(relDur)){
        gs.log("*** calcRelativeDuration failed");
        return;}
    gs.log("Three days later 4:00pm: "+ dc.getEndDateTime());}
 
/** 
 * Add a specific schedule to the DurationCalculator object.
 *  
 * @param durationCalculator An instance of DurationCalculator
 */
function addSchedule(durationCalculator){
  //  Load the "8-5 weekdays excluding holidays" schedule into our duration calculator.
  var scheduleName ="8-5 weekdays excluding holidays";
  var grSched =new GlideRecord('cmn_schedule');
  grSched.addQuery('name', scheduleName);
  grSched.query();
  if(!grSched.next()){
        gs.log('*** Could not find schedule "'+ scheduleName +'"');
        return;}
  durationCalculator.setSchedule(grSched.getUniqueValue(),"GMT");}
```

### How to implement a relative duration

You can implement a relative duration by creating the cmn\_relative\_duration table and the DurationCalculator script include.

#### Before you begin

Role required: admin

#### Procedure

1.  Create the cmn\_relative\_duration table.

2.  Create the DurationCalculator script include.

3.  Create a sample relative duration entry \(for example, "Next business day by 4pm"\).

4.  Add the needed fields to SLA tables to support relative durations.

5.  Modify duration calculation for SLAs.

6.  Modify SLA Percentage timer calculation for SLAs \(this must use work\_seconds\).

7.  Add schedule fields to the Workflow: Schedule and Timezone \(selected based on the field from workflow table\).

8.  Add duration support fields to the Workflow Task activity.

9.  Implement duration calculation script for the task activity.


#### The relative duration table and the DurationCalculator methods

The cmn\_relative\_duration table supports the definition of a due date as either a duration of time or a relative duration.

This table consists of two fields: "name" and "script." The "script" field contains the relative duration calculation script. This script includes the "calculator" variable, which is used to calculate the due date.

The DurationCalculator script include can be used to perform the duration calculations. The following are methods that are available in this script include.

<table id="table_vbs_swt_1q"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

setSchedule\(String schedID, \[String timezone\]\)

</td><td>

Sets the schedule and time zone to be used for calculating the due date.

</td></tr><tr><td>

setStartDateTime\(GlideDateTime start\)

</td><td>

Sets the start time for the duration calculations. If 'start' is blank, uses current date/time.

</td></tr><tr><td>

calcDuration\(int seconds\)

</td><td>

Calculates the end date and time. Upon completion the this.endDateTime and this.seconds properties will be set to indicate the results of the calculation.

</td></tr><tr><td>

calcRelativeDuration\(String relativeDurationID\)

</td><td>

Calculates the duration using the specified relative duration script. Upon completion the this.endDateTime and this.seconds properties will be set to indicate the results of the calculation.

</td></tr><tr><td>

getEndDateTime\(\)

</td><td>

Gets the this.endDateTime property that was set by calcDuration/calcRelativeDuration indicating the end date and time for the duration.

</td></tr><tr><td>

getSeconds\(\)

</td><td>

Gets the this.seconds property that was set by calcDuration/calcRelativeDuration indicating the total number of seconds of work to be performed for the duration.**Note:** This is the total work time, not the total time between start and end times and may be used to determine percentages of the work time

</td></tr><tr><td>

getTotalSeconds\(\)

</td><td>

Gets the this.totalSeconds property that was set by calcDuration/calcRelativeDuration indicating the total number of seconds between the start and end times of the duration.

</td></tr></tbody>
</table>The following functions are used in relative duration scripts:

|Function|Description|
|--------|-----------|
|boolean isAfter\(GlideDateTime dt, String time\)|Is 'time' of day after the time of day specified by 'dt'? dt, if blank, uses current date/time. time is in "hh:mm:ss" in 24-hour format.|
|calcRelativeDueDate\(GlideDateTime start, int days, String endTime\)|Calculates the due date starting at 'start' and adding 'days' using the schedule and time zone. When we find the day that the work is due on, set the time to 'endTime' of that day. Upon completion, this.endDateTime and this.seconds properties will be set to indicate the results of the calculation. If endTime is blank, use end of the ending work day.|

## Creating database aggregation queries with GlideAggregate

The GlideAggregate class is an extension of GlideRecord and allows database aggregation \(COUNT, SUM, MIN, MAX, AVG\) queries to be done. This can be helpful in creating customized reports or in calculations for calculated fields.

For additional information, refer to [GlideAggregate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideAggregateScopedAPI.md) API.

Here is an example that simply gets a count of the number of records in a table:

```javascript
var count = new GlideAggregate('incident');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if(count.next()) 
   incidents = count.getAggregate('COUNT');
```

There is no query associated with the preceding example. If you want to get a count of the incidents that were open, simply add a query as is done with GlideRecord. Here is an example to get a count of the number of active incidents.

```javascript
var count = new GlideAggregate('incident');
count.addQuery('active','true');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if(count.next()) 
   incidents = count.getAggregate('COUNT');
```

To get a count of all the open incidents by category the code is:

```javascript
var count = new GlideAggregate('incident');
count.addQuery('active','true');
count.addAggregate('COUNT','category');
count.query();
while(count.next()){
  var category = count.category;
  var categoryCount = count.getAggregate('COUNT','category');
  gs.log("The are currently "+ categoryCount +" incidents with a category of "+ category);}
```

The output is:

```javascript
 *** Script: The are currently 1.0 incidents with a category of Data  
       *** Script: The are currently 11.0 incidents with a category of Enhancement
       *** Script: The are currently 1.0 incidents with a category of Implementation
       *** Script: The are currently 197.0 incidents with a category of inquiry
       *** Script: The are currently 13.0 incidents with a category of Issue
       *** Script: The are currently 1.0 incidents with a category of 
       *** Script: The are currently 47.0 incidents with a category of request
```

The following is an example that uses multiple aggregations to see how many times records have been modified using the *MIN*, *MAX*, and *AVG* values.

```javascript
var count = new GlideAggregate('incident');
count.addAggregate('MIN','sys_mod_count');
count.addAggregate('MAX','sys_mod_count');
count.addAggregate('AVG','sys_mod_count');
count.groupBy('category');
count.query();
while(count.next()){
  var min = count.getAggregate('MIN','sys_mod_count');
  var max = count.getAggregate('MAX','sys_mod_count');
  var avg = count.getAggregate('AVG','sys_mod_count');
  var category = count.category.getDisplayValue();
  gs.log(category +" Update counts: MIN = "+ min +" MAX = "+ max +" AVG = "+ avg);}
```

The output is:

```javascript
       *** Script: Data Import Update counts: MIN = 4.0 MAX = 21.0 AVG = 9.3333
       *** Script: Enhancement Update counts: MIN = 1.0 MAX = 44.0 AVG = 9.6711
       *** Script: Implementation Update counts: MIN = 4.0 MAX = 8.0 AVG = 6.0
       *** Script: inquiry Update counts: MIN = 0.0 MAX = 60.0 AVG = 5.9715
       *** Script: Inquiry / Help Update counts: MIN = 1.0 MAX = 3.0 AVG = 2.0
       *** Script: Issue Update counts: MIN = 0.0 MAX = 63.0 AVG = 14.9459
       *** Script: Monitor Update counts: MIN = 0.0 MAX = 63.0 AVG = 3.6561
       *** Script: request Update counts: MIN = 0.0 MAX = 53.0 AVG = 5.0987
```

The following is a more complex example that shows how to compare activity from one month to the next.

```javascript
var agg = new GlideAggregate('incident');
agg.addAggregate('count','category'); 
agg.orderByAggregate('count','category'); 
agg.orderBy('category'); 
agg.addQuery('opened_at','>=','javascript:gs.monthsAgoStart(2)'); 
agg.addQuery('opened_at','<=','javascript:gs.monthsAgoEnd(2)'); 
agg.query();
while(agg.next()){
  var category = agg.category;
  var count = agg.getAggregate('count','category');
  var query = agg.getQuery();
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count','category');
  agg2.orderByAggregate('count','category');
  agg2.orderBy('category');
  agg2.addQuery('opened_at','>=','javascript:gs.monthsAgoStart(3)');
  agg2.addQuery('opened_at','<=','javascript:gs.monthsAgoEnd(3)');
  agg2.addEncodedQuery(query);
  agg2.query();
  var last ="";
  while(agg2.next()){
     last = agg2.getAggregate('count','category');}
  gs.log(category +": Last month:"+ count +" Previous Month:"+ last);
 
}
```

The output is:

```javascript
 *** Script: Monitor: Last month:6866.0 Previous Month:4468.0
 *** Script: inquiry: Last month:142.0 Previous Month:177.0
 *** Script: request: Last month:105.0 Previous Month:26.0
 *** Script: Issue: Last month:8.0 Previous Month:7.0
 *** Script: Enhancement: Last month:5.0 Previous Month:5.0
 *** Script: Implementation: Last month:1.0 Previous Month:0
```

The following is an example to obtain distinct count of a field on a group query.

```javascript
var agg = new GlideAggregate('incident');
agg.addAggregate('count');
agg.addAggregate('count(distinct','category');
agg.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(2)');
agg.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(2)');
//
agg.groupBy('priority');
agg.query();
while (agg.next()) {
// Expected count of incidents and count of categories within each priority value (group)
  gs.info('Incidents in priority ' + agg.priority + ' = ' + agg.getAggregate('count') + 
            ' (' + agg.getAggregate('count(distinct','category') + ' categories)');
}
```

The output is:

```javascript
*** Script: Incidents in priority 1 = 13 (3 categories)
*** Script: Incidents in priority 2 = 10 (5 categories)
*** Script: Incidents in priority 3 = 5 (3 categories)
*** Script: Incidents in priority 4 = 22 (6 categories)
```

You can implement the SUM aggregate with or without the use of the groupBy\(\) method. If you do not use the groupBy\(\) method, the result of the SUM is the cumulative value for each different value of the field for which you request the SUM. For example, if you SUM the total\_cost field in the Fixed Asset table, and the Fixed Asset table contains 12 total records:

-   Three records with a total\_cost of $12
-   Four records with a total\_cost of $10
-   Five records with a total\_cost of $5

When you SUM the record set, the getAggregate\(\) method returns three different sums: $36, $40, and $25.

The following code illustrates implementing the SUM aggregate without using the groupBy\(\) method:

```javascript
var totalCostSum = new GlideAggregate('fixed_asset');
totalCostSum.addAggregate('SUM', 'total_cost');
totalCostSum.query();
 
while (totalCostSum.next()) {
  var allTotalCost = 0;
  allTotalCost = totalCostSum.getAggregate('SUM', 'total_cost');
  aTotalCost = totalCostSum.getValue('total_cost');
  gs.print('Unique field value: ' + aTotalCost + ', SUM = ' + allTotalCost + ', ' + allTotalCost/aTotalCost + ' records');
}
```

The output for this example is:

```javascript
*** Script: Unique field value: 12, SUM = 36, 3 records
*** Script: Unique field value: 10, SUM = 40, 4 records
*** Script: Unique field value: 5, SUM = 25, 5 records
```

Using the same data points as the prior example, if you use the groupBy\(\) method, the SUM aggregate returns the sum of all values for the specified field.

The following example illustrates implementing the SUM aggregate using the groupBy\(\) method:

```javascript
var totalCostSum = new GlideAggregate('fixed_asset');
totalCostSum.addAggregate('SUM', 'total_cost');
totalCostSum.groupBy('total_cost');
totalCostSum.query();
if(totalCostSum.next()){  // in case there is no result
   var allTotalCost = 0;
   allTotalCost = totalCostSum.getAggregate('SUM', 'total_cost');
   gs.print('SUM of total_cost: = ' + allTotalCost);
}
```

The output for this example is:

```javascript
*** Script: SUM of total_cost: 101
```

## Enforcing ACLs with GlideRecordSecure

GlideRecordSecure is a class inherited from GlideRecord that performs the same functions as GlideRecord, and also enforces ACLs.

By default, GlideRecordSecure doesn't enforce query ACLs. While it enforces standard read-write ACLs automatically, query ACLs require explicit opt-in by developers. For more information, see [Enforcing query ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/useful-server-side-scripts.md).

### Non-writable fields

When using GlideRecordSecure, non-writable fields are set to NULL when trying to write to the database. By default, the canCreate\(\) method on the column is replaced with canWrite\(\) on the column. If the canWrite\(\) method returns false, the column value is set to NULL.

### Getting the object type

You can check if an object type is ScopedGlideRecordSecure by calling the toString\(\) method.

-   **Checking the returned GlideRecord real type**

    The current object can be passed as ScopedGlideRecordSecure. In most cases, you can call current.toString\(\) to return the current object type.

    The following line returns `[object ScopedGlideRecordSecure]` for a ScopedGlideRecordSecure object:

    `gs.info(current.toString());`

-   **If the returned object type is different than expected**

    Calling a scoped function that returns a GlideRecord object as its type returns different results depending on the scope it’s called from.

    -   Calling the scoped function within application scope returns the expected object type of `GlideRecord` or `GlideRecordSecure`.
    -   Calling the scoped function within global scope returns the object type is `ScopedGlideRecord` or `ScopedGlideRecordSecure`.

### Checking for NULL values

If an element cannot be read because an ACL restricts access, a NULL value is created in memory for that record. With GlideRecord, you must explicitly check for any ACLs that might restrict read access to the record. To do so, an `if`statement such as the following is required to check if the record can be read:

```javascript
if (!now_GRScanRead())
   continue;
```

With GlideRecordSecure, it's unnecessary to explicitly check for read access using canRead\(\). Instead, you can use next\(\) by itself to move to the next record. The following example provides a comparison between GlideRecord and GlideRecordSecure.

```javascript
var count = 0;
var now_GR = new GlideRecord('mytable');
now_GR.query(); 
while (now_GR.next()) { 
    if (!now_GR.canRead()) continue; 
    if (!now_GR.canWrite()) continue; 
    if (!now_GR.val.canRead() || !now_GR.val.canWrite())
        now_GR.val = null;
    else
        now_GR.val = "val-" + now_GR.id; 
    if (now_GR.update())
        count ++; 
}
```

```javascript
var count = 0;
var now_GRS = new GlideRecordSecure('mytable');
now_GRS.query(); 
while (now_GRS.next()) {
    now_GRS.val = "val-" + now_GRS.id; 
    if (now_GRS.update())
        count ++; 
}
```

### Enforcing query ACLs

By default, GlideRecordSecure doesn't enforce query ACLs. Query ACL enforcement requires explicit opt-in.

Enforcing query ACLs is a security approach that ensures users can only query fields and records they're authorized to access. This strategy provides defense-in-depth by applying access controls at the query level, not just at the data retrieval level. Explicit query ACL enforcement represents a more secure design pattern for applications handling user input.

To explicitly specify query ACL enforcement behavior, use GlideRecordSecure.addEncodedQuery\(\). Update the basic addEncodedQuery\(query\) usage without explicit ACL specification. Use one of the following secure options.

-   **Option 1: Convenience methods \(recommended\)**

    Use the [addUserEncodedQuery\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md) method for the following use cases:

    -   Queries built from user input in which query ACLs apply
    -   Build dynamic filters based on user selections
    -   Handle untrusted data
    Use the [addSystemEncodedQuery\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md) method for the following use cases:

    -   Hard-coded query conditions
    -   Back end or system-only logic with no user input
    -   Safe, predefined query conditions
    Mix both methods as needed. Different parts of your query can use different enforcement levels based on their source.

    ```javascript
    // Queries built from user input
    nowGRS_ACL.addUserEncodedQuery(userInput);
    
    // Hard-coded system queries
    nowGRS.addSystemEncodedQuery("active=true");
    ```

-   **Option 2: Boolean parameter**

    The following example shows how to use the [addEncodedQuery\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md) method for ACL enforcement.

    ```javascript
    // Explicitly enforce query ACLs
    var now_GRS_true = new GlideRecordSecure(<table_name>); 
    nowGRS_true.addEncodedQuery(query, true);
    
    // Explicitly skip query ACL enforcement (use cautiously) 
    var nowGRS_false = new GlideRecordSecure(<table_name>); 
    nowGRS_false.addEncodedQuery(query, false);
    ```


### Examples

These are two simple examples using GlideRecordSecure.

```javascript
var att = new GlideRecordSecure('sys_attachment');
att.get('$[sys_attachment.sys_id]'); 
var sm = GlideSecurityManager.get(); 
var checkMe = 'record/sys_attachment/delete'; 
var canDelete = sm.hasRightsTo(checkMe, att);
gs.log('canDelete: ' + canDelete);
canDelete;
```

```javascript
var now_GRS = new GlideRecordSecure('task_ci');
now_GRS.addSystemQuery();
now_GRS.query(); 
var count = now_GRS.getRowCount(); 
if (count > 0 ) { 
    var allocation = parseInt(10000/count) / 100;
    while (now_GRS.next()) {
      now_GRS.u_allocation = allocation;
      now_GRS.update();
    }
}
```

## Get a user object

In a business rule or other server script, the gs.getUser\(\) method returns a user object. The user object is an internal representation of the currently logged in user and provides information about the user and various utility functions.

### About this task

For a list and description of the available scoped methods for the user object, see [GlideUser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/GUserAPI.md).

### Procedure

1.  Retrieve the current user.

    ```javascript
    var myUserObject = gs.getUser()
    ```

2.  Use the getUserByID method to fetch a different user using the `user_name` field or `sys_id` on the target record.

    For example:

    ```javascript
    var ourUser = gs.getUser(); 
    gs.print(ourUser.getFirstName()); //print the first name of the user you are currently logged in as 
    newUser = ourUser.getUserByID(<user_sys_id>); //fetch a different user, using the sys_id of the target user record. 
    gs.print(newUser.getFirstName()); //first name of the user you fetched above 
    gs.print(newUser.isMemberOf('Capacity Mgmt'));
    ```


## Log output

GSLog is a script include that simplifies script logging and debugging by implementing levels of log output, selectable by per-caller identified sys\_properties values.

### Log level

Logs can be at the level of debug, info, notice, warning, err, or crit \(after BSD syslog.h and followers\). The default logging level is notice, so levels should be chosen accordingly.

### Where to use

Use for any server-side script where you want to implement event logging.

For the API reference, see [GSLog\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/GSLogBoth.md).

For more information, see [Debugging scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/script-debug-overview.md)

## Manipulate date and time values

The GlideDateTime class provides methods for performing operations on GlideDateTime objects, such as instantiating GlideDateTime objects or working with *glide\_date\_time* fields.

In addition to the instantiation methods described below, a GlideDateTime object can be instantiated from a *glide\_date\_time* field using the getGlideObject\(\) method \(for example, `var gdt = gr.my_datetime_field.getGlideObject();`\).

Some methods use the Java Virtual Machine time zone when retrieving or modifying a date and time value. Using these methods may result in unexpected behavior. Use equivalent local time and UTC methods whenever possible.

### GlideDate and GlideDateTime examples

The GlideDate and GlideDateTime APIs are used to manipulate date and time values.

For additional information, refer to [GlideDate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideDateScopedAPI.md) API and [GlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideDateTimeScoped.md) API.

You can create a GlideDateTime object from a GlideDate object by passing in the GlideDate object as a parameter to the GlideDateTime constructor. By default, the GlideDateTime object is expressed in the internal format, yyyy-MM-dd HH:mm:ss and the system time zone UTC.

```javascript
var gDate = new GlideDate();
gDate.setValue('2015-01-01');
gs.info(gDate);
 
var gDT = new GlideDateTime(gDate);
gs.info(gDT);
```

Output:

```javascript
2015-01-01
2015-01-01 00:00:00
```

#### Modify a GlideDateTime field value

This example demonstrates how to modify a GlideDateTime field value using a server-side script.

The following server-side script example shows how to modify values using the GlideDateTime API. The same concept also applies to the GlideDate object.

**Note:** The following script is only intended for global applications.

```javascript
//You first need a GlideDateTime object
//this can be from instantiating a new object "var gdt = new GlideDateTime()"
//or getting the object from a GlideDateTime field
//getting the field value (for example: var gdt = current.start_date) only returns the string value, not the object
//to get the object use var gdt = current.start_date.getGlideObject(); (GlideElement)
//now gdt is a GlideDateTime object
var gdt = current.start_date.getGlideObject();
 
//All methods can use negative values to subtract intervals
 
//add 1 hour (60 mins * 60 secs)
gdt.addSeconds(3600);
 
//add 1 day
gdt.addDaysLocalTime(1);
 
//subtract 1 day
gdt.addDaysLocalTime(-1);
 
//add 3 weeks
gdt.addWeeksLocalTime(3);
 
//subtract 6 months
gdt.addMonthsLocalTime(-6);
 
//add 1 year, representing the date and time using the UTC timezone instead of the local user's timezone.
gdt.addYearsUTC(1);
 
//set the value of the GlideDateTime object to the current session timezone/format
GlideSession.get().setTimeZoneName('US/Eastern');
gdt.setDisplayValue('2018-2-28 00:00:00');
gs.info('In ' + GlideSession.get().getTimeZoneName() + ": " + gdt.getDisplayValue());
```

See also:

-   [Manipulate date and time values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/useful-server-side-scripts.md)
-   [GlideDate - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/GlideDateAPI.md)
-   [GlideDate - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideDateScopedAPI.md)
-   [GlideDateTime - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideDateTimeAPI.md)
-   [GlideDateTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideDateTimeScoped.md)
-   [GlideElement - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideElementAPI.md)
-   [GlideElement - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideElementScopedAPI.md)
-   [GlideTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideTimeScopedAPI.md)

### Set a duration field value in script

Examples of JavaScript that can be used to set the value of a duration field.

**Note:** Negative duration values are not supported.

#### Using the GlideDateTime.subtract\(\) method

The subtract\(GlideDateTime start, GlideDateTime end\) method in [GlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_GlideDateTimeScoped.md) enables you to set the duration value using a given start date/time and end date/time. An example on how to set the duration for the time a task was opened is:

```javascript
var duration = GlideDateTime.subtract(start, end);
```

If you want to work with the value returned as a number to use in date or duration arithmetic, convert the return to milliseconds:

```javascript
var time = GlideDateTime.subtract(start,end).getNumericValue();

```

If you want to set a duration to the amount of time between some event and the current date/time:

```javascript
<duration_field> = GlideDateTime.subtract(new GlideDateTime(<start_time>.getValue()),gs.nowDateTime());
```

The time values presented to GlideDateTime.subtract are expected to be in the user's time zone and in the user's format.

#### Setting a default value of a duration field

Setting the default value for a duration field is similar to the method used in the previous topic.

#### Setting the duration field value in a client script

This script sets a *duration\_field* value in a client script. Replace *duration\_field* with the field name from your instance.

```javascript
g_form.setValue('<duration_field>','11 01:02:03');
```

#### Calculating and setting a duration using a client script

Here is an example of how to return a value and populate it using a client script.

Create an `onChange` client script that includes the following code. You can modify this script if you need the calculation to happen in an `onLoad` script or some other way.

```javascript
function onChange(control, oldValue, newValue, isLoading){
var strt = g_form.getValue('<start_field>');
var end = g_form.getValue('<end_field>');
var ajax = new GlideAjax('AjaxDurCalc');
  ajax.addParam('sysparm_name','durCalc');
  ajax.addParam('sysparm_strt',strt);
  ajax.addParam('sysparm_end',end);
  ajax.getXMLWait();
  var answer = ajax.getAnswer();
  g_form.setValue('<duration_field>', answer);}
```

Create a system script include file called *AjaxDurCalc* that handles the request. It may be reused for other functions as well.

```javascript
var AjaxDurCalc = Class.create();
AjaxDurCalc.prototype = Object.extendsObject(AbstractAjaxProcessor,{
 durCalc:function(){return GlideDuration.subtract(this.getParameter('sysparm_strt'),this.getParameter('sysparm_end'));}});
```

#### Changing the duration field value

If you manipulate a duration value with addition/subtraction of some amount of time, use the functions that allow you to get and set the numeric value of the duration. A unit of measure for a duration numeric value is milliseconds. The following is an example that adds 11 seconds to the *duration* field in the current record.

```javascript
var timems = current.duration.dateNumericValue();
timems = timems + 11*1000; 
current.duration.setDateNumericValue(timems);
```

#### Formatting the Resolve Time

To format the **Resolve Time** or the **Business Resolve Time** fields as durations, which displays them as a duration instead of a large integer, add the following attribute to those fields:

```xml
format=glide_duration
```

Modify the dictionary entry for the field and add the attribute. If there is an existing attribute, separate multiple attributes with commas.

#### Setting the maximum unit of measurement

The *max\_unit* dictionary attribute defines the maximum unit of time used in a duration. For example, if `max_unit=minutes`, a duration of 3 hours 5 minutes 15 seconds appears as 185 minutes 15 seconds. To set the maximum unit of duration measurement, add the following dictionary attribute to the *duration* field:

```xml
max_unit=<unit>
```

### Date and time format guidelines

You can specify a date format with a sequence of specific date and time pattern strings. A pattern string consists of one or more uppercase and lowercase letters from A to Z. Any text within quotation marks is ignored and is instead copied into the date output.

|String|Description|Output Format|Example|
|------|-----------|-------------|-------|
|G|Era designator|Text|AD|
|y|Year|Year|2019; 19|
|Y|Week in year|Year|2019; 19|
|M|Month in year \(within date\)|Month|July; Jul; 07|
|L|Month in year \(standalone value\)|Month|July; Jul; 07|
|w|Week in year|Number|52|
|W|Week in month|Number|1|
|D|Day in year|Number|365|
|d|Day in month|Number|2|
|F|Day of week in month|Number|3|
|E|Day name in week|Text|Wednesday; Wed|
|u|Day number of week|Number|3|
|a|a.m. or p.m.|Text|p.m.|
|H|Hour in day from 0 through 23|Number|0|
|k|Hour in day from 1 through 24|Number|24|
|K|Hour in a.m. or p.m. from 0 through 11|Number|0|
|h|Hour in a.m. or p.m. from 1 through 12|Number|12|
|m|Minute in hour|Number|59|
|s|Second in minute|Number|1|
|S|Millisecond|Number|500|
|z|Time zone in default format|Time zone in default format|Pacific Standard Time; PST|
|Z|Time zone in RFC 822 format|Time zone in RFC 822 format|-0800|
|X|Time zone in ISO 8601 format|Time zone in ISO 8601 format|-08; -0800; -08:00|

## Using custom queues to process events

You can use custom queues for applications that create a large volume of events or events that take a long time to process. This task shows how to create a custom queue, its monitoring process, and use a script to send events to the queue.

### Before you begin

Role required: admin

**Note:** This information is for advanced users who understand event processing.

### Procedure

1.  Navigate to **System Policy** &gt; **Events** &gt; **Registry**.

2.  Select the event for which you want to create a custom queue.

    The **Event Registration** form displays.

3.  Populate the **Queue** field for the event in the Event Registry.

    Use only lowercase letters, no spaces, and no special characters except underscore \(\_\).

4.  Click **Submit**.

    A new event is listed in the Events \[sysevent\] table.

    In the following example, when the employeeOccasion event is generated, the event is added to my\_queue. The events are stuck in the queue. To resolve this issue, create a process to watch the queue for events.\[Omitted image "queue-create-new-val.png"\] Alt text: Events table listing the event with the added queue listed in the queue field.

5.  Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs** and open the scheduled job named **text index events process**.

    \[Omitted image "queue-create-process-locate.png"\] Alt text: Schedule table with \*text in the Name search field and the name of the text index events process schedule highlighted.

6.  Click the additional actions menu icon \[Omitted image "additional\_icon.png"\] Alt text: additional actions icon menu\)--&gt; and select **Insert and Stay** to create a copy of **text index events process**.

    **Important:** Be sure to copy the job and not overwrite the **text index events process** Scheduled Job.

7.  In the copied schedule item, change the value in the **Name** field.

8.  In the **Job context** field, replace the value for the GlideEventManager\(\) parameter with the name of the new queue.

    \[Omitted image "queue-create-process-name.png"\] Alt text: Schedule Item form showing the copied item renamed and the updated queue name for GlideEventManager in theJob context field.

    The queue monitoring process looks for and processes events in the example **my\_queue** event queue.

    \[Omitted image "queue-create-processed.png"\] Alt text: Events table highlighting the contents of the Processed and Queue fields.

9.  Use the gs.eventQueue\(\) method's fifth parameter to send events to the custom queue.

    The following code shows how to send an event to the my\_queue custom queue.

    ```javascript
    gs.eventQueue('x_60157_employee_spe.employeeOccasion', todaysOccasions, todaysOccasions.number, todaysOccasions.u_employee.name, 'my_queue');
    ```

    **Note:** If an event is in the **Event Registry** and no queue name is provided to gs.eventQueue, the queue from the **Event Registry** is still assigned to the event. For example, `gs.eventQueue('x_60157_employee_spe.employeeOccasion')` still associates the event with `my_queue`. If the queue name is provided in the `gs.eventQueue()` call, the queue takes priority.

    You can verify that the event called was processed by checking the **Events** \[sysevent\] table.



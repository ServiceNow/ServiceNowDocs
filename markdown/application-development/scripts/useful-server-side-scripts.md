---
title: Server-side script use cases
description: Use cases for server-side scripts include logging output, getting user objects, and modifying date/time values.A catalog item has been requested, and the attached workflow contains a run script activity that populates a value in the scratchpad. From a business rule running on the requested item, you want to retrieve or set scratchpad values.Assign a service catalog item to the database group if it uses a delivery plan that has a catalog task that is assigned to the desktop group.Often you may need to provide users with a way to specify when a task or process is due. Using the DurationCalculator script include, you can calculate the due date using either a simple duration or relative duration.How much work is required to complete a task can be expressed as a "relative duration".This business rule and script example demonstrate how to calculate a simple duration.An example of a relative duration calculation script.You can implement a relative duration by creating the cmn\_relative\_duration table and the DurationCalculator script include.The cmn\_relative\_duration table supports the definition of a due date as either a duration of time or a relative duration.In a business rule or other server script, the gs.getUser\(\) method returns a user object. The user object is an internal representation of the currently logged in user and provides information about the user and various utility functions.GSLog is a script include that simplifies script logging and debugging by implementing levels of log output, selectable by per-caller identified sys\_properties values.This example demonstrates how to modify a GlideDateTime field value using a server-side script.You can use custom queues for applications that create a large volume of events or events that take a long time to process. This task shows how to create a custom queue, its monitoring process, and use a script to send events to the queue.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-02-04"
reading_time_minutes: 16
breadcrumb: [Useful scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Server-side script use cases

Use cases for server-side scripts include logging output, getting user objects, and modifying date/time values.

**Parent Topic:**[Useful scripts](usefulScripts.md)

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

```
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

```
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

Typically, setting a due date requires that you calculate work time rather than the total time. Only the part of the day when work is performed is considered when determining the due date. For example, a task is due in 10 hours, but is restricted to a business day schedule. If the work starts at 10am on Monday, it is due on Tuesday at 12pm as calculated below.

```
10am-5pm on Monday (6 hours) + 8am-12pm on Tuesday (4 hours)
```

For information on schedules, which you can use as inputs to DurationCalculator methods, see [Creating and using schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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
 
    // First we need a DurationCalculator object.var dc =new DurationCalculator();
 
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

For more information on relative durations, see [Define a relative duration](https://www.servicenow.com/docs/access?context=t_DefineARelativeDuration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

#### Calculating a simple duration

This business rule and script example demonstrate how to calculate a simple duration.

```
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

```
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

```
// Next day at 4pm if before 10am
var days =1;
if(calculator.isAfter(calculator.startDateTime,"10:00:00")) 
      days++;
 
calculator.calcRelativeDueDate(calculator.startDateTime, days,"16:00:00");
```

This script demonstrates how to use DurationCalculator to calculate a relative duration.

```
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

## Get a user object

In a business rule or other server script, the gs.getUser\(\) method returns a user object. The user object is an internal representation of the currently logged in user and provides information about the user and various utility functions.

### About this task

For a list and description of the available scoped methods for the user object, see [GlideUser](https://www.servicenow.com/docs/access?context=GUserAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

### Procedure

1.  Retrieve the current user.

    ```
    var myUserObject = gs.getUser()
    ```

2.  Use the getUserByID method to fetch a different user using the `user_name` field or `sys_id` on the target record.

    For example:

    ```
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

For the API reference, see [GSLog\(\)](https://www.servicenow.com/docs/access?context=GSLogBoth&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

For more information, see [Debugging scripts](https://www.servicenow.com/docs/access?context=script-debug-overview&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

## Modify a GlideDateTime field value

This example demonstrates how to modify a GlideDateTime field value using a server-side script.

Given a GlideDateTime field or script object, show a variety of ways to easily modify value. The same concept also applies to the GlideDate object.

**Note:** The following script is only intended for global applications.

```
//You first need a GlideDateTime object
//this can be from instantiating a new object "var gdt = new GlideDateTime()"
//or getting the object from a GlideDateTime field
//getting the field value (for example: var gdt = current.start_date) only returns the string value, not the object
//to get the object use var gdt = current.start_date.getGlideObject();
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

-   [GlideDateTime](https://www.servicenow.com/docs/access?context=p_GlideServerAPIs&version=yokohama&pubname=yokohama-api-reference&section=c_GlideDateTime&ft:locale=en-US)
-   [GlideDate - Global](https://www.servicenow.com/docs/access?context=GlideDateAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [GlideDate - Scoped](https://www.servicenow.com/docs/access?context=c_GlideDateScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [GlideDateTime - Global](https://www.servicenow.com/docs/access?context=c_GlideDateTimeAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [GlideDateTime - Scoped](https://www.servicenow.com/docs/access?context=c_GlideDateTimeScoped&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [GlideTime - Scoped](https://www.servicenow.com/docs/access?context=c_GlideTimeScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

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

    ![Event Registration form highlighting Queue field containing the name of the queue in lower case.](../image/queue-create-field.png)

4.  Click **Submit**.

    A new event is listed in the Events \[sysevent\] table.

    In the following example, when the employeeOccasion event is generated, the event is added to my\_queue. The events are stuck in the queue. To resolve this issue, create a process to watch the queue for events.![Events table listing the event with the added queue listed in the queue field.](../image/queue-create-new-val.png)

5.  Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs** and open the scheduled job named **text index events process**.

    ![Schedule table with *text in the Name search field and the name of the text index events process schedule highlighted.](../image/queue-create-process-locate.png)

6.  Click the additional actions menu icon ![additional actions icon menu](../../../product/wsd-indoor-mapping/images/additional_icon.png)\)--&gt; and select **Insert and Stay** to create a copy of **text index events process**.

    **Important:** Be sure to copy the job and not overwrite the **text index events process** Scheduled Job.

7.  In the copied schedule item, change the value in the **Name** field.

8.  In the **Job context** field, replace the value for the GlideEventManager\(\) parameter with the name of the new queue.

    ![Schedule Item form showing the copied item renamed and the updated queue name for GlideEventManager in theJob context field.](../image/queue-create-process-name.png)

    The queue monitoring process looks for and processes events in the example **my\_queue** event queue.

    ![Events table highlighting the contents of the Processed and Queue fields.](../image/queue-create-processed.png)

9.  Use the gs.eventQueue\(\) method's fifth parameter to send events to the custom queue.

    The following code shows how to send an event to the my\_queue custom queue.

    ```
    gs.eventQueue('x_60157_employee_spe.employeeOccasion', todaysOccasions, todaysOccasions.number, todaysOccasions.u_employee.name, 'my_queue');
    ```

    **Note:** If an event is in the **Event Registry** and no queue name is provided to gs.eventQueue, the queue from the **Event Registry** is still assigned to the event. For example, `gs.eventQueue('x_60157_employee_spe.employeeOccasion')` still associates the event with `my_queue`. If the queue name is provided in the `gs.eventQueue()` call, the queue takes priority.

    You can verify that the event called was processed by checking the **Events** \[sysevent\] table.

    ![Events table listing processed events filtered by the event name.](../image/queue-use-sent.png)



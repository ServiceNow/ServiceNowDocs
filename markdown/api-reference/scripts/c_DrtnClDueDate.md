---
title: Using DurationCalculator to calculate a due date
description: Using the DurationCalculator script include, you can calculate a due date, using either a simple duration or a relative duration base on schedules.A simple duration is the number of seconds between two date times.Relative duration is very similar to simple duration except a piece of script is used to determine what parts of a day to remove from the difference calculation.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Using DurationCalculator to calculate a due date

Using the DurationCalculator script include, you can calculate a due date, using either a simple duration or a relative duration base on schedules.

The following script demonstrates how to use the global API [DurationCalculator](../../../app-store/dev_portal/API_reference/DurationCalculator/concept/c_DurationCalculatorAPI.md#) to calculate a due date. The first part of the script illustrates how to set a start datetime using the [setStartDateTime\(\)](../../../app-store/dev_portal/API_reference/DurationCalculator/concept/c_DurationCalculatorAPI.md#) method and then use the [calcDuration\(\)](../../../app-store/dev_portal/API_reference/DurationCalculator/concept/c_DurationCalculatorAPI.md#) method to determine a due date that is "x" amount of continuous time \(seconds\) from the specified start datetime. The second half of the script illustrates how to use DurationCalculator to calculate a due date based on a schedule. Schedules enable you to apply a "filter" on future time, such as only including the days in a work week within the calculation. For example, if you apply a schedule "weekdays" \(which only includes Monday through Friday\) to your duration calculation, and the start datetime is Friday at 5:00 pm, when you add a duration of two days, your due date would be Tuesday at 5:00 pm. If you did not use a schedule, your due date would be Sunday at 5:00 pm. For additional information on schedules, see [Creating and using schedules](https://www.servicenow.com/docs/access?context=c_UseSchedules&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

This script can be cut and pasted into the Scripts Background page and run as is. It can also serve as an example for authoring business rules, UI actions, or used any other place that server-side script can be authored.

```
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
 */
function executeSample(){
 
    // First we need a DurationCalculator object.
    var dc = new DurationCalculator();
 
    // --------------- No schedule examples ------------------
 
    // Simple computation of a due date without using a schedule. Seconds
    // are added to the start date continuously to get to a due date.
    var gdt = new GlideDateTime("2012-05-01 00:00:00");
    dc.setStartDateTime(gdt);
    if(!dc.calcDuration(2*24*3600)){ // 2 days
      gs.log("*** Error calculating duration");
      return;
    }
    gs.log("calcDuration no schedule: " + dc.getEndDateTime()); // "2012-05-03 00:00:00" two days later
 
    // Start in the middle of the night (2:00 am) and compute a due date 1 hour in the future
    // Without a schedule this yields 3:00 am.
    var gdt = new GlideDateTime("2012-05-03 02:00:00");
    dc.setStartDateTime(gdt);
    if(!dc.calcDuration(3600)){
      gs.log("*** Error calculating duration");
      return;
     }
    gs.log("Middle of night + 1 hour (no schedule): "+ dc.getEndDateTime()); // No scheduled start date, just add 1 hour
 
 
    // -------------- Add a schedule to the date calculator ---------------------
    addSchedule(dc);
 
    // Start in the middle of the night and compute a due date 1 hour in the future.
    // Since we start at 2:00 am the computation adds the 1 hour from the start
    // of the day, 8:00am to get to 9:00am
    var gdt = new GlideDateTime("2012-05-03 02:00:00");
    dc.setStartDateTime(gdt);
    if(!dc.calcDuration(3600)){
      gs.log("*** Error calculating duration");
      return;
    }
    gs.log("Middle of night + 1 hour (with 8-5 schedule): " + dc.getEndDateTime()); // 9:00 am
 
    // Start in the afternoon and add hours beyond quiting time. Our schedule says the work day
    // ends at 5:00pm, if the duration extends beyond that, we roll over to the next work day.
    // In this example we are adding 4 hours to 3:00pm which gives us 10:00 am the next day.
    var gdt = new GlideDateTime("2012-05-03 15:00:00");
    dc.setStartDateTime(gdt);

    if(!dc.calcDuration(4*3600)){ 
      gs.log("*** Error calculating duration");
      return;}
    gs.log("Afternoon + 4 hour (with 8-5 schedule): " + dc.getEndDateTime()); // 10:00 am.
 
    // This is a demo of adding 2 hours repeatedly and examine the result. This
    // is a good way to visualize the result of a due date calculation.
    var gdt = new GlideDateTime("2012-05-03 15:00:00");
    dc.setStartDateTime(gdt); 
    for(var i=2; i<24; i+=1){
      if(!dc.calcDuration(i*3600)){
        gs.log("*** Error calculating duration");
        return;
      }
      gs.log("add "+ i +" hours gives due date: " + dc.getEndDateTime());
    }
 
    // Setting the timezone causes the schedule to be interpreted in the specified timezone.
    // Run the same code as above with different timezone. Note that the 8 to 5 workday is
    // offset by the two hours as specified in our timezone.
    dc.setTimeZone("GMT-2");
    var gdt = new GlideDateTime("2012-05-03 15:00:00");
    dc.setStartDateTime(gdt);
    for(var i=2; i<24; i+=1){
      if(!dc.calcDuration(i*3600)){ 
        gs.log("*** Error calculating duration");
        return;
      }
        gs.log("add "+ i +" hours gives due date (GMT-2): " + dc.getEndDateTime());
    }
}
 
/** 
 * Add a specific schedule to the DurationCalculator object.
 *  
 * @param durationCalculator An instance of DurationCalculator
 */
function addSchedule(durationCalculator){
    // Load the "8-5 weekdays excluding holidays" schedule into our duration calculator.
    var scheduleName = "8-5 weekdays excluding holidays";
    var grSched = new GlideRecord('cmn_schedule');
    grSched.addQuery('name', scheduleName);
    grSched.query();
    if(!grSched.next()){
      gs.log('*** Could not find schedule "'+ scheduleName +'"');
      return;
    }
    durationCalculator.setSchedule(grSched.getUniqueValue(),"GMT");
}
```

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

## Using DurationCalculator to compute a simple duration

A simple duration is the number of seconds between two date times.

If no schedule is used then this is a simple time date subtraction. If a schedule is used, then the schedule is consulted to remove non-work hours from the computation. Suppose schedule "8-5 weekdays excluding holidays" is used. In this case, the number of work hours from noon Monday to noon Tuesday is nine hours. To compute a simple duration, initialize the global API DurationCalculator and call the [calcScheduleDuration\(\)](../../../app-store/dev_portal/API_reference/DurationCalculator/concept/c_DurationCalculatorAPI.md#) method.

This script demonstrates how to use DurationCalculator to compute a simple duration.

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
    var dc = new DurationCalculator();
 
    // Compute a simple duration without any schedule. The arguments
    // can also be of type GlideDateTime, such as fields from a GlideRecord.
    var dur = dc.calcScheduleDuration("2012-05-01", "2012-05-02");
    gs.log("calcScheduleDuration no schedule: " + dur); // 86400 seconds (24 hours)
 
    // The above sample is useful in limited cases. We almost always want to 
    // use some schedule in a duration computation, let's load a schedule.
    addSchedule(dc);
 
    // Compute a duration using the schedule. The schedule
    // specifies a nine hour work day. The output of this is 32400 seconds, or
    // a nine hour span.
    dur = dc.calcScheduleDuration("2012-05-23 12:00:00","2012-05-24 12:00:00");
    gs.log("calcScheduleDuration with schedule: " + dur); // 32400 seconds (9 hours)
 
    // Compute a duration that spans a weekend and holiday. Even though this
    // spans three days, it only spans 9 work hours based on the schedule.
    dur = dc.calcScheduleDuration("2012-05-25 12:00:00", "2012-05-29 12:00:00");
    gs.log("calcScheduleDuration with schedule spaning holiday: " + dur); // 32400 seconds (9 hours)
 
    // Use the current date time in a calculation. The output of this is
    // dependent on when you run it.
    var now = new Date();
    dur = dc.calcScheduleDuration("2012-05-15", new GlideDateTime());
    gs.log("calcScheduleDuration with schedule to now: " + dur); // Different on every run.
}
 
/** 
 * Add a specific schedule to the DurationCalculator object.
 *  
 * @param durationCalculator An instance of DurationCalculator
 */
function addSchedule(durationCalculator){
    // Load the "8-5 weekdays excluding holidays" schedule into our duration calculator.
    var scheduleName = "8-5 weekdays excluding holidays";
    var grSched = new GlideRecord('cmn_schedule');
    grSched.addQuery('name', scheduleName);
    grSched.query();
    if(!grSched.next()){
        gs.log('*** Could not find schedule "'+ scheduleName +'"');
        return;
    }
    durationCalculator.setSchedule(grSched.getUniqueValue());
}
```

## Using relative duration

Relative duration is very similar to simple duration except a piece of script is used to determine what parts of a day to remove from the difference calculation.

This script is stored in table cmn\_relative\_duration and can be examined by navigating to **System Scheduler** &gt; **Schedules** &gt; **Relative Durations**. There are some example relative duration scripts in the out-of-the-box instance.

A relative duration sys\_id is passed to the method calcRelativeDuration\(\) of the global API [DurationCalculator](../../../app-store/dev_portal/API_reference/DurationCalculator/concept/c_DurationCalculatorAPI.md#) class after initialization. When this method is called, the DurationCalculator object is passed to the relative duration script \(stored in table cmn\_relative\_duration\) as the variable *calculator*. So, the relative duration script you write and store in cmn\_relative\_duration has access to the executing DurationCalculator through the variable *calculator*.

The following script demonstrates how to use DurationCalculator to calculate a relative duration.

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
    var dc = new DurationCalculator();
    var relDur = "3bf802c20a0a0b52008e2859cd8abcf2"; // 2 bus days by 4pm if before 10am
    addSchedule(dc);
 
    // Since our start date is before 10:00am our result is two days from// now at 4:00pm.
    var gdt = new GlideDateTime("2012-05-01 09:00:00");
    dc.setStartDateTime(gdt);
    if(!dc.calcRelativeDuration(relDur)){
      gs.log("*** calcRelativeDuration failed");
      return;
    }
    gs.log("Two days later 4:00pm: "+ dc.getEndDateTime());
 
    // Since our start date is after 10:00am our result is three days from
    // now at 4:00pm.
    var gdt = new GlideDateTime("2012-05-01 11:00:00");
    dc.setStartDateTime(gdt);
    if(!dc.calcRelativeDuration(relDur)){
      gs.log("*** calcRelativeDuration failed");
      return;
    }
    gs.log("Three days later 4:00pm: "+ dc.getEndDateTime());}
 
/** 
 * Add a specific schedule to the DurationCalculator object.
 *  
 * @param durationCalculator An instance of DurationCalculator
 */
function addSchedule(durationCalculator){
    // Load the "8-5 weekdays excluding holidays" schedule into our duration calculator.
    var scheduleName ="8-5 weekdays excluding holidays";
    var grSched =new GlideRecord('cmn_schedule');
    grSched.addQuery('name', scheduleName);
    grSched.query();
    if(!grSched.next()){
      gs.log('*** Could not find schedule "'+ scheduleName +'"');
      return;}
    durationCalculator.setSchedule(grSched.getUniqueValue(),"GMT");}
```


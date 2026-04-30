---
title: Date/time input setup for different action item types
description: After you create an input form screen and define its IncludeTimezone attribute for date/time inputs, you must associate the input form screen with an action item. How you set up the date/time inputs depends on the type of action item you use.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure inputs, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Date/time input setup for different action item types

After you create an input form screen and define its IncludeTimezone attribute for date/time inputs, you must associate the input form screen with an action item. How you set up the date/time inputs depends on the type of action item you use.

<table id="table_iz4_xnx_t5b"><thead><tr><th>

Action item type

</th><th>

Set up

</th></tr></thead><tbody><tr><td>

**New** or **Update**

</td><td>

Make sure that date/time inputs are mapped to date/time fields in the back-end instance. The back-end instance uses the Device Time Zone information sent by the input form screen. Then the back-end instance converts the date/time value to Coordinated Universal Time \(UTC/GMT\) before saving it to the database.

</td></tr><tr><td>

**Script**

</td><td>

You must convert the date/time input value to UTC/GMT. Refer to the following script examples for more information. For more information about scripting in general for ServiceNow, see [Scripting](https://www.servicenow.com/docs/access?context=c_Script&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) **Note:** Customizations might be needed depending on the use case involved.

</td></tr></tbody>
</table>## GlideDateTime script example

The following example sets fields of the GlideDateTime type.

```
/sys_sg_write_back_action_step.do?sys_id=b390e6a7c1120110fa9b5abd6a7dbb64
(function WriteBackAction(parm_input, parm_variable, actionResult) {
	var shortDescription = parm_input.shortdescription;
	var scheduledStart = parm_input.expectedstart;
	var estimatedEnd = parm_input.estimatedend;
	var description = parm_input.description;
	var wotSysId = parm_variable['sys_id'];
	
	var wotGr = new GlideRecord("wm_task");
	wotGr.get(wotSysId);
	wotGr.setValue("description", description);
	wotGr.setValue("short_description", shortDescription);
	
	var newEnd = new GlideDateTime(estimatedEnd);
	var endMS = newEnd.getNumericValue();
	
	var newStart = new GlideDateTime(scheduledStart);
	var startMS = newStart.getNumericValue();
	
	if (endMS - startMS < 0) {
		gs.addErrorMessage(gs.getMessage("The start date should come before the end date"));
	} else {
		//set the time on screen all the time
		wotGr.setValue("expected_start", newStart);
		wotGr.setValue("estimated_end", newEnd);
		var duration = endMS - startMS;
		var newDur = new GlideDuration();
		newDur.setValue(duration);
		wotGr.setValue("estimated_work_duration", newDur);
		
		//check double booking no matter which field is changed. set needs_attention so that dispatcher can review it.
		var info = new global.FSMAgentInfo(gs.getUserID());
		var doubleBooking = info.allowAgentDoubleBookingTask();
		if (doubleBooking){
			var conflict = !(new global.SMDDateValidation().checkSchedulingConflictSimple(wotGr));
			if (conflict) {
				//BR Date Checks will display conflict message as Warning: {0} has been scheduled for a time the assigned
				//only when time change.
				wot.Gr.setValue("needs_attention", true);
			}
		}
```

-   In this example, the `expected_start` and `estimated_end` fields are edited based on the values of their corresponding date/time inputs of `expectedstart` and `estimatedend`.
-   Because the IncludeTimezone attribute is set to `true`, the `parm_input.expectedstart` variable returns a date/time string in the format YYYY-MM-DDThh:mm:ss.sssTZD. To enable the system to handle this date/time format, initialize a GlideDateTime object by passing the string into the constructor.
-   Because `expected_start` and `estimated_end` are Date Time columns in the database, you can directly call GlideRecord.setValue\(\) and pass the `GlideDateTime` object as the value.

## GlideScheduleDateTime script example

The following example sets fields of the GlideScheduleDateTime type.

```
/sys_sg_write_back_action_item.do?sys_id=539b20d6b72120107be0e34e9e11a971
(function WriteBackAction(parm_input,parm_variable,actionResult) {

	var personalSchedule = new global.FSMMobileUtil().getUserSchedule(parm_variable.user);
	if (gs.nil(personalSchedule)) {
		gs.error("create_event: personal schedule id is not found.");
		gs.addErrorMessage(gs.getMessage("Create Event Failed"));
		return;
	}
	
	if(gs.nil(parm_input.type))
		parm_input.type = "";
	
	var scheduleEntryGR = new GlideRecord("cmn_schedule_span");
	scheduleEntryGR.initialize();
	scheduleEntryGR.setValue("name", parm_input.name);
	
	var start_time = new GlideDateTime(parm_input.start_time);
	scheduleEntryGR.start_date_time = start_time.getDisplayValueInternal();
	
	var end_time = new GlideDateTime(parm_input.end_time);
	scheduleEntryGR.end_date_time = end_time.getDisplayValueInternal();
	
	scheduleEntryGR.setValue("show_as", parm_input.show_as);
	scheduleEntryGR.setValue("type", parm_input.type);
	scheduleEntryGR.setValue("user", parm_variable.user);
	scheduleEntryGR.setValue("schedule", personalSchedule);
	scheduleEntryGR.setValue("repeat_type", parm_input.repeats);
	if(parm_input.repeats!=""){
		scheduleEntryGR.setValue("repeat_count", parm_input.repeat_every);
		scheduleEntryGR.repeat_until = parm_input.repeat_until;
	}
	scheduleEntryGR.insert();
	
	
})(parm_input,parm_variable,actionResult);
```

-   In this example, the `start_date_time` and `end_date_time` fields of a schedule entry are set based on the values of their corresponding date/time inputs of `start_time` and `end_time`.
-   Because the **IncludeTimezone** attribute is set to `true`, the `parm_input.start_time` variable returns a date/time string in the format YYYY-MM-DDThh:mm:ss.sssTZD. To enable the system to handle this date/time format, initialize a `GlideDateTime` object by passing the string into the constructor.
-   Because `start_date_time` and `end_date_time` are not Date Time Columns in the database \(instead, they are Schedule Date/Time columns\), their value are set with `gr.start_date_time = {date_time_value}`.

    **Note:** The `date_time_value` is expected to be in the User Profile Time Zone \(the value provided is expected to be the `Display Value` of a `GlideDateTime`\). This configuration makes it possible to call the GlideDateTime.getDisplayValueInternal\(\) method, which returns a date/time string in the internal format of YYYY-MM-DD hh:mm:ss and in the User Profile Time Zone.



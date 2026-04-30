---
title: Configure the time zone setting for badge and daily log data
description: Add a script include in the Global scope to consider the affected user's time zone when you run a diagnostic request using the badge reader or user daily log data source.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure the time zone setting for badge and daily log data

Add a script include in the Global scope to consider the affected user's time zone when you run a diagnostic request using the badge reader or user daily log data source.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Script Includes**.

2.  Click **New**.

3.  In the **Name** field, enter `TimeZoneUtils`.

4.  From the Accessible from list, select **All application scopes**.

5.  Copy the following script into the **Script** field.

    ```
    var TimeZoneUtils = Class.create();
    TimeZoneUtils.prototype = {
    	initialize: function() {
    	},
    	getTimeZone: function(timeZoneString) {
    		return Packages.java.util.TimeZone.getTimeZone(timeZoneString);
    	},
    	getTimeZoneOffSet: function(timeZoneString, gdt) {
    		var timeZoneObj = this.getTimeZone(timeZoneString);
    		var dateTime = new GlideDateTime();
    		if (gdt) {
    			dateTime.setValue(gdt);
    		}
    		dateTime.setTZ(timeZoneObj);
    		return dateTime.getTZOffset();
    	},
    	getBoundaryDates: function(timeZoneString, offset, dateTime) {
    		var tz = this.getTimeZone(timeZoneString);
    		var gd = new GlideDateTime();
    		gd.setValue(dateTime);
    		gd.add(offset);
    		var startTime = '00:00:00';
    		var endTime = '23:59:59';
    		var actualDate = new GlideDate();
    		actualDate.setValue(gd.getValue());		
    		var startDateTime = new GlideDateTime();
    		startDateTime.setTZ(tz);
    		startDateTime.setDisplayValueInternal(actualDate + ' ' + startTime);
    		var endDateTime = new GlideDateTime();
    		endDateTime.setTZ(tz);
    		endDateTime.setDisplayValueInternal(actualDate + ' ' + endTime);
    		return {
    			startDateTime: startDateTime,
    			endDateTime: endDateTime
    		};
    	},
    	type: 'TimeZoneUtils'
    };
    ```

6.  Click **Submit**.


## Result

The script is used when you run the diagnostic request using the badge reader or user daily log data source. These data sources identify the potentially exposed users who might have come in contact with an affected user. The script considers the affected user's time zone while calculating the date and time from the badge swipe data or daily log data.

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)


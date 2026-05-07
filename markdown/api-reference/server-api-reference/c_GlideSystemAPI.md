---
title: GlideSystem - Global
description: The GlideSystem API, which is referred to by the variable name gs in any server-side JavaScript, provides a number of convenient methods to get information about the system, the current logged in user, and date/time information.Adds an error message for the current session.Displays a high priority message at the top of the form.Adds an info message for the current session.Displays a low priority message at the top of the form.Adds a message for the current session.Displays a moderate priority message at the top of the form.Displays a message confirming a successful action at the top of the form.Gets the date and time for the beginning of last month in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of last week in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of next week in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of next month in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of next year in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of the current month in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of the current quarter in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of this week in the user's session time zone as a UTC timestamp.Returns the date and time for the beginning of this year in the user's session time zone as a UTC timestamp.Retrieves the date and time for the beginning of today in the user's session time zone as a UTC timestamp.Retrieves the \(UTC\) beginning of tomorrow adjusted for the timezone of the user's current session.Retrieves the date and time for the beginning of yesterday in the user's session time zone as a UTC timestamp.Calculate the difference between two dates using the default calendar.Calculates the difference between two dates.Generates a date and time for the specified date in the user's session time zone as a UTC timestamp.Returns a date and time for a certain number of days ago. Returned in the user's session time zone as a UTC timestamp.Returns a date and time for the end of the day a specified number of days ago. Returns the value in the user's session time zone as a UTC timestamp.Returns the date and time of the beginning of the day for the specified number of days ago. The returned date and time reflect the time zone of the current session \(local time\).Returns a date and time for the beginning of the day a specified number of days ago. Returned in the user's session time zone as a UTC timestamp.Returns the date and time for the end of last month in the user's session time zone as a UTC timestamp.Returns the date and time for the end of last week in the user's session time zone as a UTC timestamp.Returns the date and time for the end of last year in the user's session time zone as a UTC timestamp.Returns the date and time for the end of next month in the user's session time zone as a UTC timestamp.Returns the date and time for the end of next week in the user's session time zone as a UTC timestamp.Returns the date and time for the end of next year in the user's session time zone as a UTC timestamp.Returns the date and time for the end of this month in the user's session time zone as a UTC timestamp.Returns the date and time for the end of this quarter in the user's session time zone as a UTC timestamp..Returns the date and time for the end of this week in the user's session time zone as a UTC timestamp.Returns the date and time for the end of this year in the user's session time zone as a UTC timestamp.Retrieves the date and time for the end of today in the user's session time zone as a UTC timestamp.Retrieves the date and time for the end of tomorrow in the user's session time zone as a UTC timestamp.Gets the date and time for the end of yesterday in the user's session time zone as a UTC timestamp.Queues an event for the event manager.Queues an event for the event manager at a specified date and time.Clears session messages saved using addErrorMessage\(\) or addInfoMessage\(\).Returns the file path to the user's avatar.Returns the name of the current application scope.Returns the date format associated with the current user.Returns the date and time format associated with the current user.Retrieves the display column for the table.Returns the display value for a specified field on a specified record.Returns the list of error messages for the session that were added by addErrorMessage\(\).Retrieves the property and escapes it for XML parsing.Returns the display name of the impersonating user.Returns the name of the impersonating user or null if not impersonating.Retrieves the list of info messages for the session that were added by addInfoMessage\(\).Returns the user's initials.Retrieves translated messages from the Message \[sys\_ui\_message\] table to display in a UI.Retrieves translated messages to display in the UI and escapes all ticks \('\).Translates the specified message into the specified language.Returns the node name for the specified index.Returns the node value for the specified index.Returns the specified user preference.Returns the value of a Glide property. If the property is not found, returns the specified alt value.Returns the script error found in the specified script, if there is one.Returns a GlideSession object.Returns the GlideSession session ID.Returns the style defined for the table, field, and field value.Returns the time format associated with the current user.Returns a reference to the user object for the current user.Gets the display name of the current user.Returns the sys\_id of the current user.Returns the user name of the current user.Returns the user display name based on a provided user login name.Constructs an array of all the nodes and values in an XML document.Returns the XML text for the first element in the XML string that matches the XPath query.Determines if the current user has at least one of the passed-in roles.Determines if the current user has the specified role within a specified group.Returns a date and time for the specified number of hours ago. The returned value is adjusted for the time zone of the instance.Returns a date and time for the end of the hour for the specified number of hours ago. The returned value is adjusted for the time zone of the instance.Returns a date and time for the start of the hour for the specified number of hours ago. The returned value is adjusted for the time zone of the instance.Checks whether the date in the specified date object is the first day of the month.Checks whether the date in the specified date object is the first day of the week. This method uses the ISO standard of Monday being the first day of the week.Checks whether the date in the specified date object is the first day of the year.Checks if the current session is interactive.Checks whether the date in the specified date object is the last day of the month.Checks whether the date in the specified date object is the last day of the week. This method uses the ISO standard of Sunday being the last day of the week.Checks whether the date in the specified date object is the last day of the year.Determines if the current user is currently logged in.Determines whether the request came from a mobile device.Returns the date and time one week ago in the user's session time zone as a UTC timestamp.Logs a message to the system log and saves it to the syslog table.Logs an error to the system log and saves it to the syslog table.Logs a warning to the system log and saves it to the syslog table.Returns a date and time for the specified number of minutes ago.Returns a date and time for the end of the minute a certain number of minutes ago. Returned in the user's session time zone as a UTC timestamp.Returns a date and time for the start of the minute a certain number of minutes ago. Returned in the user's session time zone as a UTC timestamp.Returns a date and time for a certain number of months ago in the user's session time zone as a UTC timestamp.Returns the date and time for the last day of the month a specified number of months ago.Returns a date and time for the start of the month a certain number of months ago. Returned in the user's session time zone as a UTC timestamp.Queries an object and returns true if the object is null or contains an empty string.Returns the current date in UTC.Returns the current date and time in UTC format.Returns the current date and time in the user-defined format.Gets a GlideDateTime object with the current date and time in the user's session time zone as a UTC timestamp.Writes a message to the system log.Returns a date and time for a certain number of quarters ago in the user's session time zone as a UTC timestamp.Returns a date and time for the last day of the quarter, for a specified number of quarters ago. Returned in the user's session time zone as a UTC timestamp.Returns a date and time for the first day of the quarter, for a specified number of quarters ago. Returned in the user's session time zone as a UTC timestamp.Sets the specified key to the specified value.Sets the redirect URI for this transaction, which then determines the next page the user will see.Sets the return URI for this transaction. This determines what page the user will be directed to when they return from the next form.Determines if a database table exists in the ServiceNow instance.Returns the sys\_id of the user associated with this session. Use getUserID\(\) instead.Deletes any open scheduled job records in the Schedule \(sys\_trigger\) table for the specified GlideRecord.Gets a date and time for a certain number of years ago in the user's session time zone as a UTC timestamp.Returns yesterday's time \(24 hours ago\) in the user's session time zone as a UTC timestamp.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 63
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSystem- Global

The GlideSystem API, which is referred to by the variable name `gs` in any server-side JavaScript, provides a number of convenient methods to get information about the system, the current logged in user, and date/time information.

Many of the GlideSystem methods facilitate the easy inclusion of dates in query ranges, and are most often used in filters and reporting.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSystem - addErrorMessage\(Object message\)

Adds an error message for the current session.

Use getErrorMessages\(\) to retrieve a list of error messages currently being shown.

|Name|Type|Description|
|----|----|-----------|
|message|Object|The message to add.|

|Type|Description|
|----|-----------|
|void| |

```
gs.include("PrototypeServer");
  var ValidatePasswordStronger = Class.create();
  ValidatePasswordStronger.prototype = {
       process : function() {
          var user_password = request.getParameter("user_password");
          var min_len = 8;
          var rules = "Password must be at least " + min_len + 
             " characters long and contain a digit, an uppercase letter, and a lowercase letter.";
          if (user_password.length() < min_len) {
             gs.addErrorMessage("TOO SHORT: " + rules);
             return false;
          }
          var digit_pattern = new RegExp("[0-9]", "g");
          if (!digit_pattern.test(user_password)) {
             gs.addErrorMessage("DIGIT MISSING: " + rules);
             return false;
          }
          var upper_pattern = new RegExp("[A-Z]", "g");
          if (!upper_pattern.test(user_password)) {
             gs.addErrorMessage("UPPERCASE MISSING: " + rules);
             return false;
          }
          var lower_pattern = new RegExp("[a-z]", "g");
          if (!lower_pattern.test(user_password)) {
             gs.addErrorMessage("LOWERCASE MISSING: " + rules);
             return false;
          }
          return true; // password is OK
       }
  }
[edit]
```

### Scoped equivalent

To use the addErrorMessage\(\) method in a scoped application, use the corresponding scoped method: [addErrorMessage\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - addHighMessage\(String message\)

Displays a high priority message at the top of the form.

|Name|Type|Description|
|----|----|-----------|
|message|String|High priority message to display.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to display a high priority message at the top of the form.

```
gs.addHighMessage("This is a high priority message");
```

## GlideSystem - addInfoMessage\(Object message\)

Adds an info message for the current session.

Use getInfoMessages\(\) to retrieve the list of info messages being shown. This method is not supported for asynchronous business rules and cannot be used within transform scripts.

|Name|Type|Description|
|----|----|-----------|
|message|Object|The message to add.|

|Type|Description|
|----|-----------|
|void| |

```
if ((!current.u_date1.nil()) && (!current.u_date2.nil())) {
  var start = current.u_date1.getGlideObject().getNumericValue();
  var end = current.u_date2.getGlideObject().getNumericValue();
  if (start > end) {
    gs.addInfoMessage('start must be before end');
    current.u_date1.setError('start must be before end');
    current.setAbortAction(true);
  }
}
```

### Scoped equivalent

To use the addInfoMessage\(\) method in a scoped application, use the corresponding scoped method: [addInfoMessage\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - addLowMessage\(String message\)

Displays a low priority message at the top of the form.

|Name|Type|Description|
|----|----|-----------|
|message|String|Low priority message to display.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to display a low priority message at the top of the form.

```
gs.addLowMessage("This is a low priority message");
```

## GlideSystem - addMessage\(String type, Object message\)

Adds a message for the current session.

|Name|Type|Description|
|----|----|-----------|
|type|String|Type of message, such as `error` or `info`.|
|message|Object|Message to add to the current session.|

|Type|Description|
|----|-----------|
|void| |

## GlideSystem - addModerateMessage\(String message\)

Displays a moderate priority message at the top of the form.

|Name|Type|Description|
|----|----|-----------|
|message|String|Moderate message to display.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to display a moderate priority message at the top of the form.

```
gs.addModerateMessage("This is a moderate priority message");
```

## GlideSystem - addSuccessMessage\(String message\)

Displays a message confirming a successful action at the top of the form.

|Name|Type|Description|
|----|----|-----------|
|message|String|Success message to display.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to display a message confirming a success message at the top of the form.

```
gs.addSuccessMessage("This is a success message");
```

## GlideSystem - beginningOfLastMonth\(\)

Gets the date and time for the beginning of last month in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The UTC beginning of last month, in the format yyyy-mm-dd hh:mm:ss.|

This example sets the date and time of the GlideDateTime object to the beginning of last month.

```
var date = new GlideDate();
date.setValue(gs.beginningOfLastMonth());
var dateasint = date.toString().replace('-','');
gs.print(dateasint);
```

### Scoped equivalent

To use the beginningOfLastMonth\(\) method in a scoped application, use the corresponding scoped method: [beginningOfLastMonth\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfLastWeek\(\)

Returns the date and time for the beginning of last week in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ogp_m5v_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of last week. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of last week.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfLastWeek());
```

### Scoped equivalent

To use the beginningOfLastWeek\(\) method in a scoped application, use the corresponding scoped method: [beginningOfLastWeek\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfNextWeek\(\)

Returns the date and time for the beginning of next week in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_i2f_v5v_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of next week. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of next week.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfNextWeek());
```

### Scoped equivalent

To use the beginningOfNextWeek\(\) method in a scoped application, use the corresponding scoped method: [beginningOfNextWeek\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfNextMonth\(\)

Returns the date and time for the beginning of next month in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qp1_dvv_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of next month. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of next month.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfNextMonth());
```

### Scoped equivalent

To use the beginningOfNextMonth\(\) method in a scoped application, use the corresponding scoped method: [beginningOfNextMonth\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfNextYear\(\)

Returns the date and time for the beginning of next year in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The UTC beginning of next year, in the format yyyy-mm-dd hh:mm:ss.|

This example sets the value of the current Glide date/time record to the beginning of next year.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfNextYear());
```

### Scoped equivalent

To use the beginningOfNextYear\(\) method in a scoped application, use the corresponding scoped method: [beginningOfNextYear\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfThisMonth\(\)

Returns the date and time for the beginning of the current month in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_nkk_tvv_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of the current month. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of this month.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfThisMonth());
```

### Scoped equivalent

To use the beginningOfThisMonth\(\) method in a scoped application, use the corresponding scoped method: [beginningOfThisMonth\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfThisQuarter\(\)

Returns the date and time for the beginning of the current quarter in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_us5_1wv_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of the current quarter. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of the current quarter.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfThisQuarter());
```

### Scoped equivalent

To use the beginningOfThisQuarter\(\) method in a scoped application, use the corresponding scoped method: [beginningOfThisQuarter\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfThisWeek\(\)

Returns the date and time for the beginning of this week in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bmj_3wv_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of the current week. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of the current week.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfThisWeek());
```

### Scoped equivalent

To use the beginningOfThisWeek\(\) method in a scoped application, use the corresponding scoped method: [beginningOfThisWeek\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfThisYear\(\)

Returns the date and time for the beginning of this year in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_psd_5wv_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of the current year. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of the current year.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfThisYear());
```

### Scoped equivalent

To use the beginningOfThisYear\(\) method in a scoped application, use the corresponding scoped method: [beginningOfThisYear\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - beginningOfToday\(\)

Retrieves the date and time for the beginning of today in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wgl_bxv_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of the current day. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example sets the value of the current Glide date/time record to the beginning of the current day.

```
var gdt2 = new GlideDateTime(dt);
gdt2.setValue(gs.beginningOfToday());
```

## GlideSystem - beginningOfTomorrow\(\)

Retrieves the \(UTC\) beginning of tomorrow adjusted for the timezone of the user's current session.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wgl_bxv_dm" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC beginning of tomorrow. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>```
var today = new GlideDateTime(gs.beginningOfTomorrow()).getNumericValue();
```

## GlideSystem - beginningOfYesterday\(\)

Retrieves the date and time for the beginning of yesterday in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The UTC beginning of yesterday, in the format yyyy-mm-dd hh:mm:ss.|

```
var start = new GlideDateTime();
start.setValue(gs.beginningOfYesterday());
```

## GlideSystem - calDateDiff\(String startDate, String endDate, Boolean numericValue\)

Calculate the difference between two dates using the default calendar.

Calendars are now legacy. If Schedules are being used, see the 'Calculate during a given schedule' section of the topic [Scheduling script use cases](../../../../../script/useful-scripts/concept/c_UsefulSchedulingScripts.md#).

<table id="table_ulx_gyv_mt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

startDate

</td><td>

String

</td><td>

Starting date to compare in the current user's date format.

</td></tr><tr><td>

endDate

</td><td>

String

</td><td>

Ending date to compare in the current user's date format.

</td></tr><tr><td>

numericValue

</td><td>

Boolean

</td><td>

Flag that indicates ther format of the returned time value.Valid values:

 -   true: Return value is formatted in number of seconds
-   false: Return value is formatted ddd hh:mm:ss.

</td></tr></tbody>
</table><table id="table_vlx_gyv_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

If the **numericValue** parameter is true, returns the difference between the two dates as an integer number of seconds.If false, returns the difference between the two dates in the format ddd hh:mm:ss.

</td></tr></tbody>
</table>```
var endDateTime = gs.nowDateTime();
gs.print('--- Total records: ' + countRecordsTotal);
gs.print('--- End time: ' + endDateTime);
gs.print('Time diff: ' + gs.calDateDiff(startDateTime, endDateTime));
```

## GlideSystem - dateDiff\(String startDate, String endDate, Boolean numericValue\)

Calculates the difference between two dates.

This method expects the earlier date as the first parameter and the later date as the second parameter; otherwise, the method returns the difference as a negative value. Use getDisplayValue\(\) to convert the strings to the expected format.

This method expects parameters in the user/system date time format, which may not be the same as the internal format. Using parameters in formats other than the user/system date time format may return invalid results.

If you are working with GlideDateTime objects use the GlideDateTime subtract\(\) method instead of dateDiff\(\).

|Name|Type|Description|
|----|----|-----------|
|startDate|String|The starting date to compare in the current user's date format.|
|endDate|String|The ending date to compare in the current user's date format.|
|numericValue|Boolean|If true, the return value will be formatted in number of seconds; if false the return value will be formatted ddd hh:mm:ss.|

|Type|Description|
|----|-----------|
|String|If the numericValue parameter is true, returns the difference between the two dates as an integer number of seconds; if false, returns the difference between the two dates in the format ddd hh:mm:ss.|

```
// Given two date/times as DateTime objects
// Set the values this way to ensure a consistent input time
var date1 = new GlideDateTime();
var date2 = new GlideDateTime();
date1.setDisplayValueInternal('2014-01-01 12:00:00');
date2.setDisplayValueInternal('2014-01-01 13:00:00');
 
// Determine the difference as number of seconds (returns a string)
// Use getDisplayValue() to convert the string to the format expected by dateDiff()
var diffSeconds = gs.dateDiff(date1.getDisplayValue(), date2.getDisplayValue(), true);
 
// JavaScript will coerce diffSeconds from a string to a number
// since diffSeconds is being compared to a number
var msg = (diffSeconds <= 0) ? ' is on or after ' : ' is before ';
gs.print(date1.getDisplayValue() + msg + date2.getDisplayValue())
```

## GlideSystem - dateGenerate\(String date, String range\)

Generates a date and time for the specified date in the user's session time zone as a UTC timestamp.

<table id="table_ghf_3jw_mt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

date

</td><td>

String

</td><td>

Date to generate in UTC.Format: yyyy-mm-dd

</td></tr><tr><td>

range

</td><td>

String

</td><td>

Start, end, or a time. Format: 24-hour hh:mm:ss

</td></tr></tbody>
</table><table id="table_hhf_3jw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Generated date and time. If the range is `start`, the returned value is yyyy-mm-dd 00:00:00.

If range is `end` the return value is yyyy-mm-dd 23:59:59.

Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows using dateGenerate\(\) to set the start date when querying records in the Incident table.

```
var tableData = new GlideRecord('incident');
tableData.addEncodedQuery("sys_created_onBETWEENjavascript:gs.dateGenerate('2015-10-07','00:00:00')@javascript:gs.daysAgoEnd(0)^priority=1^severityIN1,2");
tableData.query();
gs.info("Count: " + tableData.getRowCount());
```

Output:

```
Count: 7
```

### Scoped equivalent

To use the dateGenerate\(\) method in a scoped application, use the corresponding scoped method: [dateGenerate\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - daysAgo\(Number days\)

Returns a date and time for a certain number of days ago. Returned in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|days|Number|Number of days|

<table id="table_wlc_zjw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC of the specified number of days ago. Format: yyyy-mm-dd hh:mm:ss.

</td></tr></tbody>
</table>```
function contractNoticeDue() {
  var now_GR = new GlideRecord("contract");
  now_GR.addQuery("u_contract_status", "Active");
  now_GR.query();
  while (now_GR.next()) {
    if ((now_GR.u_termination_date <= gs.daysAgo(-90)) && (now_GR.u_contract_duration == "Long")) {
      now_GR.u_contract_status = "In review";
    } 
    else if ((now_GR.u_termination_date <= gs.daysAgo(-50)) && (now_GR.u_contract_duration == "Medium")) {
      now-GR.u_contract_status = "In review";
    }
    else if ((now_GR.u_termination_date <= gs.daysAgo(-10)) && (now_GR.u_contract_duration == "Short")) {
      now_GR.u_contract_status = "In review";
    }
  }
  now_GR.update();
}
```

### Scoped equivalent

To use the daysAgo\(\) method in a scoped application, use the corresponding scoped method: [daysAgo\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - daysAgoEnd\(Number days\)

Returns a date and time for the end of the day a specified number of days ago. Returns the value in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|days|Number|Integer number of days|

|Type|Description|
|----|-----------|
|String|The UTC end of the day in the format yyyy-mm-dd hh:mm:ss.|

This example shows using daysAgoEnd\(\) to set the end date when querying records in the Incident table.

```
var tableData = new GlideRecord('incident');
tableData.addEncodedQuery("sys_created_onBETWEENjavascript:gs.dateGenerate('2015-10-07','00:00:00')@javascript:gs.daysAgoEnd(0)^priority=1^severityIN1,2");
tableData.query();
gs.addInfoMessage("Count: " +tableData.getRowCount());
```

### Scoped equivalent

To use the daysAgoEnd\(\) method in a scoped application, use the corresponding scoped method: [daysAgoEnd\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - daysAgoLocal\(Number days\)

Returns the date and time of the beginning of the day for the specified number of days ago. The returned date and time reflect the time zone of the current session \(local time\).

|Name|Type|Description|
|----|----|-----------|
|days|Number|Number of days ago|

|Type|Description|
|----|-----------|
|String|Local date and time for the beginning of the day in the user-defined date time format. If the date time format is not modified from its initial value the format is yyyy-mm-dd hh:mm:ss.|

```
if (due_in == "1 Day") {
  dd = gs.daysAgoLocal(-1);
}
if (due_in == "1 Week") {
  dd = gs.daysAgoLocal(-7);
}
```

## GlideSystem - daysAgoStart\(Number days\)

Returns a date and time for the beginning of the day a specified number of days ago. Returned in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|days|String|Integer number of days|

|Type|Description|
|----|-----------|
|String|UTC start of the day in the format yyyy-mm-dd hh:mm:ss|

```
var now_GR = new GlideRecord('sysapproval_approver');
now_GR.addQuery('state', 'requested');
now_GR.addQuery('sys_updated_on', '<', gs.daysAgoStart(5));
now_GR.query();
```

### Scoped equivalent

To use the daysAgoStart\(\) method in a scoped application, use the corresponding scoped method: [daysAgoStart\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfLastMonth\(\)

Returns the date and time for the end of last month in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ff1_jlw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC of the end of last month. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to query a report record from the last day of last month.

```
var month = gs.endOfLastMonth();
var monthd = new GlideDateTime(month);
monthd.addDays(-1);

var queueLast = new GlideRecord('u_amazon_connect_phone_metrics');
queueMtd.addQuery('u_queue_name',queueNames[i]);
queueMtd.addEncodedQuery('u_time_range=MTD');
queueMtd.addEncodedQuery('u_report_date'+ monthd);
queueMtd.orderByDesc('u_report_date');
        
queueMtd.query();

if(queueMtd.next()){
  gs.info(queueMtd.u_report_date);
} 
```

### Scoped equivalent

To use the endOfLastMonth\(\) method in a scoped application, use the corresponding scoped method: [endOfLastMonth\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfLastWeek\(\)

Returns the date and time for the end of last week in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_nth_qlw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC end of last week. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to query records opened on the last week of the previous month.

```
var inc = new GlideRecord('incident');
inc.addQuery('active=true^priority=1^opened_atONLast month@javascript:gs.beginningOfLastMonth()@javascript:gs.endOfLastMonth()^opened_atONLast week@javascript:gs.beginningOfLastWeek()@javascript:gs.endOfLastWeek()');
inc.query();
while(inc.next())
 {
   gs.addInfoMessage(inc.getRowCount());
 }
```

### Scoped equivalent

To use the endOfLastWeek\(\) method in a scoped application, use the corresponding scoped method: [endOfLastWeek\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfLastYear\(\)

Returns the date and time for the end of last year in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|UTC in format yyyy-mm-dd hh:mm:ss.|

This example shows how to query records created for all records created in the last year.

```
var inc = new GlideRecord('incident');
inc.addEncodedQuery('sys_created_onONLast year@javascript:gs.beginningOfLastYear()@javascript:gs.endOfLastYear()');
inc.query();
while(inc.next()){
  inc.assignment_group = "d625dccec0a8016700a222a0f7900d06";
  inc.update();
}
```

### Scoped equivalent

To use the endOfLastYear\(\) method in a scoped application, use the corresponding scoped method: [endOfLastYear\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfNextMonth\(\)

Returns the date and time for the end of next month in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_dpz_xww_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC data and time. Format yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to query KB knowledge records created since the beginning of today until the end of next month.

```
var query = "kb_knowledge_base=e81c9a0ddbc15810c38f0763b99619c1^ORkb_knowledge_base=21302e89db055810c38f0763b99619cc^valid_toBETWEENjavascript:gs.beginningOfToday()@javascript:gs.endOfNextMonth()^ORworkflow_state=pending_retirement^latest=true";
var rec = new GlideRecord('kb_knowledge');
rec.addEncodedQuery(query);
rec.addQuery('author', current.author);
rec.query();
while (rec.next()) {
  var Kbtitle = rec.getValue('short_description');
  articles.push(rec.number.toString()+ '' + Kbtitle);
  template.print('Click here to view record<a href="https://give urs instance url here/nav_to.do?uri=kb_knowledge.do?sys_id=' + rec.sys_id + '">' + rec.number + '</a>');
}
var articlesList = "<ul>";
for (i = 0; i <= articles.length-1; i++) {
  articlesList = articlesList + "<li>" + articles[i] + "</li>";
}
articlesList = articlesList + "</ul>";
```

### Scoped equivalent

To use the endOfNextMonth\(\) method in a scoped application, use the corresponding scoped method: [endOfNextMonth\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfNextWeek\(\)

Returns the date and time for the end of next week in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_d2q_kxw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of next week.Format yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to use endOfNextWeek\(\) in a query to obtain all visitors in the past week.

```
var title = 'Visitors arriving this Week';
var visitorQuery = 'active=true^category=visitor_request^u_my_start_dateONThis week@javascript:gs.beginningOfThisWeek()@javascript:gs.endOfNextWeek()';
```

### Scoped equivalent

To use the endOfNextWeek\(\) method in a scoped application, use the corresponding scoped method: [endOfNextWeek\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfNextYear\(\)

Returns the date and time for the end of next year in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_v3w_rxw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of next year.Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to use endOfNextYear\(\) to set the GlideDateTime object to the end of next year.

```
setEndDate : function(dt) {
  var gdt2 = new GlideDateTime(dt);
  gdt2.setValue(gs.endOfNextYear());
}
```

### Scoped equivalent

To use the endOfNextYear\(\) method in a scoped application, use the corresponding scoped method: [endOfNextYear\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfThisMonth\(\)

Returns the date and time for the end of this month in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_cky_lyw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of this month. Format yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to use endOfThisMonth\(\) to set the GlideDateTime object to the end of the current month.

```
setEndDate : function(dt) {
  var gdt2 = new GlideDateTime(dt);
  gdt2.setValue(gs.endOfThisMonth());
}
```

### Scoped equivalent

To use the endOfThisMonth\(\) method in a scoped application, use the corresponding scoped method: [endOfThisMonth\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfThisQuarter\(\)

Returns the date and time for the end of this quarter in the user's session time zone as a UTC timestamp..

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_jjn_5yw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of this quarter. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to use endOfThisQuarter\(\) to set the GlideDateTime object to the end of the current month.

```
setEndDate : function(dt) {
  var gdt2 = new GlideDateTime(dt);
  gdt2.setValue(gs.endOfThisQuarter());
}
```

### Scoped equivalent

To use the endOfThisQuarter\(\) method in a scoped application, use the corresponding scoped method: [endOfThisQuarter\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfThisWeek\(\)

Returns the date and time for the end of this week in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_kqb_czw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of this week. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to use endOfThisWeek\(\) to set the GlideDateTime object to the end of the current month.

```
setEndDate : function(dt) {
  var gdt2 = new GlideDateTime(dt);
  gdt2.setValue(gs.endOfThisWeek());
}
```

### Scoped equivalent

To use the endOfThisWeek\(\) method in a scoped application, use the corresponding scoped method: [endOfThisWeek\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfThisYear\(\)

Returns the date and time for the end of this year in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_byg_4zw_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of this year.Format yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to use endOfThisYear\(\) to set the GlideDateTime object to the end of the current month.

```
setEndDate : function(dt) {
  var gdt2 = new GlideDateTime(dt);
  gdt2.setValue(gs.endOfThisYear());
}
```

### Scoped equivalent

To use the endOfThisYear\(\) method in a scoped application, use the corresponding scoped method: [endOfThisYear\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - endOfToday\(\)

Retrieves the date and time for the end of today in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|UTC in the format yyyy-mm-dd hh:mm:ss.|

```
var beginToday = gs.beginningOfToday(); 
        var endToday = gs.endOfToday(); 
        var beginTomorrow = gs.beginningOfTomorrow(); 
        var endTomorrow = gs.endOfTomorrow(); 
        var beginYesterday = gs.beginningOfYesterday(); 
        var endYesterday = gs.endOfYesterday(); 
        
        gs.info('beginningOfToday: ' + beginToday); 
        gs.info('endOfToday: ' + endToday); 
        gs.info('-----------'); 
        gs.info('beginningOfTomorrow: ' + beginTomorrow); 
        gs.info('endOfTomorrow: ' + endTomorrow); 
        gs.info('beginningOfYesterday: ' + beginYesterday); 
        gs.info('endOfYesterday: ' + endYesterday); 
        gs.info('-----------'); 
        var gdt1 = new GlideDateTime(beginToday); 
        var gdt2 = new GlideDateTime(beginTomorrow); 
        var dur = GlideDateTime.subtract(gdt1, gdt2); //the difference between gdt1 and gdt2 
        gs.info('BeginTomorrow: ' + dur.getDisplayValue()); 
        
        var gdt1 = new GlideDateTime(endToday); 
        var gdt2 = new GlideDateTime(endTomorrow); 
        var dur = GlideDateTime.subtract(gdt1, gdt2); //the difference between gdt1 and gdt2 
        gs.info('EndTomorrow: ' + dur.getDisplayValue()); 
        
        var gdt1 = new GlideDateTime(beginToday); 
        var gdt2 = new GlideDateTime(beginYesterday); 
        var dur = GlideDateTime.subtract(gdt2, gdt1); //the difference between gdt1 and gdt2 
        gs.info('BeginningYesterday: ' + dur.getDisplayValue()); 
        
        var gdt1 = new GlideDateTime(endToday); 
        var gdt2 = new GlideDateTime(endYesterday); 
        var dur = GlideDateTime.subtract(gdt2, gdt1); //the difference between gdt1 and gdt2 
        gs.info('EndYesterday: ' + dur.getDisplayValue());
```

## GlideSystem - endOfTomorrow\(\)

Retrieves the date and time for the end of tomorrow in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|UTC in the format yyyy-mm-dd hh:mm:ss.|

```
var tomorrowEnd = new GlideDateTime();
tomorrowEnd.setValue(gs.endOfTomorrow());
```

## GlideSystem - endOfYesterday\(\)

Gets the date and time for the end of yesterday in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|UTC in the format \(yyyy-mm-dd huh:mm:ss\).|

```
var yesterdayEnd = new GlideDateTime();
yesterdayEnd.setValue(gs.endOfYesterday());
```

## GlideSystem - eventQueue\(String name, Object glideRecord, String parm1, String parm2, String queue\)

Queues an event for the event manager.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the event being queued.|
|glideRecord|Object|GlideRecord object, such as "current".|
|parm1|String|\(Optional\) Saved with the instance if specified.|
|parm2|String|\(Optional\) Saved with the instance if specified.|
|queue|String|Name of the queue.|

|Type|Description|
|----|-----------|
|void| |

```
if (current.operation() != 'insert' && current.comments.changes()) {
    gs.eventQueue("incident.commented", current, gs.getUserID(), gs.getUserName());
}
```

### Scoped equivalent

To use the eventQueue\(\) method in a scoped application, use the corresponding scoped method: [eventQueue\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - eventQueueScheduled\(String name, Object glideRecord, String parm1, String parm2, Object expiration\)

Queues an event for the event manager at a specified date and time.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the event being queued.|
|glideRecord|Object|GlideRecord object, such as "current".|
|parm1|String|\(Optional\) Saved with the instance if specified.|
|parm2|String|\(Optional\) Saved with the instance if specified.|
|expiration|Object|Date and time to process this event.|

|Type|Description|
|----|-----------|
|void| |

```
if (current.operation() != 'insert' && current.comments.changes()) {
    gs.eventQueueScheduled("incident.commented", current, gs.getUserID(), gs.getUserName(), new GlideDateTime('2018-06-02 20:00:00'));
}
```

### Scoped equivalent

To use the eventQueueScheduled\(\) method in a scoped application, use the corresponding scoped method: [eventQueueScheduled\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - flushMessages\(\)

Clears session messages saved using addErrorMessage\(\) or addInfoMessage\(\).

Session messages are shown at the top of the form. In client side scripts, use g\_form.clearMessages\(\) to remove session messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to parse through and pass back error messages and then clears the messages using flushMessages\(\).

```
MySessionUtil.getSessionError = function() {
  var msg = null;
  var msgs = gs.getErrorMessages().toArray();
  if (msgs.length > 0) {
    msg = msgs[0] + '';
    gs.flushMessages();
  }
  return msg;
};

```

## GlideSystem - getAvatar\(\)

Returns the file path to the user's avatar.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The file path to the user's avatar.|

```
var avatarFile = gs.getUser().getAvatar();        
gs.addInfoMessage('User avatar ID: ' + avatarFile);
```

Output:

```
User avatar ID: c148e1d13741310042106710ce41f149.iix?t=small
```

## GlideSystem - getCurrentScopeName\(\)

Returns the name of the current application scope.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current scope name.|

This example shows how to use getCurrentScopeName\(\) to get the scope of the processor.

```
var incident_GR = new GlideRecord('Incident');

if (incident_GR.get("2e3f6baddb9ad600added8fdbf9618cb")) {
  gs.debug("processor scope = "+ gs.getCurrentScopeName());
  var w = new global.Workflow();
  var context = w.startFlow('1f4a4baddb9ad600affed8fdbf9619bc', incident_GR, "update");   //id = id workflow
}
```

### Scoped equivalent

To use the getCurrentScopeName\(\) method in a scoped application, use the corresponding scoped method: [getCurrentScopeName\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getDateFormat\(\)

Returns the date format associated with the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The date format associated with the current user.|

The following example returns the date format associated with the user.

```
var userDateFormat = gs. getDateFormat();
gs.info(userDateFormat);

```

Output:

```
yyyy-MM-dd
```

## GlideSystem - getDateTimeFormat\(\)

Returns the date and time format associated with the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The date and time format associated with the current user.|

The following example returns the format of the date and time that is associated with the user.

```
var userDateTimeFormat = gs.getDateTimeFormat();
gs.info(userDateTimeFormat);

```

Output:

```
yyyy-MM-dd HH:mm:ss
```

## GlideSystem - getDisplayColumn\(String tableName\)

Retrieves the display column for the table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table from which to get the display column name.|

|Type|Description|
|----|-----------|
|String|Display column name|

```
// Return the sys_id value for a given table and its display value
function GetIDValue(table, displayValue) { 
    var rec = new GlideRecord(table);
    var dn = gs.getDisplayColumn(table);
    if (rec.get(dn, displayValue))
        return rec.sys_id;
    else
        return null;
}
```

## GlideSystem - getDisplayValueFor\(String tableName, String recordID, String fieldName\)

Returns the display value for a specified field on a specified record.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table.|
|recordID|String|Sys\_id for the record.|
|fieldName|String|Name of the field whose display value to return.|

|Type|Description|
|----|-----------|
|String|Display value for the field.|

This example shows how to use getDisplayValueFor\(\) to return the display value of the *number* field.

```
var value = gs.getDisplayValueFor(current.getTableName(),current.getValue('sys_id'),'number');

```

## GlideSystem - getErrorMessages\(\)

Returns the list of error messages for the session that were added by addErrorMessage\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|List of error messages|

This example shows how to parse through and pass back error messages using getErrorMessages\(\).

```
MySessionUtil.getSessionError = function() {
  var msg = null;
  var msgs = gs.getErrorMessages().toArray();
  if (msgs.length > 0) {
    msg = msgs[0] + '';
    gs.flushMessages();
  }
  return msg;
};

```

### Scoped equivalent

To use the getErrorMessages\(\) method in a scoped application, use the corresponding scoped method: [getErrorMessages\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getEscapedProperty\(String key, Object substituteObject\)

Retrieves the property and escapes it for XML parsing.

|Name|Type|Description|
|----|----|-----------|
|key|String|Key for the property whose value should be returned.|
|substituteObject|Object|Optional. Object to return if the property is not found.|

|Type|Description|
|----|-----------|
|String|Property, or the substituteObject if the property is not found.|

```
var propValue = gs.getEscapedProperty("com.example.my_test_property");
gs.addInfoMessage("This is my property value " + propValue);
```

## GlideSystem - getImpersonatingUserDisplayName\(\)

Returns the display name of the impersonating user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display name of the impersonating user.|

This example shows how to obtain the impersonator's user display name.

```
var user = gs.getUserDisplayName();
gs.print ("The current user display name is: " + user);

var name = gs.getImpersonatingUserDisplayName(); 
gs.print("Impersonating user display name: " + name);
```

Output:

```
The current user display name is: abel.tuter
Impersonating user display name: admin
```

## GlideSystem - getImpersonatingUserName\(\)

Returns the name of the impersonating user or null if not impersonating.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of impersonating user|

This example shows how to obtain the impersonator's user name.

```
var name = gs.getImpersonatingUserName();
var actual_user = null;
if (name == null || name == '')
  actual_user = user;
else
  actual_user = Packages.com.glide.sys.User.getUser(name);

var recent_impersonations = actual_user.getPreference('recent.impersonations');
var admin_role=actual_user.hasRole("admin");
```

## GlideSystem - getInfoMessages\(\)

Retrieves the list of info messages for the session that were added by addInfoMessage\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|List of info messages.|

This example shows how to obtain the information messages.

```
var messages = gs.getInfoMessages();
if (messages.toString().indexOf('Conflicts Detected') == -1)
  gs.addInfoMessage(msg);
```

## GlideSystem - getInitials\(\)

Returns the user's initials.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's initials.|

```
var userInitials = gs.getUser().getInitials();        
gs.addInfoMessage('User initials: ' + userInitials);
```

Output:

```
User initials: SA
```

## GlideSystem - getMessage\(String messageID, Object args\)

Retrieves translated messages from the Message \[sys\_ui\_message\] table to display in a UI.

If the specified message identifier \(key\) exists in the Message \[sys\_ui\_message\] table for the current language, the method returns the translated message. If the specified message identifier does not exist for the current language, the method returns the English version of the message. If the message identifier does not exist in the table, then it returns the message ID.

For additional information about the Message table, see [Message table](https://www.servicenow.com/docs/access?context=r_MessageTable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** If the UI message has a tick \('\), there may be issues with the message in the script; to escape the ticks \('\), use getMessageS\(String, Object\).

<table id="table_czl_5j5_lt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

messageID

</td><td>

String

</td><td>

Message identifier. You can locate this value in the Key field of the Message \[sys\_ui\_message\] table. Note the Key field may look exactly like the actual message string.

</td></tr><tr><td>

args

</td><td>

Object

</td><td>

Optional. List of strings or other values defined by java.text.MessageFormat that replace the variables within the specified message. For example: `gs.getMessage("Abort adding action '{0}', same subflow can't be added twice in this subflow.", current.action.name);`

 In this example *'\{0\}'* is replaced with the content of *current.action.name*.

 **Note:** The passed in values are not translated. They are inserted verbatim in the message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Requested UI message.|

This example shows the message returned for the current user when Spanish is the current language.

```
var my_message = gs.getMessage("rows will not be updated");
alert(my_message);
```

Output:

```
las filas no se actualizarán
```

This example shows how to replace a single variable within a message.

```
// current.action.name is "update record"
var my_message = gs.getMessage("Abort adding action '{0}', same subflow can't be added twice in this subflow.", current.action.name);
alert(my_message);
```

Output:

```
Abort adding action update record, same subflow can't be added twice in this subflow.
```

This example shows how to replace multiple variables within a message.

```
// current.sub_flow.name is 'schedule users'
// current.action.name is "update record"
var my_message = gs.getMessage("Abort adding action '{0}', same subflow can't be added twice in {1} subflow.", [current.action.name, current.sub_flow.name]);
alert(my_message);
```

Output:

```
Abort adding action update record, same subflow can't be added twice in schedule users subflow.
```

### Scoped equivalent

To use the getMessage\(\) method in a scoped application, use the corresponding scoped method: [getMessage\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getMessageS\(String messageID, Object args\)

Retrieves translated messages to display in the UI and escapes all ticks \('\).

If the specified message identifier \(key\) exists in the Message \[sys\_ui\_message\] table for the current language, the method returns the translated message. If the specified message identifier does not exist for the current language, the method returns the English version of the message. If the message identifier does not exist in the table, then it returns the message ID.

For additional information about the Message table, see [Message table](https://www.servicenow.com/docs/access?context=r_MessageTable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Useful if you are inserting into a JavaScript expression from Jelly.

<table id="table_gyt_xk5_lt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MessageID

</td><td>

String

</td><td>

Message identifier. You can locate this value in the Key field of the Message \[sys\_ui\_message\] table. Note the Key field may look exactly like the actual message string.

</td></tr><tr><td>

args

</td><td>

Object

</td><td>

Optional. List of strings or other values defined by java.text.MessageFormat that replace the variables within the specified message. For example: `gs.getMessage("Abort adding action '{0}', same subflow can't be added twice in this subflow.", current.action.name);`

 In this example *'\{0\}'* is replaced with the content of *current.action.name*.

 **Note:** The passed in values are not translated. They are inserted verbatim in the message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Specified message with ticks escaped.|

```
/*
"I love France" translates to "J'aime la France" in French.
Rendering this without escaping the tick in "J'aime" would break Jelly, because 
the tick would prematurely end the variable assignment, and everything that 
follows (aime la France') would be a jelly syntax error.
*/
var my_message = '${gs.getMessageS("I love France")}'; 
alert(my_message);
```

Output:

```
J'aime la France
```

## GlideSystem - getMessageLang\(String message, String language, Array args\)

Translates the specified message into the specified language.

You can also embed variables in the passed message. The method resolves those variables with the values passed in the **args** array.

<table id="table_m4v_3tl_zyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

String

</td><td>

Message to translate.

</td></tr><tr><td>

language

</td><td>

String

</td><td>

Language in which to translate the message.Format: BCP 47 standard

</td></tr><tr><td>

args

</td><td>

Array

</td><td>

Optional. List of strings or other values defined by java.text.MessageFormat that replace the variables within the specified message. For example: `gs.getMessageLang("Abort adding action '{0}', same subflow can't be added twice in this subflow.", current.action.name);`

In this example *'\{0\}'* is replaced with the content of *current.action.name*.

**Note:** The passed in values are not translated. They are inserted verbatim in the message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Translated message.|

The following example transforms the specified message into Spanish.

```
var my_message = gs.getMessageLang("New email", "es");
gs.info(my_message);
```

Output:

```
Nuevo correo electrónico
```

The following example shows how to replace variables within a message.

```
var my_message = gs.getMessageLang("There are {0} new emails for {1}", "es", [current.numEmails, current.userName]);
gs.info(my_message);
```

Output:

```
Hay 7 correos nuevos para John Smith
```

## GlideSystem - getNodeName\(Object obj, Number index\)

Returns the node name for the specified index.

|Name|Type|Description|
|----|----|-----------|
|obj|Object|Object to examine.|
|index|Number|Index from which to obtain the node name.|

|Type|Description|
|----|-----------|
|String|Node's name|

```
function doInsert(nodeList) {
  gs.print('Doing insert');
  var task = new GlideRecord('task');
  task.initialize();
  for (var x=0; x < nodeList.size(); x++) {
    var name = gs.getNodeName(nodeList, x);
    var value = gs.getNodeValue(nodeList, x);
    task.setValue(name, value);
  }
  task.insert();
}
```

## GlideSystem - getNodeValue\(Object obj, Number index\)

Returns the node value for the specified index.

|Name|Type|Description|
|----|----|-----------|
|obj|Object|Object to examine.|
|index|Number|Index from which to get the node valu.e|

|Type|Description|
|----|-----------|
|Object|Node value|

```
function doInsert(nodeList) {
  gs.print('Doing insert');
  var task = new GlideRecord('task');
  task.initialize();
  for (var x=0; x < nodeList.size(); x++) {
    var name = gs.getNodeName(nodeList, x);
    var value = gs.getNodeValue(nodeList, x);
    task.setValue(name, value);
  }
  task.insert();
}
```

## GlideSystem - getPreference\(String key, Object default\)

Returns the specified user preference.

|Name|Type|Description|
|----|----|-----------|
|key|String|Key for the preference.|
|default|Object|Default value to use if the specified preference is not found.|

|Type|Description|
|----|-----------|
|String|Preference value. If no preference, returns the specified default value.|

```
function getSelectedProject() {
  var array= new Array();
  var prj_id = gs.getPreference("prj_id"); //This will fetch value from user preference
  var gr = new GlideRecord('pm_project_task');
  gr.addQuery('parent', prj_id);
  gr.addActiveQuery();
  while(gr.next()) {
    array.push(gr.sys_id.toString());
  }
  return array;
}
```

## GlideSystem - getProperty\(String key, Object alt\)

Returns the value of a Glide property. If the property is not found, returns the specified **alt** value.

|Name|Type|Description|
|----|----|-----------|
|key|String|Key for the property whose value should be returned.|
|alt|Object|Optional. Alternate object to return if the property is not found.|

|Type|Description|
|----|-----------|
|String|Value of the Glide property, or the alternate object defined above.|

```
//Check for attachments and add link if there are any
var attachment_link = '';
var rec = new GlideRecord('sc_req_item');
rec.addQuery('sys_id', current.request_item);
rec.query();
if(rec.next()){
  if(rec.hasAttachments()){
    attachment_link = gs.getProperty('glide.servlet.uri') + rec.getLink();
  }   
}
```

## GlideSystem - getScriptError\(String script\)

Returns the script error found in the specified script, if there is one.

**Note:** The script is not executed by this function, it is only checked for syntax errors.

|Name|Type|Description|
|----|----|-----------|
|script|String|Script to check for errors.|

|Type|Description|
|----|-----------|
|String|Error message. Null if there is no error.|

```
if (gs.isValidScript(current.script) == false)
  {
    current.setAbortAction(true);
    var error = gs.getScriptError(current.script);
    current.script.setError(error);
  }
```

## GlideSystem - getSession\(\)

Returns a GlideSession object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideSession Object|GlideSession object for the current session|

```
if(!gs.hasRole("admin") && gs.getSession().isInteractive() && gs.getUserName() != "guest"){
  var qc = current.addQuery('u_visibility', "both");
  qc.addOrCondition('u_visibility', '');
  if (gs.getImpersonatingUserName() != null) {
    gs.getSession().clearClientData('navQuery');
  }
  var navQuery = gs.getSession().getClientData('navQuery');
  if (navQuery == null) {
    var isManager = gs.getUser().getRecord().getValue('u_is_manager');
      if (!isManager) {
        qc.addOrCondition('u_visibility', 'nonmanager');
        gs.getSession().putClientData('navQuery', 'nonmanager');
      } else {
        qc.addOrCondition('u_visibility', 'manager');
        gs.getSession().putClientData('navQuery', 'manager');
        }
  } else {
  qc.addOrCondition('u_visibility', navQuery);
  }   
}
```

### Scoped equivalent

To use the getSession\(\) method in a scoped application, use the corresponding scoped method: [getSession\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getSessionID\(\)

Returns the GlideSession session ID.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Session ID|

```
var gr_NOW = new GlideRecord('v_user_session');
var sessionId = gs.getSessionID();
gs.log("Session ID is: " + sessionId);
```

Output

```
Session ID is: FEE589B3DB7EE4103DD9C39D139619D7
```

### Scoped equivalent

To use the getSessionID\(\) method in a scoped application, use the corresponding scoped method: [getSessionID](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getStyle\(String tableName, String fieldName, String fieldValue\)

Returns the style defined for the table, field, and field value.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Table name|
|fieldName|String|Field name|
|fieldValue|String|Field value|

|Type|Description|
|----|-----------|
|String|Style of the specified field.|

```
var returnString = gs.getStyle('<tableName>', '<fieldName>', '<fieldValue>');
gs.print(returnString);
```

## GlideSystem - getTimeFormat\(\)

Returns the time format associated with the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Time format associated with the current user.|

The following code example shows how to call this method.

```
var userTimeFormat = gs. getTimeFormat();
gs.info(userTimeFormat);

```

Output:

```
HH:mm:ss
```

## GlideSystem - getUser\(\)

Returns a reference to the user object for the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideUser|Reference to a user object for the current user.|

The following example shows how to get the current user object.

```
var user = gs.getUser();
gs.print ("The current user is: " + user);
```

Output:

```
The current user is: com.glide.sys.User@db5dd9
```

The following example shows how to check whether the current user has the workflow\_admin role.

```
var role = gs.getUser().hasRole('workflow_admin');
gs.print ("Does the current user have the workflow_admin role: " + role);
```

Output:

```
Does the current user have the workflow_admin role: true
```

### Scoped equivalent

To use the getUser\(\) method in a scoped application, use the corresponding scoped method: [getUser\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getUserDisplayName\(\)

Gets the display name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_nvv_vjb_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The name field of the current user. For example, this method returns Abel Tuter as opposed to abel.tuter.

</td></tr></tbody>
</table>This example gets the current user's display name.

```
gs.info(gs.getUserDisplayName());
```

Output:

```
System Administrator
```

### Scoped equivalent

To use the getUserDisplayName\(\) method in a scoped application, use the corresponding scoped method: [getUserDisplayName\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getUserID\(\)

Returns the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current user.|

This example gets the current user's sys\_id.

```
var currentUserId = gs.getUserID();
gs.print("Current user ID: " + currentUserId);
```

Output:

```
Current user ID: 6816f79cc0a8016401c5a33be04be441
```

### Scoped equivalent

To use the getUserID\(\) method in a scoped application, use the corresponding scoped method: [getUserID\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getUserName\(\)

Returns the user name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bpf_plb_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The user name of the current user.For example, this method returns abel.tuter as opposed to Abel Tuter.

</td></tr></tbody>
</table>This example gets the user name of the current user and an impersonated user.

```
var user = gs.getUserName();
gs.info("The current user name is: " + user);

var impUser = new GlideImpersonate();
impUser.impersonate("62826bf03710200044e0bfc8bcbe5df1");
var user2 = gs.getUserName();
gs.info("The impersonated user name is: " + user2);
```

Output:

```
The current user name is: admin
The impersonated user name is: abel.tuter
```

### Scoped equivalent

To use the getUserName\(\) method in a scoped application, use the corresponding scoped method: [getUserName\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - getUserNameByUserID\(String user\_id\)

Returns the user display name based on a provided user login name.

|Name|Type|Description|
|----|----|-----------|
|user\_id|String|Login name of the user from which to retrieve the associated display name.|

<table id="table_pp4_1mb_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Display name of the requested user.**Note:** If this method can't find a user with the requested ID, it returns the input value provided.

</td></tr></tbody>
</table>The following example shows how to get the specified user's display name.

```
var displayName = gs.getUserNameByUserID('abel.tuter');
gs.info('User display name is: ' + displayName);
```

Output:

```
User display name is: Abel Tuter
```

## GlideSystem - getXMLNodeList\(String xml\)

Constructs an array of all the nodes and values in an XML document.

|Name|Type|Description|
|----|----|-----------|
|xml|String|XML document to parse.|

|Type|Description|
|----|-----------|
|Array list|List of names and values of the outer most XML node.|

The following example shows how to get a list of XML nodes and their associated values in an array list.

```
var nodeList = gs.getXMLNodeList("<note><to>Tove</to><from>Jani</from><heading>Reminder</heading><body>Don't forget me this weekend!</body></note>");
gs.print ("The node contains: " + nodeList);

```

Output:

```
The node contains: [to : Tove, from : Jani, heading : Reminder, body : Don't forget me this weekend!]

```

## GlideSystem - getXMLText\(String xml, String xpathQuery\)

Returns the XML text for the first element in the XML string that matches the XPath query.

|Name|Type|Description|
|----|----|-----------|
|xml|String|XML string to search.|
|xpathQuery|String|XPath query to match.|

|Type|Description|
|----|-----------|
|String|XML node matching the search parameters.|

The following example shows how to get the value of a specified XML element within a passed-in node.

```
var nodeList = gs.getXMLText("<outer><note><to>Tove</to><from>Jani</from><heading>Reminder</heading><body>Don't forget me this weekend!</body></note></outer>", "//from");
gs.print ("The from element contains: " + nodeList);
```

Output:

```
The from element contains: Jani
```

## GlideSystem - hasRole\(String roleName\)

Determines if the current user has at least one of the passed-in roles.

|Name|Type|Description|
|----|----|-----------|
|roleName|String|Comma-separated list of roles.|

<table id="table_cyk_5nb_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user has at least one of the specified roles.Possible values:

-   true: User has at least one of the passed-in roles. Also returns true if the user has the administrator role.
-   false: User does not have any of the passed-in roles.

</td></tr></tbody>
</table>The following example shows how to check whether the current user has the admin or groups\_admin role.

```
if (!gs.hasRole("admin, groups_admin") && gs.getSession().isInteractive()) {
  var qc = current.addQuery("u_hidden", "!=", "true"); //cannot see hidden groups... 
  qc.addOrCondition("sys_id", "javascript:getMyGroups()"); //...unless in the hidden group
}
```

### Scoped equivalent

To use the hasRole\(\) method in a scoped application, use the corresponding scoped method: [hasRole\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - hasRoleInGroup\(Object roleName, Object group\)

Determines if the current user has the specified role within a specified group.

|Name|Type|Description|
|----|----|-----------|
|roleName|Object|Name of the role.|
|group|Object|Sys\_id of the group to check for the specified role.|

<table id="table_eys_m4b_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user has the specified role in the specified group.Possible values:

-   true: The logged-in user is assigned to the specified role in the specified group.
-   false: The logged-in user is not assigned to the specified role in the specified group.

</td></tr></tbody>
</table>The following example shows how to check whether the sys\_user\_group group has the role\_name role.

```
var group = new GlideRecord('sys_user_group');
group.addQuery('name', 'GROUP_NAME');
group.setLimit(1);
group.query();
if (group.next()) {
   if (gs.hasRoleInGroup('role_name', group)) {
      gs.print('User has role in group');  
   } else {
      gs.print('User does NOT have role in group');
   }  
}
```

## GlideSystem - hoursAgo\(Number hours\)

Returns a date and time for the specified number of hours ago. The returned value is adjusted for the time zone of the instance.

|Name|Type|Description|
|----|----|-----------|
|hours|Number|Number of hours ago.|

<table id="table_wrq_j1x_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the specified number of hours ago. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>```
var currentDateTime = gs.hoursAgo(0);
gs.info("Current date/time: " + currentDateTime);

var agoDateTime = gs.hoursAgo(1);
gs.info("Ago date/time: " + agoDateTime);
```

Output

```
Current date/time: 2021-03-17 20:53:25
Ago date/time: 2021-03-17 19:53:25
```

### Scoped equivalent

To use the hoursAgo\(\) method in a scoped application, use the corresponding scoped method: [hoursAgo\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - hoursAgoEnd\(Number hours\)

Returns a date and time for the end of the hour for the specified number of hours ago. The returned value is adjusted for the time zone of the instance.

|Name|Type|Description|
|----|----|-----------|
|hours|Number \(Integer\)|Number of hours ago.|

<table id="table_edc_v1x_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of the specified number of hours ago. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>```
var currentDateTime = gs.hoursAgoEnd(0);
gs.print("Current date/time: " + currentDateTime);

var agoDateTime = gs.hoursAgoEnd(1);
gs.print("Ago date/time: " + agoDateTime);
```

Output

```
Current date/time: 2021-03-17 20:59:59
Ago date/time: 2021-03-17 19:59:59
```

### Scoped equivalent

To use the hoursAgoEnd\(\) method in a scoped application, use the corresponding scoped method: [hoursAgoEnd\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - hoursAgoStart\(Number hours\)

Returns a date and time for the start of the hour for the specified number of hours ago. The returned value is adjusted for the time zone of the instance.

|Name|Type|Description|
|----|----|-----------|
|hours|Number|Number of hours ago.|

<table id="table_xwb_xbx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the end of the specified number of hours ago. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>```
var currentDateTime = gs.hoursAgoStart(0);
gs.print("Current date/time: " + currentDateTime);

var agoDateTime = gs.hoursAgoStart(1);
gs.print("Ago date/time: " + agoDateTime);
```

Output

```
Current date/time: 2021-03-17 20:00:00
Ago date/time: 2021-03-17 19:00:00
```

### Scoped equivalent

To use the hoursAgoStart\(\) method in a scoped application, use the corresponding scoped method: [hoursAgoStart\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - isFirstDayOfMonth\(Object date\)

Checks whether the date in the specified date object is the first day of the month.

|Name|Type|Description|
|----|----|-----------|
|date|Object|Date object on which to check the date, such as GlideDateTime or GlideDate.|

<table id="table_qyc_x3x_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the date in the specified date object is the first day of the month.Possible values:

-   true: First day of the month.
-   false: Not the first day of the month.

</td></tr></tbody>
</table>This example show how to determine whether the date in the specified date object is the first day of the month.

```
var gdt = new GlideDateTime();
gdt.setValue('2021-04-01 12:00:00');
var currentDay = gs.isFirstDayOfMonth(gdt);
gs.print("First day of month: " + currentDay);

gdt.setValue('2021-04-21 12:00:00');
var currentDay = gs.isFirstDayOfMonth(gdt);
gs.print("First day of month: " + currentDay);
```

Output

```
First day of month: true
First day of month: false
```

## GlideSystem - isFirstDayOfWeek\(Object date\)

Checks whether the date in the specified date object is the first day of the week. This method uses the ISO standard of Monday being the first day of the week.

|Name|Type|Description|
|----|----|-----------|
|date|Object|Date object on which to check the date, such as GlideDateTime or GlideDate.|

<table id="table_ew2_hjx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the date in the current date object is the first day of the week \(Monday\).Possible values:

-   true: First day of the week.
-   false: Not the first day of the week.

</td></tr></tbody>
</table>This example show how to determine whether the date in the specified date object is the first day of the week.

```
var gdt = new GlideDateTime();
gdt.setValue('2021-03-02 12:00:00');
var currentDay = gs.isFirstDayOfWeek(gdt);
gs.info("First day of week: " + currentDay);

gdt.setValue('2021-03-22 12:00:00');
var currentDay = gs.isFirstDayOfWeek(gdt);
gs.info("First day of week: " + currentDay);
```

Output

```
First day of week: false
First day of week: true
```

## GlideSystem - isFirstDayOfYear\(Object date\)

Checks whether the date in the specified date object is the first day of the year.

|Name|Type|Description|
|----|----|-----------|
|date|Object|Date object on which to check the date, such as GlideDateTime or GlideDate.|

<table id="table_vrv_sjx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the date in the specified date object is the first day of the year.Possible values:

-   true: First day of the year.
-   false: Not the first day of the year.

</td></tr></tbody>
</table>This example show how to determine whether the date in the specified date object is the first day of the year.

```
var gdt = new GlideDateTime();
gdt.setValue('2020-12-31 12:00:00');
var currentDay = gs.isFirstDayOfYear(gdt);
gs.info("First day of year: " + currentDay);

gdt.setValue('2021-01-01 12:00:00');
var currentDay = gs.isFirstDayOfYear(gdt);
gs.info("First day of year: " + currentDay);
```

Output

```
First day of year: false
First day of year: true
```

## GlideSystem - isInteractive\(\)

Checks if the current session is interactive.

An example of an interactive session is when a user logs in using the log-in screen. An example of a non-interactive session is using a SOAP request to retrieve data.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_cc5_kpb_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the session is interactive.Possible values:

-   true: Session is interactive.
-   false: Session is not interactive.

</td></tr></tbody>
</table>```
if (!gs.hasRole('admin') && gs.isInteractive()) {
  var qc1 = current.addQuery('u_group', '');
  var gra = new GlideRecord('sys_user_grmember');
  gra.addQuery('user', gs.getUserID());
  gra.query();
  while (gra.next()) {
    qc1.addOrCondition('u_group', gra.group);
  }
}
```

### Scoped equivalent

To use the isInteractive\(\) method in a scoped application, use the corresponding scoped method: [isInteractive\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - isLastDayofMonth\(Object date\)

Checks whether the date in the specified date object is the last day of the month.

|Name|Type|Description|
|----|----|-----------|
|date|Object|Date object on which to check the date, such as GlideDateTime or GlideDate.|

<table id="table_h2y_ckx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the date in the specified date object is the last day of the month.Possible values:

-   true: Last day of the month.
-   false: Not the last day of the month.

</td></tr></tbody>
</table>This example show how to determine whether the date in the specified date object is the last day of the month.

```
var gdt = new GlideDate();
gdt.setValue('2020-12-31 12:00:00');
var currentDay = gs.isLastDayOfMonth(gdt);
gs.print("First day of year: " + currentDay);

gdt.setValue('2021-01-01 12:00:00');
var currentDay = gs.isLastDayOfMonth(gdt);
gs.print("First day of year: " + currentDay);
```

Output

```
Last day of month: true
Last day of month: false
```

## GlideSystem - isLastDayOfWeek\(Object date\)

Checks whether the date in the specified date object is the last day of the week. This method uses the ISO standard of Sunday being the last day of the week.

|Name|Type|Description|
|----|----|-----------|
|date|Object|Date object on which to check the date, such as GlideDateTime or GlideDate.|

<table id="table_e55_nkx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the date in the current date object is the last day of the week \(Sunday\).Possible values:

-   true: Last day of the week.
-   false: Not the last day of the week.

</td></tr></tbody>
</table>This example show how to determine whether the date in the specified date object is the last day of the week.

```
var gdt = new GlideDate();
gdt.setValue('2021-03-01 12:00:00');
var currentDay = gs.isLastDayOfWeek(gdt);
gs.info("Last day of week: " + currentDay);

gdt.setValue('2021-03-21 12:00:00');
var currentDay = gs.isLastDayOfWeek(gdt);
gs.info("Last day of week: " + currentDay);
```

Output

```
First day of week: false
First day of week: true
```

## GlideSystem - isLastDayOfYear\(Object date\)

Checks whether the date in the specified date object is the last day of the year.

|Name|Type|Description|
|----|----|-----------|
|date|Object|Date object on which to check the date, such as GlideDateTime or GlideDate.|

<table id="table_d2t_xkx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the date in the current date object is the last day of the year.Possible values:

-   true: Last day of the year.
-   false: Not the last day of the year.

</td></tr></tbody>
</table>This example show how to determine whether the date in the specified date object is the last day of the year.

```
var gdt = new GlideDateTime();
gdt.setValue('2020-12-31 12:00:00');
var currentDay = gs.isLastDayOfYear(gdt);
gs.info("Last day of year: " + currentDay);

gdt.setValue('2021-01-01 12:00:00');
var currentDay = gs.isLastDayOfYear(gdt);
gs.info("Last day of year: " + currentDay);
```

Output

```
Last day of year: true
Last day of year: false
```

## GlideSystem - isLoggedIn\(\)

Determines if the current user is currently logged in.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_kdh_5pb_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user is logged in.Possible values:

-   true: User is logged in.
-   false: User is not logged in.

</td></tr></tbody>
</table>This example show how to determine whether the current user is logged in.

```
if(gs.isLoggedIn())
  gs.info("Current user is logged in");
else
  gs.info("Current user is NOT logged in");
```

Output

```
Current user is logged in
```

### Scoped equivalent

To use the isLoggedIn\(\) method in a scoped application, use the corresponding scoped method: [isLoggedIn\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - isMobile\(\)

Determines whether the request came from a mobile device.

You can use this method in UI action conditions and business rules.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hnw_lbz_bv" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the request came from a mobile device.Possible values:

-   true: Mobile device.
-   false: Non-mobile device.

</td></tr></tbody>
</table>This example show how to determine whether the current device is a mobile device.

```
if(gs.isMobile())
    gs.info("Submitted from mobile UI");
  else 
   gs.info("NOT submitted from mobile UI");
```

Output

```
Submitted from mobile UI
```

### Scoped equivalent

To use the isMobile\(\) method in a scoped application, use the corresponding scoped method: [isMobile\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - lastWeek\(\)

Returns the date and time one week ago in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_usk_mcx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date and time one week ago. Format: \(UTC\) yyyy-MM-dd hh:mm:ss

</td></tr></tbody>
</table>This example show how to obtain the date that is one week from the date in the current date object.

```
var gdt = new GlideDateTime();
gdt.setValue('2021-03-22 01:00:00');

gs.info("Current date: " + gs.nowDateTime());

gs.info("One week earlier: " + gs.lastWeek());
```

Output

```
Current date: 2021-03-22 15:27:07
One week earlier: 2021-03-15 15:27:07
```

## GlideSystem - log\(String message, String source\)

Logs a message to the system log and saves it to the syslog table.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message to log.|
|source|String|Optional. Source of the message.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to post a log entry using constants and variables.

```
var count = new GlideAggregate('incident');
count.addQuery('active', 'true');
count.addAggregate('COUNT', 'category');
count.query();   
while (count.next()) {
   var category = count.category;
   var categoryCount = count.getAggregate('COUNT', 'category');
   gs.log("The are currently " + categoryCount + " incidents with a category of " + category, "Incident Counter");
}
```

## GlideSystem - logError\(String message, String source\)

Logs an error to the system log and saves it to the syslog table.

|Name|Type|Description|
|----|----|-----------|
|message|String|Error message to log.|
|source|String|Optional. Source of the message.|

|Type|Description|
|----|-----------|
|void| |

The following example logs an error if the Incident table cannot be found.

```
var gr_NOW = new GlideRecord("incident");
if (!gr_NOW.isValid()) {
  gs.logError('Incident table could not be found');
  return;
}
```

## GlideSystem - logWarning\(String message, String source\)

Logs a warning to the system log and saves it to the syslog table.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message to log.|
|source|String|Optional. Source of the message.|

|Type|Description|
|----|-----------|
|void| |

The following example logs a warning if the Incident table cannot be found.

```
var gr_NOW = new GlideRecord("incident");
if (!gr_NOW.isValid()) {
  gs.logWarning('Incident table could not be found');
  return;
}
```

## GlideSystem - minutesAgo\(Number minutes\)

Returns a date and time for the specified number of minutes ago.

|Name|Type|Description|
|----|----|-----------|
|minutes|Number|Number of minutes in the past to return.|

<table id="table_hnh_vcx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC date and time for the specified number of minutes ago. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>This example shows how to use the minutesAgo\(\) method in an addQuery\(\) call.

```
// Check to see if the user has failed to login too many times
// when the limit is reached, lock the user out of the system
//
//Check failed logins in the last 15 minutes
var now_GR = new GlideRecord('sysevent');
now_GR.addQuery('name', 'login.failed');
now_GR.addQuery('parm1', event.parm1.toString());
now_GR.addQuery('sys_created_on','>=', gs.minutesAgo(15));
now_GR.query();
var rowCount = now_GR.getRowCount();
if(rowCount >= 5){
  var now_GR = new GlideRecord("sys_user");
  now_GR.addQuery("user_name", event.parm1.toString());
  now_GR.query();
  if (now_GR.next()) {
    now_GR.locked_out = true;
    now_GR.update();
    gs.log("User " + event.parm1 + " locked out due to too many invalid login attempts");
  }
}
```

## GlideSystem - minutesAgoEnd\(Number minutes\)

Returns a date and time for the end of the minute a certain number of minutes ago. Returned in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|minutes|Number|Integer number of minutes ago, such as 5 or 11.|

<table id="table_gp2_hdx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC the specified number of minutes ago, at the end of the minute \(59 seconds\). Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time 30 minutes ago at the end of the minute in UTC.

```
var nowDateTime = new GlideDateTime();
gs.print("Now: " + nowDateTime);
var thirtyMinutesAgoDateTime = gs.minutesAgoEnd(30);
gs.print("Thirty minutes ago end time: " + thirtyMinutesAgoDateTime);
```

Output:

```
Now: 2021-10-20 15:22:13
Thirty minutes ago end time: 2021-10-20 14:52:59
```

### Scoped equivalent

To use the minutesAgoEnd\(\) method in a scoped application, use the corresponding scoped method: [minutesAgoEnd\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - minutesAgoStart\(Number minutes\)

Returns a date and time for the start of the minute a certain number of minutes ago. Returned in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|minutes|Number|Integer number of minutes ago, such as 15 or 112.|

<table id="table_yzm_tdx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC the specified number of minutes ago, at the start of the minute. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time 30 minutes ago at the start of the minute in UTC.

```
var nowDateTime = new GlideDateTime();
gs.info("Now: " + nowDateTime);
var thirtyMinutesAgoDateTime = gs.minutesAgoStart(30);
gs.info("Thirty minutes ago: " + thirtyMinutesAgoDateTime);
```

Output:

```
Now: 2021-10-20 14:56:18
Thirty minutes ago: 2021-10-20 14:26:00
```

### Scoped equivalent

To use the minutesAgoStart\(\) method in a scoped application, use the corresponding scoped method: [minutesAgoStart\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - monthsAgo\(Number months\)

Returns a date and time for a certain number of months ago in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|months|Number|Integer number of months ago.|

<table id="table_qhw_f2x_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC of the specified number of months ago at the exact same time.Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time one month ago at the same time in UTC.

```
var nowDateTime = new GlideDateTime();
gs.info("Now: " + nowDateTime);
var oneMonthAgoDateTime = gs.monthsAgo(1);
gs.info("One month ago: " + oneMonthAgoDateTime);
```

Output:

```
Now: 2021-10-20 15:29:15
One month ago: 2021-09-20 15:29:15
```

### Scoped equivalent

To use the monthsAgo\(\) method in a scoped application, use the corresponding scoped method: [monthsAgo\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - monthsAgoEnd\(Number months\)

Returns the date and time for the last day of the month a specified number of months ago.

|Name|Type|Description|
|----|----|-----------|
|months|Number \(Integer\)|Number of months, such as 4 or 16.|

<table id="table_oqx_r2x_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date and time stamp of the month, the specified number of months ago, in local time. Format: UTC yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time two months ago at the end of the business month.

```
var nowDateTime = new GlideDateTime();
gs.info("Now: " + nowDateTime);
var endOfTheMonthDateTime = gs.monthsAgoEnd(2);
gs.info("End of the month: " + endOfTheMonthDateTime);
```

Output:

```
Now: 2021-10-20 19:23:35
End of the month: 2021-08-01 06:59:59
```

## GlideSystem - monthsAgoStart\(Number months\)

Returns a date and time for the start of the month a certain number of months ago. Returned in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|months|Number|Integer number of months ago, such as 5 or 14.|

<table id="table_ymk_bfx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC start of the month the specified number of months ago.Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time three months ago in UTC.

```
var nowDateTime = new GlideDateTime();
gs.info("Now: " + nowDateTime);
var threeMonthsAgoDateTime = gs.monthsAgoStart(3);
gs.info("Three months ago start date and time: " + threeMonthsAgoDateTime);
```

Output:

```
Now: 2021-10-20 15:05:27
Three months ago start date and time: 2021-07-01 07:00:00
```

### Scoped equivalent

To use the monthsAgoStart\(\) method in a scoped application, use the corresponding scoped method: [monthsAgoStart\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - nil\(Object obj\)

Queries an object and returns true if the object is null or contains an empty string.

|Name|Type|Description|
|----|----|-----------|
|obj|Object|The object to be checked.|

|Type|Description|
|----|-----------|
|Boolean|True if null or empty string; otherwise, false.|

```
if ((!current.u_date1.nil()) && (!current.u_date2.nil())) {
  var start = current.u_date1.getGlideObject().getNumericValue();
  var end = current.u_date2.getGlideObject().getNumericValue();
  if (start > end) {
    gs.addInfoMessage('start must be before end');
    current.u_date1.setError('start must be before end');
    current.setAbortAction(true);
  }
}
```

### Scoped equivalent

To use the nil\(\) method in a scoped application, use the corresponding scoped method: [nil\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - now\(\)

Returns the current date in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current date in the user-defined format, in UTC.|

```
// When the user password changes then set the u_password_last_reset field
// to now so we know when to force another update
 
var now_GR = new GlideRecord("sys_user");
if (now_GR.get(event.parm1.toString())) {
    // Do something based on the Password Changing
    gs.log("The user password changed so do something else...");
    now_GR.u_password_last_reset = gs.now();
    now_GR.update();
}
```

## GlideSystem - nowNoTZ\(\)

Returns the current date and time in UTC format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current UTC date time|

```
// When the user password changes then set the u_password_last_reset field
// to now so we know when to force another update
 
var now_GR = new GlideRecord("sys_user");
if (now_GR.get(event.parm1.toString())) {
    // Do something based on the Password Changing
    gs.log("The user password changed so do something else...");
    now_GR.u_password_last_reset = gs.nowNoTZ();
    now_GR.update();
}
```

## GlideSystem - nowDateTime\(\)

Returns the current date and time in the user-defined format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current date and time in the user-defined format. For more information on setting the system date and time format, see [Date and Date/Time fields](https://www.servicenow.com/docs/access?context=r_UseDateAndTimeFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).|

```
var currentDateTime = gs.nowDateTime();
gs.print("Current date/time: " + currentDateTime);
```

Output

```
Current date/time: 2021-03-17 14:04:02
```

When setting a variable in a workflow script to the current date and time, use the setDisplayValue\(\) method. The following script sets the workflow variable end\_date to the current date and time.

```
current.variables.end_date.setDisplayValue(gs.nowDateTime());
```

## GlideSystem - nowGlideDateTime\(\)

Gets a GlideDateTime object with the current date and time in the user's session time zone as a UTC timestamp.

After you get a GlideDateTime object with the current date and time, you can use the GlideDateTime methods to perform date-time operations, such as performing date-time calculations, formatting a date-time, or converting between date-time formats.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|GlideDateTime object with the current date and time in UTC format.|

Sets the field u\_target\_date to the current date and time in UTC format.

```
current.u_target_date = gs.nowGlideDateTime();
```

## GlideSystem - print\(String message\)

Writes a message to the system log.

This method does not write the message to the syslog table unless debug has been activated.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to log|

|Type|Description|
|----|-----------|
|void| |

```
var rec = new GlideRecord('incident');
rec.addQuery('active',false);
rec.query();
while (rec.next()) { 
 gs.print('Inactive incident ' + rec.number + ' deleted');
 rec.deleteRecord();
}
```

## GlideSystem - quartersAgo\(Number quarters\)

Returns a date and time for a certain number of quarters ago in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|quarters|Number|Integer number of the quarters ago.|

<table id="table_j12_zgx_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

UTC of the quarter that was the specified number of quarters ago. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time four quarters ago at the same time.

```
var nowDateTime = new GlideDateTime();
gs.print("Now: " + nowDateTime);
var fourQuartersAgoDateTime = gs.quartersAgo(4);
gs.print("Four quarters ago: " + fourQuartersAgoDateTime);
```

Output:

```
Now: 2021-10-20 16:27:32
Four quarters ago: 2020-10-20 16:27:32
```

## GlideSystem - quartersAgoEnd\(Number quarters\)

Returns a date and time for the last day of the quarter, for a specified number of quarters ago. Returned in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|quarters|Number|An integer number of quarters|

|Type|Description|
|----|-----------|
|String|UTC end of the quarter that was the specified number of quarters ago, in the format yyyy-mm-dd hh:mm:ss|

### Scoped equivalent

To use the quartersAgoEnd\(\) method in a scoped application, use the corresponding scoped method: [quartersAgoEnd\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - quartersAgoStart\(Number quarters\)

Returns a date and time for the first day of the quarter, for a specified number of quarters ago. Returned in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|quarters|Number|An integer number of quarters|

|Type|Description|
|----|-----------|
|String|UTC end of the month that was the specified number of quarters ago, in the format yyyy-mm-dd hh:mm:ss|

### Scoped equivalent

To use the quartersAgoStart\(\) method in a scoped application, use the corresponding scoped method: [quartersAgoStart\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - setProperty\(String key, String value, String description\)

Sets the specified key to the specified value.

**Note:** Care should be taken when setting system properties \(sys\_properties\) using this method as it causes a system-wide cache flush. Each flush can cause system degradation while the caches rebuild. If a value must be updated often, it should not be stored as a system property. In general, you should only place values in the sys\_properties table that do not frequently change.

|Name|Type|Description|
|----|----|-----------|
|key|String|The key for the property to be set.|
|value|String|The value of the property to be set.|
|description|String|A description of the property.|

|Type|Description|
|----|-----------|
|void| |

```
gs.setProperty("glide.foo","bar","foo");
gs.info(gs.getProperty("glide.foo"));
```

Output: bar

### Scoped equivalent

To use the setProperty\(\) method in a scoped application, use the corresponding scoped method: [setProperty\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - setRedirect\(Object URI\)

Sets the redirect URI for this transaction, which then determines the next page the user will see.

|Name|Type|Description|
|----|----|-----------|
|URI|Object|URI to set as the redirect|

|Type|Description|
|----|-----------|
|void| |

This example redirects the user to a particular catalog item, and passes along the current email as a parameter.

```
gs.setRedirect("com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=d41ce5bac611227a0167f4bf8109bf70&sysparm_user=" 
+ current.sys_id + "&sysparm_email=" + current.email)
```

### Scoped equivalent

To use the setRedirect\(\) method in a scoped application, use the corresponding scoped method: [setRedirect\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - setReturn\(Object URI\)

Sets the return URI for this transaction. This determines what page the user will be directed to when they return from the next form.

|Name|Type|Description|
|----|----|-----------|
|URI|Object|URI to set as the return location.|

|Type|Description|
|----|-----------|
|void| |

This example ensures that the user will be returned to the current page when they are done with the next one.

```
gs.setReturn (current.getLink(true));
```

## GlideSystem - tableExists\(String tableName\)

Determines if a database table exists in the ServiceNow instance.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table to check.|

<table id="table_f3j_gw1_mt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified table exists in the ServiceNow instance.Possible values:

-   true: Table exists
-   false: Table does not exist

</td></tr></tbody>
</table>This example shows checking whether the incident and foo tables exist in the ServiceNow instance.

```
gs.info("Does the incident table exist? " + gs.tableExists("incident"));

gs.info("Does the foo table exist? " + gs.tableExists("foo"));
```

Output

```
Does the incident table exist? true
Does the foo table exist? false
```

### Scoped equivalent

To use the tableExists\(\) method in a scoped application, use the corresponding scoped method: [tableExists\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - userID\(\)

Returns the sys\_id of the user associated with this session. Use getUserID\(\) instead.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current user.|

The following example shows how to unassign all active Incident records assigned to the current user.

```
var incidentGR = new GlideRecord('incident');
incidentGR.addActiveQuery();

// Filter results to incidents assigned to the current user
var currentUserSysId = gs.userID();
incidentGR.addQuery('assigned_to', currentUserSysId);
incidentGR.query();

while (incidentGR.next()) {
    incidentGR.setValue('assigned_to', 'NULL');
    incidentGR.update();
    gs.info(
        'Unassigned Incident: {0}: {1}',
        incidentGR.number.toString(),
        incidentGR.short_description.toString()
    );
}
```

Output:

```
Unassigned Incident: INC0000057: Performance problems with wifi
Unassigned Incident: INC0009001: Unable to post content on a Wiki page
Unassigned Incident: INC0008111: ATF : Test1
```

## GlideSystem - workflowFlush\(Object glideRecord\)

Deletes any open scheduled job records in the Schedule \(sys\_trigger\) table for the specified GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|glideRecord|Object|The GlideRecord|

|Type|Description|
|----|-----------|
|void| |

## GlideSystem - yearsAgo\(Number years\)

Gets a date and time for a certain number of years ago in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|years|Number|An integer number of years|

|Type|Description|
|----|-----------|
|String|UTC beginning of the year that is the specified number of years ago, in the format yyyy-mm-dd hh:mm:ss.|

### Scoped equivalent

To use the yearsAgo\(Number years\) method in a scoped application, use the corresponding scoped method: [yearsAgo\(Number years\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideSystem - yesterday\(\)

Returns yesterday's time \(24 hours ago\) in the user's session time zone as a UTC timestamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|UTC for 24 hours ago, in the format yyyy-mm-dd hh:mm:ss|

### Scoped equivalent

To use the yesterday\(\) method in a scoped application, use the corresponding scoped method: [yesterday\(\)](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).


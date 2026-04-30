---
title: GlideSystem - Scoped
description: The scoped GlideSystem API provides a number of convenient methods to obtain information about the system, the current logged in user, and other system level information.Adds an error message for the current session.Displays a high priority message at the top of the form.Adds an info message for the current session. This method is not supported for asynchronous business rules.Displays a low priority message at the top of the form.Displays a moderate priority message at the top of the form.Displays a message confirming a successful action at the top of the form.Creates a base64 string from the specified string.Returns an ASCII string from the specified base64 string.Returns the date and time for the beginning of last month in GMT.Returns the date and time for the beginning of last week in GMT.Returns the date and time for the beginning of next month in GMT.Returns the date and time for the beginning of next week in GMT.Returns the date and time for the beginning of next year in GMT.Returns the date and time for the beginning of this month in GMT.Returns the date and time for the beginning of this quarter in GMT.Returns the date and time for the beginning of this week in GMT.Returns the date and time for the beginning of this year in GMT.Generates a date and time for the specified date in GMT.Returns the date and time for a specified number of days ago.Returns the date and time for the end of the day a specified number of days ago.Returns the date and time for the beginning of the day a specified number of days ago.Writes a debug message to the system log.Returns the date and time for the end of last month in GMT.Returns the date and time for the end of last week in GMT.Returns the date and time for the end of last year in GMT.Returns the date and time for the end of next month in GMT.Returns the date and time for the end of next week in GMT.Returns the date and time for the end of next year in GMT.Returns the date and time for the end of this month in GMT.Returns the date and time for the end of this quarter in GMT.Returns the date and time for the end of this week in GMT.Returns the date and time for the end of this year in GMT.Writes an error message to the system log.Queues an event for the event manager.Queues an event in the event manager.Executes a job for a scoped application.Generates a GUID that can be used when a unique identifier is required.Gets the caller scope name; returns null if there is no caller.Gets a string representing the cache version for a CSS file.Gets the ID of the current application as set using the Application Picker.Gets the name of the current scope.Returns the date format associated with the current user.Returns the date and time format associated with the current user.Returns the error messages that were added by addErrorMessage\(\) for the session.Retrieves the specified message from the Message \[sys\_ui\_message\] table. If the message has HTML special characters, replaces them with the corresponding HTML name codes. For example, &amp; becomes &amp;amp;.Retrieves translated messages from the Message \[sys\_ui\_message\] table to display in a UI.Gets the value of a Glide property. If the property is not found, returns an alternate value.Gets a reference to the current Glide session.Retrieves the GlideSession session ID.This method is no longer available. Instead, use gs.getSession\(\).getSessionToken\(\).Returns the time format associated with the current user.Returns the name of the time zone associated with the current user.Gets the current URI for the session.Returns a reference to the scoped GlideUser object for the current user.Gets the display name of the current user.Gets the sys\_id of the current user.Returns the user name of the current user.Determines if the current user has the specified role.Returns the date and time for a specified number of hours ago.Returns the date and time for the end of the hour a specified number of hours ago.Returns the date and time for the start of the hour a specified number of hours ago.Provides a safe way to call a script include from the sandbox, allowing only the inclusion of trusted scripts.Writes an info message to the system log.Determines if debugging is active for a specific scope.Checks if the current session is interactive. An example of an interactive session is when a user logs in normally. An example of a non-interactive session is using a SOAP request to retrieve data.Determines if the current user is currently logged in.You can determine if a request comes from a mobile device.Returns the date and time for the end of the minute a specified number of minutes ago.Returns the date and time for the start of the minute a specified number of minutes ago.Returns the date and time for a specified number of months ago.Returns the date and time for the last day of the month a specified number of months ago.Returns the date and time for the start of the month a specified number of months ago.Queries an object and returns true if the object is null, undefined, or contains an empty string.Returns the date and time for the last day of the quarter for a specified number of quarters ago.Returns the date and time for the first day of the quarter for a specified number of quarters ago.Sets the specified key to the specified value if the property is within the script's scope.Sets the redirect URI for this transaction, which then determines the next page the user will see.Determines if a database table exists.Encodes non-ASCII characters, unsafe ASCII characters, and spaces so the returned string can be used on the Internet. Uses UTF-8 encoding. Uses percent \(%\) encoding.Replaces UTF-8 encoded characters with ASCII characters.Writes a warning message to the system log.Takes an XML string and returns a JSON object.Returns a date and time for a certain number of years ago.Returns yesterday's time \(24 hours ago\).
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 31
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSystem- Scoped

The scoped GlideSystem API provides a number of convenient methods to obtain information about the system, the current logged in user, and other system level information.

Many of the GlideSystem methods facilitate the easy inclusion of dates in query ranges, and are most often used in filters and reporting.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideSystem - addErrorMessage\(String message\)

Adds an error message for the current session.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message to add.|

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
```

## Scoped GlideSystem - addHighMessage\(String message\)

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

## Scoped GlideSystem - addInfoMessage\(String message\)

Adds an info message for the current session. This method is not supported for asynchronous business rules.

|Name|Type|Description|
|----|----|-----------|
|message|String|Info message to add.|

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

## Scoped GlideSystem - addLowMessage\(String message\)

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

## Scoped GlideSystem - addModerateMessage\(String message\)

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

## Scoped GlideSystem - addSuccessMessage \(String message\)

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

## Scoped GlideSystem - base64Encode\(String source\)

Creates a base64 string from the specified string.

|Name|Type|Description|
|----|----|-----------|
|source|String|String to encode.|

|Type|Description|
|----|-----------|
|String|Encoded base64 string.|

The following code example shows how to call this method.

```
var mac = new CertificateEncryption;
var key = "sample_key"; 
key = gs.base64Encode(key);
mac.generateMac(key, "HmacSHA256", "sample_data");
```

## Scoped GlideSystem - base64Decode\(String source\)

Returns an ASCII string from the specified base64 string.

|Name|Type|Description|
|----|----|-----------|
|source|String|A base64 encoded string.|

|Type|Description|
|----|-----------|
|String|The decoded string.|

## Scoped GlideSystem - beginningOfLastMonth\(\)

Returns the date and time for the beginning of last month in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of last month, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - beginningOfLastWeek\(\)

Returns the date and time for the beginning of last week in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of last week, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - beginningOfNextMonth\(\)

Returns the date and time for the beginning of next month in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of next month, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - beginningOfNextWeek\(\)

Returns the date and time for the beginning of next week in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The GMT beginning of next week, in the format yyyy-mm-dd hh:mm:ss.|

## Scoped GlideSystem - beginningOfNextYear\(\)

Returns the date and time for the beginning of next year in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of next year, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - beginningOfThisMonth\(\)

Returns the date and time for the beginning of this month in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of this month, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - beginningOfThisQuarter\(\)

Returns the date and time for the beginning of this quarter in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of this quarter, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - beginningOfThisWeek\(\)

Returns the date and time for the beginning of this week in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of this week, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - beginningOfThisYear\(\)

Returns the date and time for the beginning of this year in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT beginning of this year, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - dateGenerate\(String date, String range\)

Generates a date and time for the specified date in GMT.

<table id="table_mhc_ljn_zv" class="parameters"><thead><tr><th>

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

Date to generate the GMT for.Format: yyyy-mm-dd

</td></tr><tr><td>

range

</td><td>

String

</td><td>

Start, end, or a time in the 24 hour format hh:mm:ss.

</td></tr></tbody>
</table><table id="table_nhc_ljn_zv" class="returns"><thead><tr><th>

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

Output

```
Count: 7
```

## Scoped GlideSystem - daysAgo\(Number days\)

Returns the date and time for a specified number of days ago.

|Name|Type|Description|
|----|----|-----------|
|days|Number|Integer number of days|

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

```
function contractNoticeDue() {
    var now_GR = new GlideRecord("contract");
    now_GR.addQuery("u_contract_status", "Active");
    now_GR.query();
    while (now_GR.next()) {
    if ((now_GR.u_termination_date <= gs.daysAgo(-90)) && (now_GR.u_contract_duration == "Long")) {
            now_GR.u_contract_status = "In review";
        } 
        else if ((now_GR.u_termination_date <= gs.daysAgo(-50)) && (now_GR.u_contract_duration == "Medium")) {
        now_GR.u_contract_status = "In review";
        } 
        else if ((now_GR.u_termination_date <= gs.daysAgo(-10)) && (now_GR.u_contract_duration == "Short")) {
            now_GR.u_contract_status = "In review";
        }
    }
    now_GR.update();
}
```

## Scoped GlideSystem - daysAgoEnd\(Number days\)

Returns the date and time for the end of the day a specified number of days ago.

|Name|Type|Description|
|----|----|-----------|
|days|Number|Integer number of days|

|Type|Description|
|----|-----------|
|String|GMT end of the day in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - daysAgoStart\(Number days\)

Returns the date and time for the beginning of the day a specified number of days ago.

|Name|Type|Description|
|----|----|-----------|
|days|String|Integer number of days|

|Type|Description|
|----|-----------|
|String|GMT start of the day in the format yyyy-mm-dd hh:mm:ss|

```
var now_GR = new GlideRecord('sysapproval_approver');
now_GR.addQuery('state', 'requested');
now_GR.addQuery('sys_updated_on', '<', gs.daysAgoStart(5));
now_GR.query();
```

## Scoped GlideSystem - debug\(String message, Object parm1, Object parm2, Object parm3, Object parm4, Object parm5\)

Writes a debug message to the system log.

|Name|Type|Description|
|----|----|-----------|
|message|String|The log message with place holders for any variable arguments.|
|param1|Object|\(Optional\) First variable argument.|
|param2|Object|\(Optional\) Second variable argument.|
|param3|Object|\(Optional\) Third variable argument.|
|param4|Object|\(Optional\) Fourth variable argument.|
|param5|Object|\(Optional\) Fifth variable argument.|

|Type|Description|
|----|-----------|
|void| |

```
gs.debug("This is a debug message");
var myFirstName = "Abel";
var myLastName = "Tuter";
gs.debug("This is a debug message from {0}.{1}", myFirstName, myLastName);
```

Output:

```
This is a debug message (sys.scripts extended logging)
This is a debug message from Abel.Tuter (sys.scripts extended logging)
```

## Scoped GlideSystem - endOfLastMonth\(\)

Returns the date and time for the end of last month in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT end of last month, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfLastWeek\(\)

Returns the date and time for the end of last week in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT end of last week, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfLastYear\(\)

Returns the date and time for the end of last year in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfNextMonth\(\)

Returns the date and time for the end of next month in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfNextWeek\(\)

Returns the date and time for the end of next week in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfNextYear\(\)

Returns the date and time for the end of next year in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfThisMonth\(\)

Returns the date and time for the end of this month in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfThisQuarter\(\)

Returns the date and time for the end of this quarter in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfThisWeek\(\)

Returns the date and time for the end of this week in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - endOfThisYear\(\)

Returns the date and time for the end of this year in GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - error\(String message, Object parm1, Object parm2, Object parm3, Object parm4, Object parm5\)

Writes an error message to the system log.

This method accepts up to five variable arguments \(varargs\) in the message using the Java MessageFormat placeholder replacement pattern.

**Note:** Variables must contain valid values for this method to provide correct output.

|Name|Type|Description|
|----|----|-----------|
|message|String|The log message with place holders for any variable arguments.|
|param1|Object|\(Optional\) First variable argument.|
|param2|Object|\(Optional\) Second variable argument.|
|param3|Object|\(Optional\) Third variable argument.|
|param4|Object|\(Optional\) Fourth variable argument.|
|param5|Object|\(Optional\) Fifth variable argument.|

|Type|Description|
|----|-----------|
|void| |

```
gs.error("This is an error message");
var myFirstName = "Abel";
var myLastName = "Tuter";
gs.error("This is an error message from {0}.{1}", myFirstName, myLastName);
```

Output:

```
This is an error message
This is an error message from Abel.Tuter
```

## Scoped GlideSystem - eventQueue\(String name, Object instance, String parm1, String parm2, String queue\)

Queues an event for the event manager.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the event being queued.|
|instance|Object|GlideRecord object, such as "current".|
|parm1|String|Optional. Saved with the instance if specified.|
|parm2|String|Optional. Saved with the instance if specified.|
|queue|String|Optional. Name of the queue.|

|Type|Description|
|----|-----------|
|void| |

```
if (current.operation() != 'insert' && current.comments.changes()) {
    gs.eventQueue('incident.commented', current, gs.getUserID(), gs.getUserName());
}
```

## Scoped GlideSystem - eventQueueScheduled\(String name, Object instance, String parm1, String parm2, Object expiration\)

Queues an event in the event manager.

The passed in event schedule information is stored in the Events \[sysevent\] table. For additional information on events, see [Events](https://www.servicenow.com/docs/access?context=events&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

<table id="table_nxv_r3k_bx" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the event to queue.

</td></tr><tr><td>

instance

</td><td>

Object/String

</td><td>

GlideRecord object or the sys\_id of the record to which this event applies.

</td></tr><tr><td>

parm1

</td><td>

String

</td><td>

Optional. String to pass into the event script. This parameter is free-form and depends on the implementation of the event script.Default: If the **instance** parameter is a GlideRecord object, then the default is the display value for that GlideRecord \(now\_GR.getDisplayValue\) otherwise it is `null`.

</td></tr><tr><td>

parm2

</td><td>

String

</td><td>

Optional. String to pass into the event script. This parameter is free-form and depends on the implementation of the event script. Default: `null`

</td></tr><tr><td>

expiration

</td><td>

Object

</td><td>

Optional. GlideDateTime object or a date/time type element that specifies the date and time to process the event.Default: Current date/time

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method using a GlideRecord, two parameters that are passed to the event script, and a specified time to schedule the event.

```
var requestXml = requestBody.dataString;
var processTime = new GlideDateTime();
processTime.addDaysLocalTime(7);
gs.eventQueueScheduled('sn_app.user.deactivate', now_GR, requestXML, gs.getUserID(), processTime);
```

This example shows how to call the method using a sys\_id and the default values for the optional parameters.

```
gs.eventQueueScheduled('event.test', '0e29421383101000dada83ec37d9292d', '', '', '');
```

## Scoped GlideSystem - executeNow\(GlideRecord job\)

Executes a job for a scoped application.

You can only use this method on a job in the same application as the script calling this method.

|Name|Type|Description|
|----|----|-----------|
|job|GlideRecord|Job to run.|

|Type|Description|
|----|-----------|
|String|Returns the sys\_id of the scheduled job. Returns null if the job is global.|

```
scheduleImportJob: function () {
  var jobId = '61847fe04c603300fa9bb64c2b491dac';
  var now_GR = new GlideRecord('sysauto_script');
  if (!now_GR.get(jobId)) {
    throw new Error('Unable to find import job');
  }
  gs.executeNow(now_GR);
}
```

## Scoped GlideSystem - generateGUID\(\)

Generates a GUID that can be used when a unique identifier is required.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A 32-character hexadecimal GUID.|

The following code example shows how to call this method.

```
personalId = gs.generateGUID();
gs.info(personalId);
```

Output:

```
af770511ff013100e04bfffffffffff6
```

## Scoped GlideSystem - getCallerScopeName\(\)

Gets the caller scope name; returns null if there is no caller.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The caller's scope name, or null if there is no caller.|

This example shows two script includes that are set to Accessible from all application scopes. One script include is created within app\_scope\_a.

```
var Scopea = Class.create(); 
 
Scopea.prototype = { 
    initialize: function() { 
    }, 
 
    callerScope: function() { 
        var scopeb = new app_scope_b.Scopeb(); 
        return scopeb.callerscope(); 
    }, 
 
    type: 'Scopea' 
}
```

Output:

This example shows another script include created within app\_scope\_b.

```
var Scopeb = Class.create(); 
 
Scopeb.prototype = { 
    initialize: function() { 
        this._constructorCallerScope = gs.getCallerScopeName(); 
    }, 
 
    callerscope: function() { 
        return gs.getCallerScopeName(); 
    }, 
 
    getConstructorCallerScope: function() { 
        return this._constructorCallerScope; 
    }, 
 
    type: 'Scopeb' 
}
```

Output:

This script can be used within scope app\_scope\_a to get the scope name of the caller—in this case app\_scope\_b.

```
gs.info(new Scopea().getCallerScopeName());
```

## Scoped GlideSystem - getCssCacheVersionString\(\)

Gets a string representing the cache version for a CSS file.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The CSS cache version.|

The following code example shows how to call this method.

```
var verStr = gs.getCssCacheVersionString();
gs.info(verStr);
```

Output:

```
_d82979516f0171005be8883e6b3ee4cf&theme=
```

## Scoped GlideSystem - getCurrentApplicationId\(\)

Gets the ID of the current application as set using the Application Picker.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current application's sys\_id, or global in none is set.|

```
var currentId = gs.getCurrentApplicationId();
gs.info(currentId);
```

Output

```
04936cb16f30b1005be8883e6b3ee4e0
```

## Scoped GlideSystem - getCurrentScopeName\(\)

Gets the name of the current scope.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current scope name.|

The following code example shows how to call this method.

```
var currentScope = gs.getCurrentScopeName();
gs.info(currentScope);
```

Output:

```
s_snc_test_scope
```

## Scoped GlideSystem - getDateFormat\(String\)

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

## Scoped GlideSystem - getDateTimeFormat\(\)

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

## Scoped GlideSystem - getErrorMessages\(\)

Returns the error messages that were added by addErrorMessage\(\) for the session.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of Strings|Error messages associated with the session.|

## Scoped GlideSystem - getEscapedMessage\(String id, Array args\)

Retrieves the specified message from the Message \[sys\_ui\_message\] table. If the message has HTML special characters, replaces them with the corresponding HTML name codes. For example, `&` becomes `&amp;`.

If the specified message identifier \(Key\) exists in the Message \[sys\_ui\_message\] table for the current language, the method returns the translated message with all special characters returned as escape sequences. If the specified message identifier does not exist for the current language, then the method returns the English version of the message with all special characters returned as escape sequences. If the message identifier does not exist in the table, then it returns the message ID.

For additional information about the Message table, see [Message table](https://www.servicenow.com/docs/access?context=r_MessageTable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** If the UI message has a tick \('\), there may be issues with the message in the script; to escape the ticks \('\), use getMessageS\(String, Object\).

<table id="table_m4y_5rz_5w" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

String

</td><td>

Message identifier. You can locate this value in the Key field of the Message \[sys\_ui\_message\] table. Note the Key field may look exactly like the actual message string.

</td></tr><tr><td>

args

</td><td>

Array

</td><td>

Optional. List of strings or other values defined by java.text.MessageFormat that replace the variables within the specified message. For example: `gs.getMessage("Abort adding action '{0}', same subflow can't be added twice in this subflow.", current.action.name);`

 In this example *'\{0\}'* is replaced with the content of *current.action.name*.

 **Note:** The passed in values are not translated. They are inserted verbatim in the message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|UI message with HTML special characters replaced with HTML name codes.|

This example shows the ampersand character being replaced with the equivalent ampersand HTML name code.

```
var my_message = gs.getEscapedMessage("Is the summary & details accurate?");
alert(my_message);
```

Output

```
Is the summary &amp; details accurate?
```

This example shows how to replace a single variable within a message and how the &lt; and &gt; symbols in the message are transposed to the corresponding HTML name codes of &amp;lt and &amp;gt.

```
// current.action.name is "update record"
var my_message = gs.getEscapedMessage("Abort adding action '{0}', same <subflow> can't be added twice in this subflow.", current.action.name);
alert(my_message);
```

Output

```
Abort adding action update record, same &ltsubflow&gt can't be added twice in this subflow.
```

## Scoped GlideSystem - getMessage\(String id, Array args\)

Retrieves translated messages from the Message \[sys\_ui\_message\] table to display in a UI.

If the specified message identifier \(key\) exists in the Message \[sys\_ui\_message\] table for the current language, then the method returns the translated message. If the specified message identifier does not exist for the current language, then the method returns the English version of the message. If the message identifier does not exist in the table, then it returns the message ID.

For additional information about the Message table, see [Message table](https://www.servicenow.com/docs/access?context=r_MessageTable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

**Note:** If the UI message has a tick \('\), there may be issues with the message in the script; to escape the ticks \('\), use getMessageS\(String, Object\).

<table id="table_nwm_grh_1r" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

String

</td><td>

Message identifier. You can locate this value in the Key field of the Message \[sys\_ui\_message\] table. Note the Key field may look exactly like the actual message.

</td></tr><tr><td>

args

</td><td>

Array

</td><td>

Optional. List of strings or other values defined by java.text.MessageFormat that replace the variables within the specified message. For example: `gs.getMessage("Abort adding action '{0}', same subflow can't be added twice in this subflow.", current.action.name);`

In this example *'\{0\}'* is replaced with the content of *current.action.name*.

**Note:** The passed in values are not translated. They are inserted verbatim in the message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|UI message.|

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
var my_message = gs.getEscapedMessage("Abort adding action '{0}', same subflow can't be added twice in {1} subflow.", [current.action.name, current.sub_flow.name]);
alert(my_message);
```

Output:

```
Abort adding action update record, same subflow can't be added twice in schedule users subflow.
```

## Scoped GlideSystem - getProperty\(String key, Object alt\)

Gets the value of a Glide property. If the property is not found, returns an alternate value.

|Name|Type|Description|
|----|----|-----------|
|key|String|The key for the property whose value should be returned.|
|alt|Object|\(Optional\) Alternate object to return if the property is not found.|

|Type|Description|
|----|-----------|
|String|The value of the Glide property, or the alternate object defined above.|

The following code example shows how to call this method.

```
var attachment_link = gs.getProperty('glide.servlet.uri');
gs.info(attachment_link);
```

Output:

```
https://instance.service-now.com/
```

## Scoped GlideSystem - getSession\(\)

Gets a reference to the current Glide session.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A reference for the current session.|

```
if (!gs.hasRole("admin") && !gs.hasRole("user_admin") && gs.getSession().isInteractive()) {
  current.addQuery("active", "true");
}
```

## Scoped GlideSystem - getSessionID\(\)

Retrieves the GlideSession session ID.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The session ID.|

```
var myUserObject = gs.getSessionID();
gs.info(myUserObject);
```

Output:

```
A0D4E5416F3F21005BE8883E6B3EE4B8
```

## Scoped GlideSystem - getSessionToken\(\)

This method is no longer available. Instead, use `gs.getSession().getSessionToken()`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The session token.|

## Scoped GlideSystem - getTimeFormat\(\)

Returns the time format associated with the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The time format associated with the current user.|

The following code example shows how to call this method.

```
var userTimeFormat = gs. getTimeFormat();
gs.info(userTimeFormat);

```

Output:

```
HH:mm:ss
```

## Scoped GlideSystem - getTimeZoneName\(\)

Returns the name of the time zone associated with the current user.

This method has been deprecated. Instead, use the [getTimeZoneName\(\)](../../GlideSessionScoped/concept/c_GlideSessionScopedAPI.md#) method in the GlideSession API.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The time zone name.|

The following code example shows how to call this method.

```
gs.info(gs.getTimeZoneName());
```

## Scoped GlideSystem - getUrlOnStack\(\)

Gets the current URI for the session.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The URI.|

```
gs.info(gs.getUrlOnStack());
```

## Scoped GlideSystem - getUser\(\)

Returns a reference to the scoped GlideUser object for the current user.

See [GlideUser - Scoped](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#)for a list of available methods.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideUser|Reference to a scoped user object.|

```
var myUserObject = gs.getUser();
gs.info(myUserObject);
```

Output

```
com.glide.script.fencing.ScopedUser@6c0645
```

## Scoped GlideSystem - getUserDisplayName\(\)

Gets the display name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_jtg_pwm_1r" class="returns"><thead><tr><th>

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

## Scoped GlideSystem - getUserID\(\)

Gets the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the current user.|

The following example shows how to unassign all active Incident records assigned to the current user.

```
var incidentGR = new GlideRecord('incident');
incidentGR.addActiveQuery();

// Filter results to incidents assigned to the current user
var currentUserSysId = gs.getUserID();
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

## Scoped GlideSystem - getUserName\(\)

Returns the user name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_u4c_mxm_1r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The user name of the current user.For example, this method returns abel.tuter as opposed to Abel Tuter.

</td></tr></tbody>
</table>This example gets the user name of the current user.

```
gs.info("The current user name is: " + gs.getUserName());
```

Output:

```
The current user name is: admin
```

## Scoped GlideSystem - hasRole\(Object role\)

Determines if the current user has the specified role.

|Name|Type|Description|
|----|----|-----------|
|role|Object|The role to check.|

|Type|Description|
|----|-----------|
|Boolean|True if the user had the role. Returns true for users with the administrator role.|

```
if (!gs.hasRole("admin") && !gs.hasRole("groups_admin")  && gs.getSession().isInteractive()) {
  var qc = current.addQuery("u_hidden", "!=", "true"); //cannot see hidden groups... 
  qc.addOrCondition("sys_id", "javascript:getMyGroups()"); //...unless in the hidden group
  gs.info("User has admin and groups admin roles");
}
else {
  gs.info("User does not have both admin and groups admin roles");
}
```

## Scoped GlideSystem - hoursAgo\(Number hours\)

Returns the date and time for a specified number of hours ago.

|Name|Type|Description|
|----|----|-----------|
|hours|Number|Integer number of hours|

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

```
if (current.operation() == 'insert') {
 // If no due date was specified, calculate a default
 if (current.due_date == '') {
 
  if (current.urgency == '1') {
   // Set due date to 4 hours ahead of current time
   current.due_date = gs.hoursAgo(-4);
  }
 
  if (current.urgency == '2') {
   // Set due date to 2 days ahead of current time
   current.due_date = gs.daysAgo(-2);
  }
 
  if (current.urgency == '3') {
   // Set due date to 7 days ahead of current time
   current.due_date = gs.daysAgo(-7);
  }
 }
}
```

## Scoped GlideSystem - hoursAgoEnd\(Number hours\)

Returns the date and time for the end of the hour a specified number of hours ago.

|Name|Type|Description|
|----|----|-----------|
|hours|Number|Integer number of hours|

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - hoursAgoStart\(Number hours\)

Returns the date and time for the start of the hour a specified number of hours ago.

|Name|Type|Description|
|----|----|-----------|
|hours|Number|Integer number of hours|

|Type|Description|
|----|-----------|
|String|GMT in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - include\(String name\)

Provides a safe way to call a script include from the sandbox, allowing only the inclusion of trusted scripts.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the script to include.|

<table id="table_z5p_2th_1r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the script include worked.Possible values:

-   true: Script include worked.
-   false: Script include failed.

</td></tr></tbody>
</table>This example gets the LDAPUtils in the current script context.

```
var ldapServer = new GlideRecord("ldap_server_config");
ldapServer.addActiveQuery();
ldapServer.query();
gs.include("LDAPUtils");
var ldapUtils = new LDAPUtils();
var errMsg = "";
while (ldapServer.next()) {
  var ldap = new GlideLDAP();
  var dn = ldapServer.dn;
  var env = ldap.setup();
  if (env == null) {
    errMsg = "Failed environment setup, missing URL";
    gs.eventQueue("ldap.connection_failed",   ldapServer, ldapServer.getDisplayValue(), errMsg);
    gs.logError("LDAP server " + ldapServer.getDisplayValue() + " failed scheduled connection test: " + errMsg, "LDAP");
 }
}
```

## Scoped GlideSystem - info\(String message, Object parm1, Object parm2, Object parm3, Object parm4, Object parm5\)

Writes an info message to the system log.

|Name|Type|Description|
|----|----|-----------|
|message|String|The log message with place holders for any variable arguments.|
|param1|Object|\(Optional\) First variable argument.|
|param2|Object|\(Optional\) Second variable argument.|
|param3|Object|\(Optional\) Third variable argument.|
|param4|Object|\(Optional\) Fourth variable argument.|
|param5|Object|\(Optional\) Fifth variable argument.|

|Type|Description|
|----|-----------|
|void| |

```
gs.info("This is an info message");
var myFirstName = "Abel";
var myLastName = "Tuter";
gs.info("This is an info message from {0}.{1}", myFirstName, myLastName);
```

Output:

```
This is an info message
This is an info message from Abel.Tuter
```

## Scoped GlideSystem - isDebugging\(\)

Determines if debugging is active for a specific scope.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if either session debugging is active or the log level is set to debug for the specified scope.|

```
gs.debug("This is a log message");
var myFirstName = "Abel";
var myLastName = "Tuter";
gs.debug("This is a log message from {0}.{1}", myFirstName, myLastName);
gs.info(gs.isDebugging());
```

## Scoped GlideSystem - isInteractive\(\)

Checks if the current session is interactive. An example of an interactive session is when a user logs in normally. An example of a non-interactive session is using a SOAP request to retrieve data.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the session is interactive.|

```
if (!gs.hasRole("admin") && gs.getSession().isInteractive()) {
    var qc1 = current.addQuery('u_group',"");
    var gra = new GlideRecord('sys_user_grmember');
    gra.addQuery('user', gs.getUserID());
    gra.query();
    while (gra.next()) {
        qc1.addOrCondition('u_group', gra.group);
    }
}
```

## Scoped GlideSystem - isLoggedIn\(\)

Determines if the current user is currently logged in.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the current user is logged in.|

```
gs.info(gs.isLoggedIn());
```

## Scoped GlideSystem - isMobile\(\)

You can determine if a request comes from a mobile device.

This method can be used in UI action conditions and business rules.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the request comes from a mobile device; otherwise, false.|

```
if (gs.isMobile())
  gs.info("submitted from mobile UI");
 else 
   gs.info("NOT submitted from mobile UI");
```

Output

```
NOT submitted from mobile UI
```

## Scoped GlideSystem - minutesAgoEnd\(Number minutes\)

Returns the date and time for the end of the minute a specified number of minutes ago.

|Name|Type|Description|
|----|----|-----------|
|minutes|Number|Integer number of minutes ago, such as 5 or 126.|

<table id="table_y1y_pny_fz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

GMT the specified number of minutes ago, at the end of the minute \(59 seconds\). Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time 30 minutes ago at the end of the minute in GMT.

```
var nowDateTime = new GlideDateTime();
gs.info("Now: " + nowDateTime);
var thirtyMinutesAgoDateTime = gs.minutesAgoEnd(30);
gs.info("Thirty minutes ago end time: " + thirtyMinutesAgoDateTime);
```

Output:

```
Now: 2021-10-20 15:22:13
Thirty minutes ago end time: 2021-10-20 14:52:59
```

## Scoped GlideSystem - minutesAgoStart\(Number minutes\)

Returns the date and time for the start of the minute a specified number of minutes ago.

|Name|Type|Description|
|----|----|-----------|
|minutes|Number|Integer number of minutes ago, such as 15 or 112.|

<table id="table_mhk_2py_fz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

GMT the specified number of minutes ago, at the start of the minute. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time 30 minutes ago at the start of the minute in GMT.

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

## Scoped GlideSystem - monthsAgo\(Number months\)

Returns the date and time for a specified number of months ago.

|Name|Type|Description|
|----|----|-----------|
|months|Number|Integer number of months ago.|

<table id="table_wyz_xpy_fz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

GMT of the specified number of months ago at the exact same time.Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time one month ago at the same time in GMT.

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

## Scoped GlideSystem - monthsAgoEnd\(Number months\)

Returns the date and time for the last day of the month a specified number of months ago.

|Name|Type|Description|
|----|----|-----------|
|months|Number \(Integer\)|Number of months, such as 4 or 16.|

<table id="table_wwt_ccv_22c" class="returns"><thead><tr><th>

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

## Scoped GlideSystem - monthsAgoStart\(Number months\)

Returns the date and time for the start of the month a specified number of months ago.

|Name|Type|Description|
|----|----|-----------|
|months|Number|Integer number of months ago, such as 3 or 14.|

<table id="table_ir4_5ry_fz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

GMT start of the month the specified number of months ago. Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>The following example displays the current date and time and the date and time three months ago in GMT.

```
var nowDateTime = new GlideDateTime();
gs.info("Now: " + nowDateTime);
var threeMonthsAgoDateTime = gs.monthsAgoStart(3);
gs.info("Three months ago start date and time: " + threeMonthsAgoDateTime);
```

Output

```
Now: 2021-10-20 15:05:27
Three months ago start date and time: 2021-07-01 07:00:00
```

## Scoped GlideSystem - nil\(Object o\)

Queries an object and returns true if the object is null, undefined, or contains an empty string.

|Name|Type|Description|
|----|----|-----------|
|o|Object|The object to check.|

|Type|Description|
|----|-----------|
|Boolean|True if the object is null, undefined, or contains an empty string; otherwise, returns false.|

```
var now_GR = new GlideRecord();
gs.info(gs.nil(now_GR));
```

Output

```
true
```

## Scoped GlideSystem - quartersAgoEnd\(Number quarters\)

Returns the date and time for the last day of the quarter for a specified number of quarters ago.

|Name|Type|Description|
|----|----|-----------|
|quarters|Number|Integer number of quarters|

|Type|Description|
|----|-----------|
|String|GMT end of the quarter that was the specified number of quarters ago, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - quartersAgoStart\(Number quarters\)

Returns the date and time for the first day of the quarter for a specified number of quarters ago.

|Name|Type|Description|
|----|----|-----------|
|quarters|Number|Integer number of quarters|

|Type|Description|
|----|-----------|
|String|GMT end of the month that was the specified number of quarters ago, in the format yyyy-mm-dd hh:mm:ss|

## Scoped GlideSystem - setProperty\(String key, String value, String description\)

Sets the specified key to the specified value if the property is within the script's scope.

**Note:** Care should be taken when setting system properties \(sys\_properties\) using this method as it causes a system-wide cache flush. Each flush can cause system degradation while the caches rebuild. If a value must be updated often, it should not be stored as a system property. In general, you should only place values in the sys\_properties table that do not frequently change.

|Name|Type|Description|
|----|----|-----------|
|key|String|The key for the property to be set.|
|value|String|The value of the property to be set.|
|description|String|A description of the property.|

|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
gs.setProperty("glide.foo","bar","foo");
gs.info(gs.getProperty("glide.foo"));
```

Output:

```
bar
```

## Scoped GlideSystem - setRedirect\(Object o\)

Sets the redirect URI for this transaction, which then determines the next page the user will see.

|Name|Type|Description|
|----|----|-----------|
|o|Object|URI object or URI string to set as the redirect|

|Type|Description|
|----|-----------|
|void| |

```
gs.setRedirect("com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=d41ce5bac611227a0167f4bf8109bf70&sysparm_user=" 
+ current.sys_id + "&sysparm_email=" + current.email)
```

## Scoped GlideSystem - tableExists\(String name\)

Determines if a database table exists.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the table to check for existence.|

|Type|Description|
|----|-----------|
|Boolean|True if the table exists. False if the table was not found.|

This example shows checking whether the incident and foo tables exist in the ServiceNow instance.

```
gs.info("Does the incident table exist? " + gs.tableExists("incident"));

gs.info("Does the foo table exist? " + gs.tableExists("foo"));
```

Output:

```
Does the incident table exist? true
Does the foo table exist? false
```

## Scoped GlideSystem - urlEncode\(String url\)

Encodes non-ASCII characters, unsafe ASCII characters, and spaces so the returned string can be used on the Internet. Uses UTF-8 encoding. Uses percent \(%\) encoding.

|Name|Type|Description|
|----|----|-----------|
|url|String|The string to encode.|

|Type|Description|
|----|-----------|
|String|A string with non-ASCII characters, unsafe ASCII characters, and spaces encoded.|

## Scoped GlideSystem - urlDecode\(String url\)

Replaces UTF-8 encoded characters with ASCII characters.

|Name|Type|Description|
|----|----|-----------|
|url|String|UTF-8 percent \(%\) encoded characters.|

|Type|Description|
|----|-----------|
|String|Encoded characters replaced with ASCII characters.|

## Scoped GlideSystem - warn\(String message, Object parm1, Object parm2, Object parm3, Object parm4, Object parm5\)

Writes a warning message to the system log.

|Name|Type|Description|
|----|----|-----------|
|message|String|The log message with place holders for any variable arguments.|
|param1|Object|\(Optional\) First variable argument.|
|param2|Object|\(Optional\) Second variable argument.|
|param3|Object|\(Optional\) Third variable argument.|
|param4|Object|\(Optional\) Fourth variable argument.|
|param5|Object|\(Optional\) Fifth variable argument.|

|Type|Description|
|----|-----------|
|void| |

```
gs.warn("This is a warning");
var myFirstName = "Abel";
var myLastName = "Tuter";
gs.warn("This is a warning from {0}.{1}", myFirstName, myLastName);
```

Output:

```
This is a warning
This is a warning from Abel.Tuter
```

## Scoped GlideSystem - xmlToJSON\(String xmlString\)

Takes an XML string and returns a JSON object.

|Name|Type|Description|
|----|----|-----------|
|xmlString|String|The XML string to be converted.|

|Type|Description|
|----|-----------|
|Object|A JSON object representing the XML string. Null if unable to process the XML string.|

The following code example shows how to call this method.

```
var jsonObject = gs.xmlToJSON(xmlString);
```

## Scoped GlideSystem - yearsAgo\(Number years\)

Returns a date and time for a certain number of years ago.

|Name|Type|Description|
|----|----|-----------|
|years|Number|An integer number of years|

|Type|Description|
|----|-----------|
|String|GMT beginning of the year that is the specified number of years ago, in the format yyyy-mm-dd hh:mm:ss.|

## Scoped GlideSystem - yesterday\(\)

Returns yesterday's time \(24 hours ago\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|GMT for 24 hours ago, in the format yyyy-mm-dd hh:mm:ss|


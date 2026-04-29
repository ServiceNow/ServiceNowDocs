---
title: Console - Scoped, Global
description: The Console API provides methods to log messages to the system log, create and stop timers, create and log counters, log stack traces, and group/organize related content.Logs an error message to system logs if the assertion is false. This method does nothing if the assertion is true.Counts and logs the number of times that count\(\) has been called with a specified label.Resets the specified counter to zero.Logs or outputs a debugging message to the system log at the debug level.Logs a message to the system log at the error level.Creates a new inline group in the system log, where all subsequent messages are indented at an additional level until groupEnd\(\) is called. Use this method to visually organize and group related messages in output and system logs.Exits the current inline group created with group\(\) and decreases the indent by one level.Logs a message to system logs at the info level.Logs a message to system logs.Starts a timer you can use to track how long an operation takes.Stops a specified timer that was previously started by calling time\(\).Logs the current value of a specified timer to the system log.Logs a stack trace to the system log at the info level.Logs a warning message to the system log at the warning level.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 25
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Console- Scoped, Global

The Console API provides methods to log messages to the system log, create and stop timers, create and log counters, log stack traces, and group/organize related content.

Console API methods provide the same logging functionality as [Glide System API](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) \(for example, gs.info, gs.warn, and gs.debug\), but allow more reflexive use for developers who are familiar with logging messages using console methods. Both Console API and Glide System API methods can be used on the server.

All Console API methods are static and are a ServiceNow® implementation of \(Microsoft Developer Network\) MDN's [Console API](https://developer.mozilla.org/en-US/docs/Web/API/Console_API). This API is provided as part of the ServiceNow base system and doesn't require a plugin to access it globally. To use this class in a scoped application, use the `sn_console` namespace identifier. Enable the Console \(com.glide.console\) plugin to access the Console API.

## Logging capabilities

Logs generated using Console API methods, like assert\(\), error\(\), debug\(\), warn\(\), info\(\), and log\(\), are logged in the System Logs. Specifically, you can find System Logs in the UI by navigating to **All** &gt; **System Logs** &gt; **System Log**. You can choose to view all logs or specific log types like Application Logs, Errors, Script Log Statements, and so on under this menu item. Filtering the Source column in the **All** logs view can help locate your entries faster.

## String substitutions

You can use zero or more substitution strings as the first parameter in many Console API methods, particularly those that allow you to log messages such as assert\(\), error\(\), debug\(\), warn\(\), info\(\), and log\(\).

Substitution strings in the Console API are placeholders you use in a log message to dynamically insert values, like strings or numbers. When the code runs, these placeholders are replaced with actual values that you pass as additional arguments, in the order they are provided. They make your logs more flexible and readable without needing to concatenate strings manually.

Common substitution strings:

-   `%s`: Inserts a string.
-   `%d` or `%i`: Inserts a number \(integer or decimal\).
-   `%f`: Inserts a floating-point number.
-   `%o`: Inserts an object.
-   `%c`: Applies CSS styles to the log \(useful for styling console output\).

Here is a simple example script using substitution strings:

```
const name = "Alex";
const age = 25;

console.log("Hello, my name is %s and I am %d years old.", name, age);
```

Example output:

```
Hello, my name is Alex and I am 25 years old.
```

Here is an example using substitution strings with CSS styling:

```
const user = { name: "Alex", role: "Developer" };
console.log("User info: %o", user); // Logs the object
console.log("%cStyled message", "color: blue; font-weight: bold;"); // Adds styles

```

The output styles the message `User info: { name: "Alex", role: "Developer" }` in blue and bold.

## Using timers

You can use Console API timers to calculate the duration of a specific operation. To start a timer, call [Console - time\(String label\)](ConsoleAPI.md#) and assign it a name using the **label** parameter. You can have a maximum of 10,000 timers per page. To stop a timer and get the elapsed time in milliseconds, call [Console - timeEnd\(String label\)](ConsoleAPI.md#) by passing the timer's name as the parameter.

For example, you can start a timer to measure the amount of time that passes by calling time\("Process Duration"\), and then call timeEnd\("Process Duration"\). Additionally, the code calculates and outputs how much time has elapsed since the timer start and when the first and second actions were completed by passing [Console - timeLog\(String label, Object valN\)](ConsoleAPI.md#) in the script.

```
console.time("Process Duration");

alert("Step 1: Click to continue."); // Simulates the first action
console.timeLog("Process Duration", "After Step 1");

alert("Step 2: Do other actions"); // Simulates additional actions
console.timeLog("Process Duration", "After Step 2");

console.timeEnd("Process Duration");
```

Output:

-   After the first alert:

    ```
    Process Duration: 2.345ms After Step 1
    ```

-   After the second alert:

    ```
    Process Duration: 7.890ms After Step 2
    ```

-   When the timer ends:

    ```
    Process Duration: 10.123ms
    ```


**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Console - assert\(Boolean assertion, Object val1...valN, String msg, String subst1...substN\)

Logs an error message to system logs if the assertion is false. This method does nothing if the assertion is true.

<table id="table_uw3_ld4_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assertion

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to log a generic message indicating an assertion failure to system logs.Valid values:

-   true: Doesn't log the assertion failure message.
-   false: Logs the assertion failure message.

Default: false

</td></tr><tr><td>

msg

</td><td>

String

</td><td>

Required if **val1...valN** is not used. Message to display in system logs when the assertion fails. Accepts a string containing zero or more substitution values that can be set using the **subst1 through substN** parameter.For more information, see 'String substitutions', see [Console - Scoped, Global](ConsoleAPI.md#).

</td></tr><tr><td>

subst1...substN

</td><td>

String

</td><td>

Optional. JavaScript values with which to replace substitution strings within **msg**. These values are logged or displayed in the order they are specified. If there are more substitution values than there are substitution strings, the extra values are themselves written are appended after the message \(**msg**\) in the same manner as when there is no format string.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr><td>

val1...valN

</td><td>

Object

</td><td>

Required if **msg** is not passed. List of additional JavaScript values to append after the main message \(**msg**\), and are separated by a space or another delimiter. Accepts any JavaScript data type, including strings or objects, and outputs them in the order they are specified.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

### Basic assertion

The following example shows how to use assert\(\) to log the error message "Math is broken!" when the assertion \(1 + 1 === 3\) is false, and does nothing when the assertion \(1 + 1 === 2\) is true.

```
console.assert(1 + 1 === 2, "This won't be logged."); // Assertion is true, nothing happens.
console.assert(1 + 1 === 3, "Math is broken!");
```

Output:

```
"Math is broken!"
```

### Logging additional values

The following example passes assert\(\) with additional values.

```
let x = 5, y = 10;
console.assert(x + y === 20, "Expected 20, got", x + y);
```

Output:

```
"Expected 20, got 15" // (because x + y is 15)
```

### Message substitution

The following example passes assert\(\) with string substitution values.

```
let expected = 20, actual = 15;
console.assert(expected === actual, "Expected %d but got %d", expected, actual);
```

Output:

```
"Expected 20 but got 15"
```

## Console - count\(String label\)

Counts and logs the number of times that count\(\) has been called with a specified label.

The count\(\) method is helpful for tracking the number of times something occurs, like how many times a block of code is executed or how many events occur in an application. Use [Console - countReset\(String label\)](ConsoleAPI.md#) to reset a counter with a specific label.

<table id="table_p2s_tt4_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String

</td><td>

Optional. Name to give the counter. Labels are case-sensitive and generates different counters in the output if cases don't match.Default: If not provided, sets the label to "default".

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example demonstrates how the output looks each time the count\(\) method is called with a label \(for example, 'apple' or 'banana'\). The count is tracked separately for each label.

```
console.count('apple');
console.count('banana');
console.count('apple');
console.count('apple');
console.count('banana');
```

Output:

```
apple: 1
banana: 1
apple: 2
apple: 3
banana: 2
```

The following count\(\) example demonstrates how the output looks when a counter label is not provided, inheriting a label of "default".

```
console.count();
console.count();
console.count();
```

Output:

```
default: 1
default: 2
default: 3
```

## Console - countReset\(String label\)

Resets the specified counter to zero.

<table id="table_imk_4w4_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String

</td><td>

Optional. Name of the counter originally set in the [Console - count\(String label\)](ConsoleAPI.md#) method that you want to reset to zero. Case-sensitive.Default: Resets the `default` counter to zero.

**Note:** A counter receives a label of `default` when a new counter is set using count\(\) without a defined label. See [Console - count\(String label\)](ConsoleAPI.md#) for more details.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to reset counter associated with the 5th iteration of the default label:

```
function greet(user) {
  console.count();
  return 'hi ${user}'
}

greet("bob");
greet("alice");
greet("alice");
console.count();
console.countReset();
```

Output:

```
"default: 1"
"default: 2"
"default: 3"
"default: 4"
"default: 0"
```

In the following example, if you pass the `user` variable as the `label` argument with the string "bob" to the first invocation of console.count\(\), and the string "alice" to the second:

```
function greet(user) {
  console.count(user);
  return'hi ${user}'
}

greet("bob");
greet("alice");
greet("alice");
console.countReset("bob");
console.count("alice");
```

Output. Note that resetting the value of the counter "bob" only changes the value of that counter. The value of "alice" is unchanged.

```
"bob: 1"
"alice: 1"
"alice: 2"
"bob: 0"
"alice: 3"
```

## Console - debug\(Object val1...valN, String msg, String subst1...substN\)

Logs or outputs a debugging message to the system log at the debug level.

The debug\(\) method allows verbose messaging and is recommended for low-priority or less critical debugging messages. For higher priority debug messaging use [Console - log\(Object val1...val2, String msg, String subst1...subst2\)](ConsoleAPI.md#). For instance, you can use this method to write longer debugging messages for internal developers about internal states or flows. The debug\(\) method messages may behave differently between certain browsers.

The console.debug\(\) method logs messages to system logs in the ServiceNow® instance. You can view these logs on the ServiceNow® platform in **System Logs** &gt; **All or System Logs** &gt; **Debug**.

**Note:** Console API methods provide the same logging functionality as [Glide System API](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) \(for example, gs.info, gs.warn, and gs.debug\), but allow more reflexive use for developers who are familiar with logging messages using console methods. Both Console API and Glide System API methods can be used on the server.

<table id="id_vct_4pl_pdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="Console-msg-parameter"><td>

msg

</td><td>

String

</td><td>

Required if **val1...valN** is not passed. The main message or object you want to log to system logs or in the output. Accepts a string containing zero or more substitution values that can be set using the **subst1 through substN** parameter.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-subst1substN-parameter"><td>

subst1...substN

</td><td>

String

</td><td>

Optional. JavaScript values with which to replace substitution strings within **msg**. These values are logged or displayed in the order they are specified. If there are more substitution values than there are substitution strings, the extra values are themselves written are appended after the message \(**msg**\) in the same manner as when there is no format string.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-val1valN-parameter"><td>

val1...valN

</td><td>

Object

</td><td>

Required if **msg** is not passed. List of additional JavaScript values to append after the main message \(**msg**\), and are separated by a space or another delimiter. Accepts any JavaScript data type, including strings or objects, and outputs them in the order they are specified.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

In the following example, console.debug\(\) logs messages to system logs in the ServiceNow® instance.

```
(function executeRule(current, previous /*null when async*/) {
    // Logging at different levels for debugging
    console.debug("Business rule triggered for record: " + current.getDisplayValue());
    
    // Example: Check and log a field value
    if (current.priority == 1) {
        console.debug("High-priority incident detected: " + current.number);
    } else {
        console.debug("Incident priority is not high. Priority: " + current.priority);
    }

    // Perform some logic
    if (current.state == 1) {
        current.state = 2;
        gs.debug("State updated from 'New' to 'In Progress' for record: " + current.number);
    }
})(current, previous);
```

## Console - error\(Object val1...valN, String msg, String subst1...subsN\)

Logs a message to the system log at the error level.

Use error\(\) to log issues that are critical and need immediate attention, such as invalid inputs, failed operations, or to debug unexpected behaviors.

**Note:** Console API methods provide the same logging functionality as [Glide System API](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) \(for example, gs.info, gs.warn, and gs.debug\), but allow more reflexive use for developers who are familiar with logging messages using console methods. Both Console API and Glide System API methods can be used on the server.

<table id="id_pjq_432_pdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="Console-msg-parameter"><td>

msg

</td><td>

String

</td><td>

Required if **val1...valN** is not passed. The main message or object you want to log to system logs or in the output. Accepts a string containing zero or more substitution values that can be set using the **subst1 through substN** parameter.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-subst1substN-parameter"><td>

subst1...substN

</td><td>

String

</td><td>

Optional. JavaScript values with which to replace substitution strings within **msg**. These values are logged or displayed in the order they are specified. If there are more substitution values than there are substitution strings, the extra values are themselves written are appended after the message \(**msg**\) in the same manner as when there is no format string.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-val1valN-parameter"><td>

val1...valN

</td><td>

Object

</td><td>

Required if **msg** is not passed. List of additional JavaScript values to append after the main message \(**msg**\), and are separated by a space or another delimiter. Accepts any JavaScript data type, including strings or objects, and outputs them in the order they are specified.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

In the following example, the error\(\) output displays the following code respectively:

-   The first example will simply display "An error occurred!" in an error-styled format.
-   The second will display "Error in module: ModuleName".
-   The third will display "Unexpected value: 42".

```
console.error("An error occurred!");
console.error("Error in module:", "ModuleName");
console.error("Unexpected value: %d", 42);

```

## Console - group\(String label\)

Creates a new inline group in the system log, where all subsequent messages are indented at an additional level until groupEnd\(\) is called. Use this method to visually organize and group related messages in output and system logs.

To end a grouping, call the [Console - groupEnd\(\)](ConsoleAPI.md#) method. The groupEnd\(\) method also decreases the indent of the group by one level.

**Note:** group\(\) shows all grouping levels in the output and are not collapsible or expandable.

<table id="table_v34_ckv_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String

</td><td>

Optional. Label name for the group to display in the output.Default: If you don't pass a label, group\(\) doesn't output any text but still indents the new empty line by one level.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example passes log\(\) to create a new nested block and then group\(\) to log indented groups. Each subsequent call to group\(\) indents the line at a new level. The script also calls groupEnd\(\) to end each group and decrease its indent by one level.

```
console.log("Start logging...");
console.group("Group 1");
console.log("Inside Group 1 - Message 1");
console.log("Inside Group 1 - Message 2");
console.group("Nested Group");
console.log("Inside Nested Group - Message 1");
console.groupEnd();
console.log("Back to Group 1 - Message 3");
console.groupEnd();
console.log("End logging...");
```

Display/output:

```
Start logging...
    Group 1
        Inside Group 1 - Message 1
        Inside Group 1 - Message 2
            Nested Group
                Inside Nested Group - Message 1
        Back to Group 1 - Message 3
End logging...
```

The following example demonstrates how groups are indented when a group label is set:

```
console.group("Group 1");
console.log("in group 1");
console.group();
console.log("in group 2");
```

Output:

```
Group 1
  in group 1
     in group 2
```

The following example demonstrates how groups are indented when a group label isn't set:

```
console.group(); // no label passed
console.log("in group 1");
console.group();
console.log("in group 2");
```

Output:

```
in group 1

     in group 2
```

## Console - groupEnd\(\)

Exits the current inline group created with group\(\) and decreases the indent by one level.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example creates a new nested block by calling group\(\) to log indented levels. The script passes groupEnd\(\)to end the group and decrease its indent by one level.

```
console.log("This is the outer level");
console.group();
console.log("Level 2");
console.group();
console.log("Level 3");
console.warn("More of level 3");
console.groupEnd();
console.log("Back to level 2");
console.groupEnd();
console.log("Back to the outer level");
```

Output:

```
This is the outer level
    Level 2
        Level 3
        ⚠️ More of level 3
    Back to level 2
Back to the outer level
```

## Console - info\(Object val1...valN, String msg, String subst1...substN\)

Logs a message to system logs at the info level.

**Note:** Console API methods provide the same logging functionality as [Glide System API](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) \(for example, gs.info, gs.warn, and gs.debug\), but allow more reflexive use for developers who are familiar with logging messages using console methods. Both Console API and Glide System API methods can be used on the server.

<table id="id_iqg_np2_pdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="Console-msg-parameter"><td>

msg

</td><td>

String

</td><td>

Required if **val1...valN** is not passed. The main message or object you want to log to system logs or in the output. Accepts a string containing zero or more substitution values that can be set using the **subst1 through substN** parameter.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-subst1substN-parameter"><td>

subst1...substN

</td><td>

String

</td><td>

Optional. JavaScript values with which to replace substitution strings within **msg**. These values are logged or displayed in the order they are specified. If there are more substitution values than there are substitution strings, the extra values are themselves written are appended after the message \(**msg**\) in the same manner as when there is no format string.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-val1valN-parameter"><td>

val1...valN

</td><td>

Object

</td><td>

Required if **msg** is not passed. List of additional JavaScript values to append after the main message \(**msg**\), and are separated by a space or another delimiter. Accepts any JavaScript data type, including strings or objects, and outputs them in the order they are specified.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example uses the info\(\) method to log two pieces of information: the record number and the priority of the current form. This method is useful for quick checks when debugging or verifying data in the form.

```
function onLoad() {
    console.info("Form loaded for record:", g_form.getValue("number")); // Log the record number
    console.info("Current priority is:", g_form.getValue("priority"));  // Log the priority
}
```

## Console - log\(Object val1...val2, String msg, String subst1...subst2\)

Logs a message to system logs.

**Note:** Console API methods provide the same logging functionality as [Glide System API](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) \(for example, gs.info, gs.warn, and gs.debug\), but allow more reflexive use for developers who are familiar with logging messages using console methods. Both Console API and Glide System API methods can be used on the server.

<table id="id_f3j_pp2_pdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="Console-msg-parameter"><td>

msg

</td><td>

String

</td><td>

Required if **val1...valN** is not passed. The main message or object you want to log to system logs or in the output. Accepts a string containing zero or more substitution values that can be set using the **subst1 through substN** parameter.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-subst1substN-parameter"><td>

subst1...substN

</td><td>

String

</td><td>

Optional. JavaScript values with which to replace substitution strings within **msg**. These values are logged or displayed in the order they are specified. If there are more substitution values than there are substitution strings, the extra values are themselves written are appended after the message \(**msg**\) in the same manner as when there is no format string.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-val1valN-parameter"><td>

val1...valN

</td><td>

Object

</td><td>

Required if **msg** is not passed. List of additional JavaScript values to append after the main message \(**msg**\), and are separated by a space or another delimiter. Accepts any JavaScript data type, including strings or objects, and outputs them in the order they are specified.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example show how to use log\(\) to log the record number and the current state of the form to system logs.

```
function onLoad() {
    console.log("Form loaded for record:", g_form.getValue("number")); // Log the record number
    console.log("Current state is:", g_form.getValue("state")); // Log the state
}
```

## Console - time\(String label\)

Starts a timer you can use to track how long an operation takes.

You can give each timer a unique name and may have up to 10,000 timers running on a given page. When you call the [Console timeEnd\(\)](ConsoleAPI.md#) method with the same label name, the counter outputs the time in milliseconds that elapsed since the timer was started. Use the [Console timeLog\(\)](ConsoleAPI.md#) method to log the elapsed time captured between the timer's start and stop time.

For examples about how to use this method with other time-based Console API methods, see "Using timers" in [Console - Scoped, Global](ConsoleAPI.md#).

<table id="table_dly_2xv_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String

</td><td>

Optional. Name to give the new timer. Use the same name when calling [Console - timeEnd\(String label\)](ConsoleAPI.md#) to stop the timer and output the elapsed time to the console.Maximum number of timers: 10,000

Default: Uses the label `"default"` if omitted.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following shows how to use time\("label"\) to start a timer with the label "label". The console.timeEnd\("label"\) method stops the timer with the same label and logs the elapsed time. In this example, it measures the time it takes to retrieve and log the record's number and priority.

```
function onLoad() {
    console.time("Form load processing time"); // Start timing

    // Example: Simulate some processing
    var recordNumber = g_form.getValue("number");
    console.log("Record number is:", recordNumber);

    var priority = g_form.getValue("priority");
    console.log("Priority is:", priority);

    console.timeEnd("Form load processing time"); // End timing and log duration
}
```

## Console - timeEnd\(String label\)

Stops a specified timer that was previously started by calling time\(\).

For examples about how to use this method with other time-based Console API methods, see "Using timers" in [Console - Scoped, Global](ConsoleAPI.md#).

<table id="table_xy4_kyv_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String

</td><td>

Optional. Name of the timer to stop. Once stopped, the elapsed time is automatically displayed in the console along with an indicator that the time has ended. This label must match the timer specified in the [Console - time\(String label\)](ConsoleAPI.md#) **label** parameter and is case-sensitive.Default: If omitted, uses the label `"default"`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to use time\("label"\) to start a timer with the label "label". The console.timeEnd\("label"\) method stops the timer with the same label; console.log\(\) logs the elapsed time. In this example, it measures the time it takes to retrieve and logs the record's number and priority in system logs.

```
function onLoad() {
    console.time("Form load processing time"); // Start timing

    // Example: Simulate some processing
    var recordNumber = g_form.getValue("number");
    console.log("Record number is:", recordNumber);

    var priority = g_form.getValue("priority");
    console.log("Priority is:", priority);

    console.timeEnd("Form load processing time"); // End timing and log duration
}
```

## Console - timeLog\(String label, Object valN\)

Logs the current value of a specified timer to the system log.

For examples about how to use this method with other time-based Console API methods, see "Using timers" in [Console - Scoped, Global](ConsoleAPI.md#).

<table id="table_mcg_hzv_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String

</td><td>

Optional. Name of the timer to log to the console. Must match the timer specified in [Console - time\(String label\)](ConsoleAPI.md#) **label** parameter and is case-sensitive.Default: Uses the label `"default"` if omitted.

</td></tr><tr><td>

valN

</td><td>

Object

</td><td>

Optional. Additional values to be logged after the timer output. Accepts an unstructured object supporting any data type with special handling for strings.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example demonstrates how to call timeLog\(\) using the label value of a timer previously started using the time\(\) method. The timeLog\(\) method logs the current value of a timer.

```
console.time("reticulating splines");
reticulateSplines();
console.timeLog("reticulating splines");
// reticulating splines: 650ms
```

If the timer name is omitted, then the timer is named `"default"`:

```
console.time();reticulateSplines();
console.timeLog();// default: 780ms
```

If there is no corresponding timer, `console.timeLog()` logs a warning like:

```
Timer "timer name" doesn't exist.

```

You can log additional values to the console after the timer output:

```
console.time();reticulateSplines();
console.timeLog("default","Hello","world");// default: 780ms Hello world
```

In another example, `console.time('Timer')` starts a timer with the label "Timer". `console.timeLog('Timer')` logs the elapsed time along with optional additional messages. `console.timeEnd('Timer')` stops the timer and logs the total elapsed time.

```
console.time('Timer');

setTimeout(() => {
    console.timeLog('Timer', 'Halfway done');
}, 1000);

setTimeout(() => {
    console.timeLog('Timer', 'Almost done');
    console.timeEnd('Timer');
}, 2000);
```

Log output:

```
Timer: 1000ms Halfway done
Timer: 2000ms Almost done
Timer: 2000ms
```

## Console - trace\(Object objects\)

Logs a stack trace to the system log at the info level.

<table id="table_bnt_x1w_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

objects

</td><td>

Object

</td><td>

Optional. Zero or more objects to output to the console along with the trace. Objects are assembled and formatted the same way they would be if passed to the [Console - log\(Object val1...val2, String msg, String subst1...subst2\)](ConsoleAPI.md#) method.Default: Returns the entire stack in output.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example demonstrates how `trace()` logs the message `Trace example` along with the stack trace.

```
function firstFunction() {
    secondFunction();
}

function secondFunction() {
    thirdFunction();
}

function thirdFunction() {
    console.trace('Trace example');
}

firstFunction();
```

The stack trace shows the call sequence: `thirdFunction` was called by `secondFunction`, which was called by `firstFunction`, and so on. The console.trace\('Trace example'\) logs the message `Trace example` along with the stack trace.

Output:

```
Trace example
    at thirdFunction (<filename>:8:13)
    at secondFunction (<filename>:4:5)
    at firstFunction (<filename>:2:5)
```

## Console - warn\(Object val1...valN, String msg, String subst1...subst2\)

Logs a warning message to the system log at the warning level.

**Note:** Console API methods provide the same logging functionality as [Glide System API](../../glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) \(for example, gs.info, gs.warn, and gs.debug\), but allow more reflexive use for developers who are familiar with logging messages using console methods. Both Console API and Glide System API methods can be used on the server.

<table id="id_lh5_ds2_pdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="Console-msg-parameter"><td>

msg

</td><td>

String

</td><td>

Required if **val1...valN** is not passed. The main message or object you want to log to system logs or in the output. Accepts a string containing zero or more substitution values that can be set using the **subst1 through substN** parameter.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-subst1substN-parameter"><td>

subst1...substN

</td><td>

String

</td><td>

Optional. JavaScript values with which to replace substitution strings within **msg**. These values are logged or displayed in the order they are specified. If there are more substitution values than there are substitution strings, the extra values are themselves written are appended after the message \(**msg**\) in the same manner as when there is no format string.See 'Using substitution strings' in [Console - Scoped, Global](ConsoleAPI.md#) for more information.

</td></tr><tr id="Console-val1valN-parameter"><td>

val1...valN

</td><td>

Object

</td><td>

Required if **msg** is not passed. List of additional JavaScript values to append after the main message \(**msg**\), and are separated by a space or another delimiter. Accepts any JavaScript data type, including strings or objects, and outputs them in the order they are specified.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example uses warn\(\) to log a warning message, typically styled to stand out \(for example, with a warning icon or yellow text\). This example checks the priority of the record: If it's high \(priority ==="1" \), it logs a warning message. If it's not high, it logs a less urgent note with the current priority value.

```
function onLoad() {
    var priority = g_form.getValue("priority");

    if (priority === "1") {
        console.warn("Warning: This is a high-priority incident! Immediate attention required.");
    } else {
        console.warn("Note: Priority is not high. Current priority:", priority);
    }
}
```

As a result, warn\(\) logs or displays the error like so:

-   For high-priority: `⚠️ Warning: This is a high-priority incident! Immediate attention required.`
-   For other priorities: `⚠️ Note: Priority is not high. Current priority: 3`


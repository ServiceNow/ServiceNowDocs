---
title: Debugging applications
description: Application developers can display debug messages about configuration records to help them troubleshoot issues. The Debug Scopes module provides information about the system switching between custom applications to run server-side scripts.Application developers can use the Debug Scopes module to display information about when the system switches between custom applications to run server-side scripts.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Debugging applications

Application developers can display debug messages about configuration records to help them troubleshoot issues. The Debug Scopes module provides information about the system switching between custom applications to run server-side scripts.

The system offers the following debugging options to help application developers determine how applications affect configuration records.

|Debugging option|Description|
|----------------|-----------|
|Debug Business Rule|Use this module to determine which application's business rules are running against tables. The system only displays application information if business rules from different application scopes run on the same table.|
|Debug Business Rule \(Details\)|Use this module to determine the results of running business rules against tables. The system only displays application information if business rules from different application scopes run on the same table.|
|Debug Security|Use this module to determine which application's access controls apply to a given table or record.|
|Debug Scopes|Use this module to determine the application scope context in which a script runs. Since one script can call another script it is possible to have multiple application scope context changes while running a series of scripts.|
|Enable Session Debug|Use this related link to enable the generation of log messages for a particular application. Application scripts that use GlideSystem logging methods will generate output to the log at the indicated verbosity level.|

When multiple applications contribute to the debug output, the system adds a new section called **Apps** to the display a list of the applications writing to the session log. Clicking on the check box next to the application name hides or displays the application's associated debug messages.

![](../image/DebuggingApplicationBusinessRules.png "Sample application debug output of business rules")

**Parent Topic:**[Debugging scripts](script-debug-overview.md)

## Debugging scopes

Application developers can use the **Debug Scopes** module to display information about when the system switches between custom applications to run server-side scripts.

When enabled, the system displays a message whenever the system switches to a custom application to run a server-side script.

![](../image/DebugScopesIncident.png "Sample debug scopes output from the incident table")

Every time the system runs a server-side script object it enters the script's scope context. When the script finishes running, the script exits the scope context. The debugging messages track changes to the script scope context.

The debugging message displays a greater than character &gt; each time the system enters a script object's context, and displays a less than character &lt; every time the system exits a script object's context. In cases where one script calls another the debugging message adds another greater than character to the path for each call. For example, if a business rule calls a script include, which in turn calls another script object there would three characters in the path such as:

```
> Entering scope [x_app_one]
>> Entering scope [x_app_two]
>>> Entering scope [x_app_three]
```

**Note:** The system does not display entering or exiting messages for script objects in the global scope.

Application developers may want to enable other debugging options to in conjunction with this option to see information about the possible source of the server-side script such as Debug Business Rule.


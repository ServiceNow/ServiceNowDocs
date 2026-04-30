---
title: Identify and resolve client errors
description: Identify client errors and resolve them in client-side scripts.There are several types of common client error.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Identify and resolve client errors

Identify client errors and resolve them in client-side scripts.

## Before you begin

Role required: admin

## About this task

When client errors occur, the Automated Test Framework fails the test on the step that was executing when the error occurred. Even though client-side scripts can fail silently on JavaScript errors while procedures are executing, the error may still impact data, and the procedure being executed. The Automated Test Framework considers these errors as validation failures.

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Automated Test Framework** &gt; **Tests** and run an Automated Test Framework test that interacts with a form.

2.  In the test results for this test, check for a step result with the following summary:

    `This step failed because the client error 'DETAILED ERROR MESSAGE' was detected on the page being tested. See failing Test Logs. To ignore these errors in the next test run, use ‘Add all client errors to warning/ignored list’ links.`

    This step result appears only on a step that interacts with the UI.

3.  To identify and resolve these script errors, open the developer tools browser console on the [Client Test Runner page](../reference/atf-client-test-runner-module.md).

    **Note:** For information about how to open the browser console, see the following article: [http://webmasters.stackexchange.com/questions/8525/how-to-open-the-javascript-console-in-different-browsers](http://webmasters.stackexchange.com/questions/8525/how-to-open-the-javascript-console-in-different-browsers)

4.  If you can see the error, try to identify and troubleshoot the problematic client-side script, which may be on any of the following base system tables:

    -   ServiceNow Client Script
    -   UI Action
    -   UI Macro \(HTML script\)
    -   UI Page \(HTML script\)
    -   UI Policy
    -   UI Script
    -   Tables that extend the preceding base system tables
5.  Review the script for errors and once you've fixed them, run your test again.


## What to do next

Determine the source of the client error by reviewing the script version history. If you customized a base system script, it's possible that the script has new versions that were skipped during upgrade.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](../concept/atf-build-overview.md)

## Example client errors

There are several types of common client error.

### Client JavaScript errors

When a client script causes an error, the browser console displays an error similar to the following example:

```
***************************************************
A script has encountered an error in render events
TypeError: Cannot read property 'id' of undefined
Script ends. Continuing happily
***************************************************
[00:00:00.002] onLoad Modify Comments Label
```

In this example, the client script Modify Comments Label caused the error.

### Other client script errors

Any other type of script error reports directly to the browser console with any formatting upon occurrence.

`TypeError: callbacks(id) is undefined`

### Script resource links by Sys ID

In some cases, the console error provides a link to the script resource file using its Sys ID. Following this link may give context to which script had executed it.

```
Uncaught ReferenceError: myobj is not defined
    at incident.do?sys_id=12345678901234567890123456789012
(anonymous) @ `incident.do?sys_id=12345678901234567890123456789012`  <---- LINK

```

### Script access permissions

While identifying problematic scripts, be sure the script has permission to access data. Check:

-   Access control rule permissions for tables and fields.
-   Application access permissions if the script accesses applications in a private scope.
-   Domain separation permissions if domain separation is configured.

**Related topics**  


[Allowed client errors](../concept/whitelisted-client-errors.md)


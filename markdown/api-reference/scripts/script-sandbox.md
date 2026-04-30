---
title: Script sandbox
description: The script sandbox is an environment with restricted rights in which client-generated scripts run when they’re made available to the script sandbox.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Script sandbox

The script sandbox is an environment with restricted rights in which client-generated scripts run when they’re made available to the script sandbox.

The script sandbox helps prevent unauthorized or unauthenticated users from executing privileged script on your instance. There are two cases that enable the client to send scripts to the server for evaluation \(client-generated scripts\).

-   Filters or queries: It’s legal to send a filter to the server such as: `assigned_to=javascript:getMyGroups()`.
-   System API: The API call AJAXEvaluate enables the client to run arbitrary scripts on the server and receive a response.

The script being evaluated via either of these two entry points runs within a reduced-rights sandbox with the following characteristics:

-   Only those business rules marked **Client callable** are available within the sandbox.
-   Only script includes marked **Sandbox enabled** are available within the sandbox.
-   Certain API calls \(largely but not entirely limited to ones dealing with direct database access\) aren’t allowed.
-   Data can’t be inserted, updated, or deleted from within the sandbox. Any calls to current.update\(\), for example, are ignored.

**Note:** Beginning with the Xanadu release, script includes marked as **Glide AJAX enabled** \(previously named **Client callable**\) aren’t accessible within the sandbox. Only those marked **Sandbox enabled** are available within the sandbox. When upgrading to the Zurich release from the Washington DC release or earlier, any script includes marked as **Client callable** are also marked as **Sandbox enabled**.

## Restricted methods with the script sandbox

These methods aren’t supported in client-generated scripts in the script sandbox.

**Note:** The GlideSystem \(gs\) methods log\(\), logError\(\), and logWarning\(\) can be enabled with script sandboxing by setting the **glide.security.sandbox\_no\_logging** system property to `false`.

<table id="table_ntx_d3s_mcb"><thead><tr><th>

Class

</th><th>

Method

</th></tr></thead><tbody><tr><td>

GlideRecord

</td><td>

-   deleteMultiple\(\)
-   deleteRecord\(\)
-   getRowCount\(\)
-   insert\(\)
-   update\(\)
-   updateMultiple\(\)

</td></tr><tr><td>

GlideSystem \(gs\)

</td><td>

-   addErrorMessage\(\)
-   addInfoMessage\(\)
-   addMessage\(\)
-   eventQueue\(\)
-   flushMessages\(\)
-   getEscapedProperty\(\)
-   getProperty\(\)
-   log\(\)
-   logError\(\)
-   logWarning\(\)
-   setProperty\(\)
-   setRedirect\(\)
-   setReturn\(\)
-   workflowFlush\(\)

</td></tr><tr><td>

ScopedGlideRecord

</td><td>

-   deleteMultiple\(\)
-   deleteRecord\(\)
-   insert\(\)
-   update\(\)
-   updateMultiple\(\)

</td></tr><tr><td>

ScopedGlideSystem \(gs\)

</td><td>

-   addErrorMessage\(\)
-   addInfoMessage\(\)
-   debug\(\)
-   eventQueue\(\)
-   executeNow\(\)
-   getProperty\(\)
-   getSessionToken\(\)
-   info\(\)
-   setRedirect\(\)

</td></tr><tr><td>

GlideDateTime

</td><td>

-   add\(\)
-   addDays\(\)
-   addDaysLocalTime\(\)
-   addDaysUTC\(\)
-   addMonths\(\)
-   addMonthsLocalTime\(\)
-   addSeconds\(\)
-   addWeeks\(\)
-   addYears\(\)
-   compareTo\(\)
-   getDate\(\)
-   getDayOfWeek\(\)
-   getDayOfWeekUTC
-   getDayOfWeekLocalTime\(\)
-   getDayOfMonth\(\)
-   getDayOfMonthLocalTime\(\)
-   getDayOfMonthNoTZ\(\)
-   getDayOfWeek\(\)
-   getDayOfWeekLocalTime\(\)
-   getDayOfWeekUTC\(\)
-   getHourOfDayLocalTime\(\)
-   getHourOfDayUTC\(\)
-   getDaysInMonth\(\)
-   getDaysInMonthUTC\(\)
-   getDaysInMonthLocalTime\(\)
-   getDisplayValueInternal\(\)
-   getDisplayValue\(\)
-   getLocalDate\(\)
-   getMonthLocalTime\(\)
-   getMonthNoTZ\(\)
-   getMonthUTC\(\)
-   getNumericValue\(\)
-   getTime\(\)
-   getTZOffset\(\)
-   getYear\(\)
-   getUserTimeZone\(\)
-   getWeekOfYearLocalTime\(\)
-   getWeekOfYearUTC\(\)
-   getYearUTC\(\)
-   getYearLocalTime\(\)
-   isDST\(\)
-   onOrAfter\(\)
-   onOrBefore\(\)
-   setDayOfMonthUTC\(\)
-   setDisplayValue\(\)
-   setMonth\(\)
-   setNumericValue\(\)
-   setTZ\(\)
-   setValue\(\)
-   setValueUTC\(\)
-   subtract\(\)
-   toString\(\)

</td></tr><tr><td>

GlideDate

</td><td>

GlideDate supports the same methods as GlideDateTime, as well as: -   getByFormat\(\)
-   getDayOfMonthNoTZ\(\)
-   getMonthNoTZint\(\)
-   parseDate\(\)

</td></tr><tr><td>

GlideTime

</td><td>

GlideTime supports the same methods as GlideDateTime, as well as: -   getByFormat\(\)
-   getHourLocalTime\(\)
-   getHourOfDayLocalTime\(\)
-   getHourOfDayUTC\(\)
-   getMinutesLocalTime\(\)
-   getMinutesUTC\(\)
-   getSeconds\(\)

</td></tr><tr><td>

GlideSchedule

</td><td>

-   add\(\)
-   isInSchedule\(\)
-   Load\(\)
-   whenNext\(\)

</td></tr></tbody>
</table>**Parent Topic:**[Server-side scripting](c_ServerScripting.md)


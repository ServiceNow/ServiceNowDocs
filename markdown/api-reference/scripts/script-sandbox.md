---
title: Script sandbox evaluator
description: The script sandbox evaluator helps prevent executing untrusted scripts on an instance by limiting the APIs available to scripts.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sandbox environment, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Script sandboxevaluator

The script sandbox evaluator helps prevent executing untrusted scripts on an instance by limiting the APIs available to scripts.

Scripts that run in the script sandbox evaluator can use features supported by the JavaScript engine and the sandbox environment, except for certain restricted methods. Untrusted scripts are processed by the script sandbox evaluator under the following conditions:

-   A script has been granted a guarded-script exemption \(manually or automatically\).
-   When guarded script is in Phase 1: Detection, and a script is sent to the server by an authenticated user.

For more information about guarded-script exemptions and enforcement phases, see [Guarded script evaluator](guarded-script.md).

## Restricted methods with the script sandboxevaluator

The script sandboxevaluator doesn't permit the following methods. Scripts using these methods fail to execute in the sandbox.

**Note:** The GlideSystem \(gs\) methods log\(\), logError\(\), and logWarning\(\) can be enabled for use with the script sandboxevaluator by setting the **glide.security.sandbox\_no\_logging** system property to `false`.

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
</table>**Parent Topic:**[Script sandbox environment](script-sandbox-environment.md)

**Related topics**  


[Guarded script evaluator](guarded-script.md)


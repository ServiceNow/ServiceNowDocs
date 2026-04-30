---
title: Configuring Script sandbox property
description: Enable the script sandbox property \(glide.script.use.sandbox\) to run client-generated scripts inside a sandbox that has restricted rights.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [High Security Settings]
---

# Configuring Script sandbox property

Enable the script sandbox property \(**glide.script.use.sandbox**\) to run client-generated scripts inside a sandbox that has restricted rights.

**Note:** This property is enabled by default when you activate the High Security Settings plugin. Don’t enable this property outside of the plugin.

There are two cases within the system that allow the client to send scripts to the server for evaluation.

-   Filters or queries: It’s legal to send a filter to the server such as: `assigned_to=javascript:getMyGroups()`.
-   System API: The API call AJAXEvaluate allows the client to run arbitrary scripts on the server and receive a response.

If you enable the script sandbox property \(**glide.script.use.sandbox**\), the script being evaluated via either of these two entry points runs within a reduced-rights sandbox with the following characteristics:

-   Only those business rules marked **Client callable** are available within the sandbox.
-   Only script includes marked **Sandbox enabled** are available within the sandbox.
-   Certain API calls \(largely but not entirely limited to those dealing with direct DB access\) aren’t allowed.
-   Data can’t be inserted, updated, or deleted from within the sandbox. Any calls to current.update\(\), for example, are ignored.

**Note:** Beginning with the Xanadu release, script includes marked as **Glide AJAX enabled** \(previously named **Client callable**\) aren’t accessible within the sandbox. Only those marked **Sandbox enabled** are available within the sandbox. When upgrading to the Yokohama release from the Washington DC release or earlier, any script includes marked as **Client callable** are also marked as **Sandbox enabled**.

<table id="simpletable_oyj_zk4_kq"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.script.use.sandbox**

</td><td>

Run client-generated scripts \(AJAXEvaluate and query conditions\) inside a reduced-rights "sandbox."If true, only those business rules with the **Client callable** option selected and script includes with the **Sandbox enabled** option selected are available and certain back-end API calls are disallowed.

-   Type: true \| false
-   Default value: true
-   Location: System Property \[sys\_properties\] table
-   For more information, see [Enable script sandbox \[Updated in Security Center 1.3\]](../../security-center/reference/sc-client-generated-scripts-sandbox.md) in Instance Security Hardening Settings.

</td></tr></tbody>
</table>## Restricted methods with sandbox enabled

These methods aren’t supported in client-generated scripts when script sandboxing is enabled.

**Note:** The GlideSystem \(gs\) methods log\(\), logError\(\), and logWarning\(\) can be enabled with script sandboxing by setting the **glide.security.sandbox\_no\_logging** system property to `false`.

If you run the system without script sandboxing enabled, then none of these restrictions apply.

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

GlideDateGlideDateTime

GlideTime

</td><td>

-   add\(\)
-   addDays\(\)
-   addDaysLocalTime\(\)
-   addDaysUTC\(\)
-   addMonthsLocalTime\(\)
-   addMonths\(\)
-   addSeconds\(\)
-   addWeeks\(\)
-   addYears\(\)
-   compareTo\(\)
-   getByFormat\(\)
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
-   getHourLocalTime\(\)
-   getLocalDate\(\)
-   getLocalTime\(\)
-   getMinutesLocalTime\(\)
-   getMinutesUTC\(\)
-   getMonthLocalTime\(\)
-   getMonthNoTZ\(\)
-   getMonthUTC\(\)
-   getNumericValue\(\)
-   getSeconds\(\)
-   getTime\(\)
-   getTZOffset\(\)
-   getValue\(\)
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

GlideSchedule

</td><td>

-   add\(\)
-   isInSchedule\(\)
-   Load\(\)
-   whenNext\(\)

</td></tr></tbody>
</table>
---
title: JavaScript APIs supported by guarded script
description: Review the JavaScript APIs that guarded script supports to help you analyze scripts in the Incompatible Guarded Scripts list and either rewrite them or create an exemption for them.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-04-21"
reading_time_minutes: 3
breadcrumb: [Guarded script evaluator, Sandbox environment, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# JavaScript APIs supported by guarded script

Review the JavaScript APIs that guarded script supports to help you analyze scripts in the Incompatible Guarded Scripts list and either rewrite them or create an exemption for them.

The guarded script evaluator permits the following methods from the ServiceNow server-side JavaScript APIs and the built-in JavaScript APIs. The guarded script evaluator handles scripts that call unsupported APIs differently depending on the transaction type and instance configuration. For more information, see [Guarded script evaluator](../concept/guarded-script.md).

## ServiceNow JavaScript APIs

Guarded script permits calling the following methods from server-side JavaScript APIs in untrusted scripts. For more information about server APIs, see [Server API reference](../../../build/applications/concept/api-server.md).

<table id="table_allowed_apis"><thead><tr><th>

Class

</th><th>

Method

</th></tr></thead><tbody><tr><td>

GlideSystem \(gs\)

</td><td>

-   beginningOfCurrentHour\(\)
-   beginningOfCurrentMinute\(\)
-   beginningOfDay\(\)
-   beginningOfLast120Days\(\)
-   beginningOfLast12Months\(\)
-   beginningOfLast15Minutes\(\)
-   beginningOfLast2Hours\(\)
-   beginningOfLast2Quarters\(\)
-   beginningOfLast2Years\(\)
-   beginningOfLast30Days\(\)
-   beginningOfLast30Minutes\(\)
-   beginningOfLast3Months\(\)
-   beginningOfLast45Minutes\(\)
-   beginningOfLast60Days\(\)
-   beginningOfLast6Months\(\)
-   beginningOfLast7Days\(\)
-   beginningOfLast90Days\(\)
-   beginningOfLast9Months\(\)
-   beginningOfLastHour\(\)
-   beginningOfLastMinute\(\)
-   beginningOfLastMonth\(\)
-   beginningOfLastQuarter\(\)
-   beginningOfLastSchedulePeriod\(\)
-   beginningOfLastWeek\(\)
-   beginningOfLastYear\(\)
-   beginningOfMonth\(\)
-   beginningOfNext2Quarters\(\)
-   beginningOfNextMonth\(\)
-   beginningOfNextQuarter\(\)
-   beginningOfNextSchedulePeriod\(\)
-   beginningOfNextWeek\(\)
-   beginningOfNextYear\(\)
-   beginningOfOneYearAgo\(\)
-   beginningOfSchedulePeriodsAgo\(\)
-   beginningOfThisMonth\(\)
-   beginningOfThisQuarter\(\)
-   beginningOfThisSchedulePeriod\(\)
-   beginningOfThisWeek\(\)
-   beginningOfThisYear\(\)
-   beginningOfToday\(\)
-   beginningOfTomorrow\(\)
-   beginningOfWeek\(\)
-   beginningOfYear\(\)
-   beginningOfYesterday\(\)
-   calDateDiff\(\)
-   dateAdd\(\)
-   dateDiff\(\)
-   dateGenerate\(\)
-   datePart\(\)
-   daysAgo\(\)
-   daysAgoEnd\(\)
-   daysAgoLocal\(\)
-   daysAgoStart\(\)
-   endOfCurrentHour\(\)
-   endOfCurrentMinute\(\)
-   endOfDay\(\)
-   endOfLast120Days\(\)
-   endOfLast12Months\(\)
-   endOfLast15Minutes\(\)
-   endOfLast2Hours\(\)
-   endOfLast2Quarters\(\)
-   endOfLast2Years\(\)
-   endOfLast30Days\(\)
-   endOfLast30Minutes\(\)
-   endOfLast3Months\(\)
-   endOfLast45Minutes\(\)
-   endOfLast60Days\(\)
-   endOfLast6Months\(\)
-   endOfLast7Days\(\)
-   endOfLast90Days\(\)
-   endOfLast9Months\(\)
-   endOfLastHour\(\)
-   endOfLastMinute\(\)
-   endOfLastMonth\(\)
-   endOfLastQuarter\(\)
-   endOfLastSchedulePeriod\(\)
-   endOfLastWeek\(\)
-   endOfLastYear\(\)
-   endOfMonth\(\)
-   endOfNext2Quarters\(\)
-   endOfNextMonth\(\)
-   endOfNextQuarter\(\)
-   endOfNextSchedulePeriod\(\)
-   endOfNextWeek\(\)
-   endOfNextYear\(\)
-   endOfOneYearAgo\(\)
-   endOfSchedulePeriodsAgo\(\)
-   endOfThisMonth\(\)
-   endOfThisQuarter\(\)
-   endOfThisSchedulePeriod\(\)
-   endOfThisWeek\(\)
-   endOfThisYear\(\)
-   endOfToday\(\)
-   endOfTomorrow\(\)
-   endOfWeek\(\)
-   endOfYear\(\)
-   endOfYesterday\(\)
-   generateGUID\(\)
-   getCurrentScopeName\(\)
-   getDurationDate\(\)
-   getMessage\(\)
-   getPreference\(\)
-   getUser\(\)
-   getUserDisplayName\(\)
-   getUserID\(\)
-   getUserName\(\)
-   hasRole\(\)
-   hoursAgo\(\)
-   hoursAgoEnd\(\)
-   hoursAgoLocal\(\)
-   hoursAgoStart\(\)
-   isFirstDayOfMonth\(\)
-   isFirstDayOfWeek\(\)
-   isFirstDayOfYear\(\)
-   isInteractive\(\)
-   isLastDayOfMonth\(\)
-   isLastDayOfWeek\(\)
-   isLastDayOfYear\(\)
-   isLoggedIn\(\)
-   lastWeek\(\)
-   minutesAgo\(\)
-   minutesAgoEnd\(\)
-   minutesAgoStart\(\)
-   monthsAgo\(\)
-   monthsAgoEnd\(\)
-   monthsAgoStart\(\)
-   nil\(\)
-   now\(\)
-   nowDateTime\(\)
-   nowGlideDateTime\(\)
-   nowNoTZ\(\)
-   quartersAgo\(\)
-   quartersAgoEnd\(\)
-   quartersAgoStart\(\)
-   user\(\)
-   userID\(\)
-   user\_id\(\)
-   yearsAgo\(\)
-   yesterday\(\)

</td></tr><tr><td>

GlideUser

</td><td>

-   getCompanyID\(\)
-   getCompanyRecord\(\)
-   getCountry\(\)
-   getDateFormat\(\)
-   getDateFormatEx\(\)
-   getDateTimeFormat\(\)
-   getDepartmentID\(\)
-   getDisplayName\(\)
-   getDomainDisplayValue\(\)
-   getDomainID\(\)
-   getEmail\(\)
-   getFirstName\(\)
-   getFullName\(\)
-   getLanguage\(\)
-   getLastName\(\)
-   getLocation\(\)
-   getManagedGroups\(\)
-   getManagerID\(\)
-   getManagerName\(\)
-   getMobileNumber\(\)
-   getMyExplicitGroups\(\)
-   getMyGroups\(\)
-   getMyGroupsExcludeAdmin\(\)
-   getTZ\(\)
-   getTimeFormat\(\)
-   getTimeFormatEx\(\)
-   getTimeZoneLabel\(\)
-   getTimeZoneLabelLang\(\)
-   getTitle\(\)
-   getUserRoles\(\)
-   isExplicitMemberOf\(\)
-   isMemberOf\(\)

</td></tr><tr><td>

GlideDate

</td><td>

-   getByFormat\(\)
-   getDayOfMonthNoTZ\(\)
-   getDisplayValue\(\)
-   getDisplayValueEx\(\)
-   getDisplayValueInternal\(\)
-   getDisplayValueLang\(\)
-   getMonthNoTZ\(\)
-   parseDate\(\)
-   setDisplayValue\(\)
-   setDisplayValueEx\(\)
-   setDisplayValueLang\(\)
-   setValue\(\)

</td></tr><tr><td>

GlideDateTime

</td><td>

-   add\(\)
-   addDays\(\)
-   addDaysLocalTime\(\)
-   addDaysUTC\(\)
-   addMonths\(\)
-   addMonthsLocalTime\(\)
-   addMonthsUTC\(\)
-   addSeconds\(\)
-   addWeeks\(\)
-   addYears\(\)
-   compareTo\(\)
-   getDate\(\)
-   getDayOfMonth\(\)
-   getDayOfMonthLocalTime\(\)
-   getDayOfMonthUTC\(\)
-   getDayOfWeek\(\)
-   getDayOfWeekLocalTime\(\)
-   getDayOfWeekUTC\(\)
-   getDaysInMonth\(\)
-   getDaysInMonthLocalTime\(\)
-   getDaysInMonthUTC\(\)
-   getDisplayValue\(\)
-   getDisplayValueEx\(\)
-   getDisplayValueInternal\(\)
-   getDisplayValueLang\(\)
-   getLocalDate\(\)
-   getLocalTime\(\)
-   getMonth\(\)
-   getMonthLocalTime\(\)
-   getMonthUTC\(\)
-   getNumericValue\(\)
-   getTZOffset\(\)
-   getTime\(\)
-   getUserTimeZone\(\)
-   getValue\(\)
-   getWeekOfYearLocalTime\(\)
-   getWeekOfYearUTC\(\)
-   getYear\(\)
-   getYearLocalTime\(\)
-   getYearUTC\(\)
-   isDST\(\)
-   onOrAfter\(\)
-   onOrBefore\(\)
-   setDayOfMonthUTC\(\)
-   setDisplayValue\(\)
-   setDisplayValueEx\(\)
-   setDisplayValueLang\(\)
-   setMonth\(\)
-   setNumericValue\(\)
-   setTZ\(\)
-   setTimeZone\(\)
-   setValue\(\)
-   setValueUTC\(\)
-   subtract\(\)
-   toString\(\)

</td></tr><tr><td>

GlideTime

</td><td>

-   getDisplayValue\(\)
-   setValue\(\)

</td></tr><tr><td>

GlideRecord

</td><td>

-   getDisplayValue\(\)
-   getUniqueValue\(\)
-   getValue\(\)
-   isValid\(\)
-   isValidRecord\(\)

</td></tr><tr><td>

GlideBusinessCalendarUtil

</td><td>

-   getCalendarEnd\(\)
-   getCalendarFilterOptions\(\)
-   getCalendarSpanBounds\(\)
-   getCalendarStart\(\)
-   getCalendars\(\)
-   isLegacySchedule\(\)

</td></tr><tr><td>

GlideApplicationProperty

</td><td>

getValue\(\)

</td></tr><tr><td>

GlidePluginManager

</td><td>

isActive\(\)

</td></tr><tr><td>

GlideLocale

</td><td>

get\(\)

</td></tr><tr><td>

GlideSessionDebug

</td><td>

-   disable\(\)
-   enable\(\)

</td></tr><tr><td>

GlideDomainSupport

</td><td>

getCurrentDomainValueOrGlobal\(\)

</td></tr><tr><td>

GlideAccessibility

</td><td>

isEnabled\(\)

</td></tr><tr><td>

GlideJSUtil

</td><td>

-   nil\(\)
-   notNil\(\)

</td></tr><tr><td>

GlideNumberManager

</td><td>

getNextObjNumberPadded\(\)

</td></tr><tr><td>

TableUtils

</td><td>

getAllExtensions\(\)

</td></tr><tr><td>

GlideListFilter

</td><td>

-   getItilDefaultGroupTypes\(\)
-   getNonItilDefaultGroupTypes\(\)

</td></tr><tr><td>

GlideEmailWatermark

</td><td>

optionallyRandomize\(\)

</td></tr><tr><td>

GlideCounter

</td><td>

next\(\)

</td></tr><tr><td>

GlideProperties

</td><td>

get\(\)

</td></tr><tr><td>

GlideTSDebug

</td><td>

enable\(\)

</td></tr><tr><td>

DashboardFiltersParser

</td><td>

-   getBookmarked\(\)
-   getCertified\(\)
-   getCreatedByMe\(\)
-   getDashboardsWithCategories\(\)
-   getRecent\(\)
-   getSharedWithMe\(\)

</td></tr></tbody>
</table>## JavaScript built-in APIs

Guarded script also permits calling the following methods on JavaScript built-in objects in untrusted scripts.

<table id="table_builtin_methods"><thead><tr><th>

Object

</th><th>

Method

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Static methods:

-   isArray\(\)
-   of\(\)

 Instance methods:

-   concat\(\)
-   entries\(\)
-   flat\(\)
-   includes\(\)
-   indexOf\(\)
-   join\(\)
-   keys\(\)
-   lastIndexOf\(\)
-   length
-   slice\(\)
-   toString\(\)
-   values\(\)

</td></tr><tr><td>

Object

</td><td>

Static methods:

-   entries\(\)
-   getOwnPropertyDescriptor\(\)
-   getOwnPropertyNames\(\)
-   is\(\)
-   isExtensible\(\)
-   isFrozen\(\)
-   isSealed\(\)
-   keys\(\)
-   values\(\)

 Instance methods:

-   hasOwnProperty\(\)
-   isPrototypeOf\(\)
-   propertyIsEnumerable\(\)
-   toLocaleString\(\)
-   toString\(\)
-   valueOf\(\)

</td></tr><tr><td>

String

</td><td>

Static methods:

-   fromCharCode\(\)
-   fromCodePoint\(\)

 Instance methods:

-   at\(\)
-   charAt\(\)
-   charCodeAt\(\)
-   codePointAt\(\)
-   concat\(\)
-   endsWith\(\)
-   includes\(\)
-   indexOf\(\)
-   lastIndexOf\(\)
-   length
-   normalize\(\)
-   replace\(\)
-   replaceAll\(\)
-   slice\(\)
-   split\(\)
-   startsWith\(\)
-   substr\(\)
-   substring\(\)
-   toLocaleLowerCase\(\)
-   toLocaleUpperCase\(\)
-   toLowerCase\(\)
-   toString\(\)
-   toUpperCase\(\)
-   trim\(\)
-   trimEnd\(\)
-   trimStart\(\)
-   valueOf\(\)

</td></tr><tr><td>

Number \(constructor\)

</td><td>

Static methods:

-   isFinite\(\)
-   isInteger\(\)
-   isNaN\(\)
-   isSafeInteger\(\)
-   parseFloat\(\)
-   parseInt\(\)

 Instance methods:

-   toExponential\(\)
-   toFixed\(\)
-   toLocaleString\(\)
-   toPrecision\(\)
-   toString\(\)
-   valueOf\(\)

</td></tr><tr><td>

Boolean \(constructor\)

</td><td>

Instance methods:

-   toString\(\)
-   valueOf\(\)

</td></tr><tr><td>

Date \(constructor\)

</td><td>

Static methods:

-   now\(\)
-   parse\(\)
-   UTC\(\)

 Instance methods:

-   getDate\(\)
-   getDay\(\)
-   getFullYear\(\)
-   getHours\(\)
-   getMilliseconds\(\)
-   getMinutes\(\)
-   getMonth\(\)
-   getSeconds\(\)
-   getTime\(\)
-   getTimezoneOffset\(\)
-   getUTCDate\(\)
-   getUTCDay\(\)
-   getUTCFullYear\(\)
-   getUTCHours\(\)
-   getUTCMilliseconds\(\)
-   getUTCMinutes\(\)
-   getUTCMonth\(\)
-   getUTCSeconds\(\)
-   toDateString\(\)
-   toGMTString\(\)
-   toISOString\(\)
-   toJSON\(\)
-   toLocaleDateString\(\)
-   toLocaleString\(\)
-   toLocaleTimeString\(\)
-   toString\(\)
-   toTimeString\(\)
-   toUTCString\(\)
-   valueOf\(\)

</td></tr><tr><td>

Math

</td><td>

Static methods:

-   abs\(\)
-   acos\(\)
-   asin\(\)
-   atan\(\)
-   atan2\(\)
-   ceil\(\)
-   cos\(\)
-   exp\(\)
-   floor\(\)
-   log\(\)
-   max\(\)
-   min\(\)
-   pow\(\)
-   random\(\)
-   round\(\)
-   sin\(\)
-   sqrt\(\)
-   tan\(\)

</td></tr><tr><td>

JSON

</td><td>

Static methods:

-   parse\(\)
-   stringify\(\)

</td></tr></tbody>
</table>**Parent Topic:**[Guarded script evaluator](../concept/guarded-script.md)


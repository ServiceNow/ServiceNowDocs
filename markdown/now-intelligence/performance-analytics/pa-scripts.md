---
title: Scripting in Performance Analytics
description: Performance Analytics provides several script objects for use in scripts and APIs for querying Performance Analytics data. The scripts serve as breakdown mappings or to calculate a value from an indicator.To create a script, first select the facts table to which the script applies and explicitly select any fields.Several variables are available for use in Performance Analytics scripts and formula indicators.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Scripting in Performance Analytics

Performance Analytics provides several script objects for use in scripts and APIs for querying Performance Analytics data. The scripts serve as breakdown mappings or to calculate a value from an indicator.

## Tips on scripts

-   In general, use scripts only to support indicators like Age with date processing, using the `score_start` and `score_end` variables.
-   Limit unnecessary fields. Every time you include an extra dot-walked field, you add an extra join to the query.
-   Try to replace manual breakdowns with [database views](performance-analytics-glossary.md#) for better performance.
-   Try to use script includes for common functions. For more information, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US).
-   If the data is not structured in a way you need for reporting, try adding 'reporting fields' to the operational tables instead of creating scripts. For more information, see this [Community post](https://community.servicenow.com/community?id=community_blog&sys_id=2f99990fdbee5b00fece0b55ca9619fb).
-   If you are running a background script that queries the Performance Analytics scores or snapshots tables, you cannot access data about a scoped application unless you have an appropriate role for that application.

**Warning:** Try not to use GlideRecords or GlideAggregates in Performance Analytics scripts or formula indicators. While sometimes you must use these operations to get what you want, they are expensive, potentially running hundreds of thousands of times. Be certain that no alternative exists before you use them.

## Breakdown mapping and indicator scripts

A [breakdown mapping](performance-analytics-glossary.md#) script typically returns either a sys\_id of a breakdown element or an integer to put the score in a bucket. Indicator scripts return a score calculated from one or more fields. The same script can serve both as a breakdown mapping script and as an indicator script.

## Breakdown script

For example, consider the provided Incident.Age.Days script, which uses the `opened_at` field from the incident table. This script serves as a breakdown mapping for the Age breakdown, which uses the Incident Age Ranges \(Days\) [bucket group](performance-analytics-glossary.md#) as the breakdown source.

```
var diff=function(x,y){return y.dateNumericValue() - x.dateNumericValue();};
var days=function(x,y){return diff(x,y)/(24*60*60*1000);};
days(current.opened_at, score_end);
```

In this example, `current.opened_at` gets the timestamp of when the currently evaluated record was opened. The `score_end` [script variable](pa-scripts.md#) comes from the [data collector](performance-analytics-glossary.md#) and is bound to the period being collected. For example, if a monthly indicator is being collected, the `score_end` is the end of the month. Here the timestamp of when the incident was opened is subtracted from the timestamp of the end of the collection period and the result is converted to days.

This example includes the `Incident.opened_at` field, which is specified in the **Fields** field for this script. You can use `score_start` and `score_end` without defining them in the **Fields** field.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

**Related topics**  


[Create a breakdown mapping on a breakdown record](../task/t_CrtBkdnBreakdownMpngs.md)

[Server Scoped API List](https://developer.servicenow.com/dev.do#!/reference/api/tokyo/server)

## Create a script in Performance Analytics

To create a script, first select the facts table to which the script applies and explicitly select any fields.

### Before you begin

Role required: admin, pa\_admin. To access data for scoped applications in Performance Analytics tables, you also need the appropriate admin role for that application.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Scripts** and click **New**.

2.  Give the script a descriptive **Name**.

3.  Select the **Facts table** that the script applies to.

    Only indicators that use the same facts table can use this script.

4.  Select the fact table **Fields**, if any, that will be used in the script.

    You select fields by their labels.

5.  Write the script.

    The script must conform to the following relationships and restrictions:

    -   You can include only the fields that are selected in this form and script variables. For more information, see the section about Performance Analytics variables.
    -   When you use a field in the script, you use the column name. If necessary, look up the column name in the facts table.
    -   When you use a field from a database view, you must include the prefix. For example, the incident\_sla database view includes the task\_sla table, with the prefix taskslatable. Task\_sla includes the business\_duration column. To use the business\_duration field from the incident\_sla database view, write it as taskslatable\_business\_duration. If you do not have access to the database view, ask your system administrator to find the prefix for you.

### What to do next

After you create the script, create a breakdown mapping or indicator that uses the script. You can open a breakdown mapping or indicator form by clicking **New** in either the breakdown mapping or indicator tab. The breakdown mappings and indicators that use this script are listed in those tabs.

## Performance Analytics variables

Several variables are available for use in Performance Analytics scripts and formula indicators.

You can use the following variables in Performance Analytics scripts and formulas.

-   `score_start`: First second of the day of the first indicator score collection. For scripts, the time is calculated based on the difference between the time zone of the Run As user for the collection job and the database time zone, which is GMT. For formulas, the time is calculated based on the difference between the time zone of the user who executes the formula and GMT. A user executes a formula by viewing the formula indicator in a dashboard widget or on the Analytics Hub.
-   `score_end`: Last second of the day of the last indicator score collection. The time is calculated the same way as for `score_start`.
-   `pa`: A formula variable, not usable in scripts, that provides a set of Analytics Hub attributes and methods.

In scripts, the score collection start and end variables are GlideElementGlideObject objects. You can obtain a GlideDateTime object from these variables by calling getGlideObject\(\), such as in this example: `gs.log("Score main = " + score_end.getGlideObject().getDayOfWeek());`

In formulas, the score collection start and end variables already are GlideDateTime objects. Therefore, you can use the variables directly without calling getGlideObject\(\), such as in this example: `gs.log("Score main = " + score_end.getDayOfWeek());`

The values of the start and end variables are bound to the period being collected. For example, if a monthly indicator is being collected, the `score_end` is the end of the month.

The `score_start` and `score_end` values are calculated based on the time zone of the relevant user. For Performance Analytics scripts, this is the Run As time zone for the collection job. For formulas, this is the time zone of the user who views the formula indicator in a dashboard widget or the Analytics Hub. Users in different time zones therefore may have different dates for `score_start` and `score_end` in a formula.

**Related topics**  


[Get analytics methods in formulas](../task/get-indicator-analytics.md)

[Changes to score\_start/end because of different user time zones](time-zones-indicator-formulas.md)


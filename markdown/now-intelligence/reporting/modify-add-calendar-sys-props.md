---
title: Modifying and adding calendar report system properties
description: Specify system property values to override Task table highlighting in calendar events, limit the number of events in a calendar cell, or change the day the calendar week starts.Highlighting for calendar report events is configured with field styles, which are defined for a particular table. You can configure whether calendar reports use field styles from the tables or report sources that they are based on.In calendar reports, you can configure the maximum number of events that appear in some calendar views.By default, weeks for calendar reports start on Sunday. You can add a system property to start weeks on Monday or another day instead.Configure a system property to specify how calendar week numbers are determined.By default, calendar reports save up to 10,000 records. Change this limit by setting the glide.ui.max\_calendar\_records system property. If the number of records fetched exceeds this limit, you are prompted to filter the data and run the report again.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Customize calendar reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Modifying and adding calendar report system properties

Specify system property values to override Task table highlighting in calendar events, limit the number of events in a calendar cell, or change the day the calendar week starts.

## Override Task table field styles for highlighting calendar events

Highlighting for calendar report events is configured with field styles, which are defined for a particular table. You can configure whether calendar reports use field styles from the tables or report sources that they are based on.

### Before you begin

Role required: admin

### About this task

By default, field styles in the Task \[task\] table are applied to calendar reports. If calendar reports are configured to use field styles from their tables or report sources, these field styles override the Task table styles.

**Note:** Calendar highlighting only applies to Core UI reports, not to Platform Analytics experience data visualizations.

### Procedure

1.  In the filter navigator, enter: `sys_properties.list`

2.  Select the **glide.ui.report.extend\_calendar\_choices** property to specify which field styles are used during calendar highlighting.

    -   If `false`, calendar reports will use only styles from the Task table when determining options for calendar highlighting. For example, a calendar report on the Change Request \[change\_request\] table will only use styles from the Task \[task\] table instead of styles from a the combination of the two tables.
    -   If `True`, calendar reports will use field styles from the table that the calendar report is based on.
3.  Click **Update**.


## Limit the number of events displayed on calendar days

In calendar reports, you can configure the maximum number of events that appear in some calendar views.

### Before you begin

Role required: report\_admin, admin.

### About this task

When the maximum number of events is exceeded, a **+ &lt;number&gt;** link appears, which opens a pop-up window with additional events. You can also configure the maximum number of events that appear in this pop-up window. When this maximum is exceeded, a **+ many** link appears, which opens a list of events instead of a pop-up window.

You can configure these settings for the following calendar views:

-   A calendar day when calendar is in month or year view
-   The top 'full day' section of a calendar day when a calendar is in day or week view

### Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Configure the **glide.report.calendar.max\_events\_displayed\_per\_cell** and **glide.report.calendar.max\_more\_events\_per\_day** properties.

3.  Click **Update**.


## Change the day that calendar weeks start on

By default, weeks for calendar reports start on Sunday. You can add a system property to start weeks on Monday or another day instead.

### Before you begin

Role required: admin

The **glide.ui.date\_format.first\_day\_of\_week** system property modifies the generated date/time value used in the query and sets the start day of the week in the rendered calender.

**Note:**

**glide.ui.filter.first\_day\_of\_week** must also be set to the same value as **glide.ui.date\_format.first\_day\_of\_week** for the set day to display properly.

If you change the **glide.ui.filter.first\_day\_of\_week** property after collecting Performance Analytics score data, you won't be able to view the scores for weekly indicators. To access them, you must [collect scores](../../performance-analytics/concept/c_ClctData.md) again.

### Procedure

1.  Add the **glide.ui.date\_format.first\_day\_of\_week** system property.

2.  Set one of the following integer values.

<table id="choicetable_mmt_yv3_55"><tbody><tr><td id="d207778e318">

**Start weeks on Sunday**

</td><td>

Set **Value** to `1`

</td></tr><tr><td id="d207778e333">

**Start weeks on Monday**

</td><td>

Set **Value** to `2`

</td></tr><tr><td id="d207778e348">

**Start weeks on Tuesday**

</td><td>

Set **Value** to `3`

</td></tr><tr><td id="d207778e363">

**Start weeks on Wednesday**

</td><td>

Set **Value** to `4`

</td></tr><tr><td id="d207778e378">

**Start weeks on Thursday**

</td><td>

Set **Value** to `5`

</td></tr><tr><td id="d207778e394">

**Start weeks on Friday**

</td><td>

Set **Value** to `6`

</td></tr><tr><td id="d207778e409">

**Start weeks on Saturday**

</td><td>

Set **Value** to `7`

</td></tr></tbody>
</table>    **Note:** Only Sunday and Monday are explicitly supported.

3.  Click **Submit**.


### What to do next

Configure the system property **glide.db.week\_numbering** to specify how weeks are calculated. For more information, see [Customize calendar weeks](modify-add-calendar-sys-props.md#).

## Customize calendar weeks

Configure a system property to specify how calendar week numbers are determined.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to `sys_properties.list`.

2.  Add the **glide.db.week\_numbering** system property.

    For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

3.  Set one of the following string values.

<table id="choicetable_mmt_yv3_55"><tbody><tr><td id="d207778e533">

**iso\_week**

</td><td>

Week 1 is the week with January 4, the first business day, or the first Thursday in it. \(These are mutually equivalent.\) There is no Week 00.

</td></tr><tr><td id="d207778e542">

**sunday\_week**

</td><td>

Week 1 is the week with the first Sunday of the year. Days before it are in Week 0.

</td></tr><tr><td id="d207778e551">

**monday\_week**

</td><td>

Week 1 is the week with the first Monday of the year. Days before it are in Week 0.

</td></tr><tr><td id="d207778e560">

**jan1\_week**

</td><td>

Week 1 is Jan 1-7; the next seven days are week 2, and so on.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Set calendar record limit

By default, calendar reports save up to 10,000 records. Change this limit by setting the **glide.ui.max\_calendar\_records** system property. If the number of records fetched exceeds this limit, you are prompted to filter the data and run the report again.

### Before you begin

Role required: admin.

### Procedure

1.  Add the **glide.ui.max\_calendar\_records** system property.

2.  Complete the form with the following values.

<table id="choicetable_xm2_5rq_y1b"><tbody><tr><td id="d207778e655">

**Name**

</td><td>

**glide.ui.max\_calendar\_records**

</td></tr><tr><td id="d207778e667">

**Description**

</td><td>

Enter a phrase that describes the function of the property, such as `Maximum number of calendar records saved`.

</td></tr><tr><td id="d207778e679">

**Type**

</td><td>

Integer

</td></tr><tr><td id="d207778e688">

**Value**

</td><td>

Enter the desired value for the number of records retained by the platform. The default value if this property is not configured is 10,000.

</td></tr></tbody>
</table>3.  Click **Submit**.


**Related topics**  


[Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)


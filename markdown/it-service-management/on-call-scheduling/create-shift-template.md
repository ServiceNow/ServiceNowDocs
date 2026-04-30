---
title: Create a shift template to simplify configuring shifts
description: You can predefine sets of shift settings using shift templates. Shift templates are a subset of group templates.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Define escalation process, On-Call Scheduling, IT Service Management]
---

# Create a shift template to simplify configuring shifts

You can predefine sets of shift settings using shift templates. Shift templates are a subset of group templates.

## Before you begin

Role required: rota\_admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **Administration** &gt; **Group Templates**.

2.  From the list of group schedule templates, select the template for which you want to create a new shift template.

3.  On the related list of the shift templates, click **New** and then fill in the On-Call Shift Template form.

    | | |
    |---|---|
    |Shift name|The friendly name of the shift template. For example, US or EMEA.|
    |Schedule type|The type of schedule. You can specify settings for a Simple schedule. Alternatively, you can select an existing template.|
    |All day|Select the check box if the shift spans the full workday.|
    |Start Time|If this is not an all-day shift, then specify the start time of the shift.|
    |End time|The end time of the shift.|
    |End time day|The day on which the shift should end.|
    |Repeat on|For repeating shifts, the days of the week on which the shift should repeat.|
    |On-Call Group Template|The group template to which the shift belongs.|
    |Time zone|The time zone of the members of the rosters that will fill the shift.|
    |Specify holiday Schedule|Select the check box to specify the holiday schedule for the shift. The setting is applied to the shift.|

4.  Click **Submit**.


## Result

The template is now available for you to choose when creating or updating a shift.

**Parent Topic:**[Defining On-Call Scheduling escalation process](../../user-administration/concept/defining-escalation-process-and-template.md)


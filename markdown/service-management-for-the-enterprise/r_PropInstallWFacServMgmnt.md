---
title: Properties installed with Facilities Service Management
description: Facilities Service Management Properties controls the behavior of the Facilities Service Management application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Installed with Facilities Service Management, Activate Facilities Service Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Properties installed with Facilities Service Management

Facilities Service Management Properties controls the behavior of the Facilities Service Management application.

Facilities Service Management adds the following properties.

<table id="table_b4f_jcp_yq"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

facilities.management.autoclose.request.time

</td><td>

Number of days \(integer\) after which Resolved requests are automatically closed. Zero \(0\) disables this feature.-   Type: integer
-   Default value: 1
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.workflow.state

</td><td>

Select the state at which the template workflow starts.-   Type: string
-   Default value: 5
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.default.end.time

</td><td>

Default end time for all work agents when no schedule is set, formatted as 17:00.-   Type: string
-   Default value: 17:00
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.fvw.area.unit

</td><td>

The system base area unit for facilities space tables. Set to true to use meters squared, or false to use feet squared.-   Type: true \| false
-   Default value: false
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.timezone.weight

</td><td>

Time zone weight.-   Type: integer
-   Default value: 10
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.state.value

</td><td>

Select the state that the request goes into after **work in progress**.-   Type: integer
-   Default value: 6
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.work.spacing

</td><td>

Amount of time \(in minutes\) to add between the end of a task and the travel start of the next.-   Type: integer
-   Default value: 0
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.skills.weight

</td><td>

Skills weight.-   Type: integer
-   Default value: 10
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.location.weight

</td><td>

Location weight.-   Type: integer
-   Default value: 10
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.default.start.time

</td><td>

Default start time for all agents when no schedule is set. If there is no scheduled task or if the task is continued from the previous day, the start time is set for a day other than the current day. This property uses a 24-hour clock.-   Type: string
-   Default value: 08:00
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.overwrite.user.location

</td><td>

Overwrite the user location with the primary location set in the fm\_m2m\_user\_to\_space table.-   Type: true \| false
-   Default value: true
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

glide.ui.facilities\_request\_task\_activity.fields

</td><td>

Facilities Request Task activity formatter fields-   Type: string
-   Default value: assigned\_to,cmdb\_ci,state,impact,priority,opened\_by,work\_notes,comments,override\_schedule\_conflict
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities\_management.map.merge.task.agent.markers

</td><td>

Merge the task and agent markers on the geolocation maps with a purple marker.-   Type: true \| false
-   Default value: false
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

facilities.management.max.agents.processed

</td><td>

Sets the maximum number of agents processed by auto-dispatch at a time. The system has an absolute limit of 300 agents. The system cannot auto-dispatch a task for a dispatch group that contains more agents than the value configured.-   Type: integer
-   Default value: 100
-   Location: **Facilities** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Service Management](r_InstallWFacServMgmnt.md)


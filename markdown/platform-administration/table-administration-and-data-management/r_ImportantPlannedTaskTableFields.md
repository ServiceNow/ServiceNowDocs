---
title: Important planned task table fields
description: The Planned Task table has these fields.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Planned tasks, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Important planned task table fields

The Planned Task table has these fields.

|Label|Name|Type|Description|
|-----|----|----|-----------|
|Actual cost|`work_cost`|currency|The actual cost of the planned task, to be compared with the Estimated cost.|
|Actual duration|`work_duration`|glide\_duration|The actual length of time \(from start time to end time\) of work on the planned task, to be compared with the Planned duration.|
|Actual effort|`work_effort`|glide\_duration|The actual time spent working, to be compared to the Planned effort.|
|Critical Path|`critical_path`|boolean| |
|Estimated cost|cost|currency|An estimation of the cost of the planned task, to be compared with the actual cost.|
|HTML Description|`html_description`|html|A description field that accepts HTML mark-up.|
|Percent Complete|`percent_complete`|decimal|A percentage of the completed effort. Generated using the Planned effort and Actual effort fields.|
|Planned duration|duration|glide\_duration|The estimated length of time \(from start time to end time\) of the planned task.|
|Planned effort|effort|glide\_duration|The estimated amount of time spent working on the planned task.|
|Planned end date|`end_date`|glide\_date\_time|The estimated date and time for the planned task to end.|
|Planned start date|`start_date`|glide\_date\_time|The estimated date and time for the planned task to start.|
|Remaining duration|`remaining_duration`|glide\_duration|The difference in planned and actual duration, representing the time left for the planned task.|
|Remaining effort|`remaining_effort`|glide\_duration|The difference in planned and actual effort, representing the amount of work time left for the planned task.|
|Rollup|rollup|boolean|Read-only field managed by the system that identifies the task as having child tasks. A rollup task has several its fields calculated from the children so those fields are read-only.|
|Time constraint|`time_constraint`|string|A description of time constraints that apply to the planned task.|
|Top Task|`top_task`|reference \(planned\_task\)|When different planned tasks are stacked in a hierarchy, this field populates with the highest-level parent task. For example, if Project A has a child Project B, and Project B has a child Project C, then the Top Task for Project C is Project A. The Top Task field for Project A is blank.|
|Actual start date|`work_start`|glide\_date\_time|The actual date when the work starts on the planned task.|
|Actual end date|`work_end`|glide\_date\_time|The actual date when the work ends on the planned task.|

**Parent Topic:**[Extending the Task table with Planned tasks](../concept/c_PlannedTask.md)


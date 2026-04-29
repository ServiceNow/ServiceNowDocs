---
title: Schedule Optimization properties
description: You can set parameters that control how optimization runs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Schedule Optimization components, Reference, Field Service Management]
---

# Schedule Optimization properties

You can set parameters that control how optimization runs.

## Field Service Schedule Optimization properties

## Schedule Optimization general properties

<table id="table_dy4_zsj_21c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Exit buffer time

</td><td>

Amount of time \(in minutes\) to add between the end of a task and the travel start of the next. An example of a valid time value is 10.-   Type: Integer
-   Default value: 0
-   Location: **All** &gt; **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Qualifier type for schedule optimization

</td><td>

The qualifier type for schedule optimization determines the criteria used to optimize schedules. There are two qualifier types available: "Assignment group" and "Territory."When the Field Service Territory model is enabled, the qualifier type automatically switches to "Territory" and remains fixed. This means that when the Territory model is active, the optimization process focuses on territories instead of assignment groups. For more information, see [Enable the Field Service territory model](../task/enable-territory-model.md).

-   Type: String
-   Default value: Assignment group
-   Location: **All** &gt; **Field Service** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Number of seconds used for task scheduling resolution

</td><td>

Specifies the acceptable interval for scheduling a task. For example, if the value is set to 300 seconds, Schedule Optimization will schedule tasks and the associated travel time, such as task start time, travel start time, or estimated end, to the nearest 5-minute start or end time.

-   Type: Integer
-   Default value: 300
-   Location: **All** &gt; **Field Service** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Maximum number of overlapping qualifiers in a qualifier set

</td><td>

Numeric value set to determine the maximum number of overlapping qualifiers that can be applied to a single qualifier set.-   Type: Integer
-   Default value: 30
-   Location: **All** &gt; **Field Service** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Logging level

</td><td>

The logging level will determine the type of information displayed in the results of an optimization log entry, providing details about the Schedule optimization run. There are four options available: Error, Warning, Info, and Debug.-   Type: Choice
-   Default value: Error
-   Location: **All** &gt; **Field Service** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>## Schedule Optimization travel time estimate properties

<table id="table_rmt_mjt_bfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum number of location points allowed in a map vendor call

</td><td>

Numeric value set to determine the maximum number of location points allowed in a map provider call. Beans.AI is the map provider that Schedule Optimization supports for travel time estimates. For more information, see [Schedule Optimization travel estimate providers](schedule-optimization-travel-estimate-providers.md).

-   Type: Integer
-   Default value: 300
-   Location:**All** &gt; **Field Service** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>## Schedule Optimization system properties

The following system properties are installed with Schedule Optimization.

<table id="table_hgt_tbh_5fc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_schedule\_optim.so\_max\_batch\_duration

</td><td>

Maximum duration between start and end time on a batch run, in hours.-   Type: Non-zero integer \(in hours\)
-   Default value: 6
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.so\_min\_batch\_duration

</td><td>

Minimum duration between start and end time on a batch run, in hours.-   Type: Non-zero integer \(in hours\)
-   Default value: 2
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.consider\_overlapping\_territories\_for\_scheduling

</td><td>

Controls whether overlapping territories are considered when scheduling tasks during optimization.-   Type: True/False
-   Default value: True
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.prioritized\_event\_assignment\_horizon\_offset

</td><td>

Number of minutes that will be adjusted to the Window start time of a task, only for GraphQL processing. This will be used by Schedule Optimization to prevent the Schedule Start and Schedule Travel Start from being scheduled in the past for prioritized events.-   Type: Non-zero integer \(in minutes\)
-   Default value: 1 minute
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.prioritized\_event\_max\_agent\_count

</td><td>

Maximum number of technicians to be considered for prioritized event optimization.-   Type: Non-zero integer
-   Default value: 20
-   Location: System Properties list \[sys\_properties\] table

**Note:**

If the data for a prioritized intraday job exceeds these limits, the job will not run, and no assignments will be received.

The 'maint' role is required to edit this property. This role is exclusive to internal users. Contact support to make changes.


</td></tr><tr><td>

sn\_schedule\_optim.prioritized\_event\_max\_task\_count

</td><td>

Maximum number of tasks to be considered for prioritized event optimization.-   Type: Non-zero integer
-   Default value: 100
-   Location: System Properties list \[sys\_properties\] table

**Note:**

If the data for a prioritized intraday job exceeds these limits, the job will not run, and no assignments will be received.

The 'maint' role is required to edit this property. This role is exclusive to internal users. Contact support to make changes.


</td></tr><tr><td>

sn\_schedule\_optim.max\_priority\_events

</td><td>

Maximum number of prioritized event types that can be configured to trigger optimization.-   Type: Non-zero integer
-   Default value: 3
-   Location: System Properties list \[sys\_properties\] table

**Note:** The 'maint' role is required to edit this property. This role is exclusive to internal users. Contact support to make changes.


</td></tr><tr><td>

sn\_schedule\_optim.prioritized\_optimization\_delay\_buffer

</td><td>

Time \(in seconds\) to wait before initiating the optimization process for prioritized events.-   Type: Non-zero integer \(in seconds 60-900\)
-   Default value: 180 seconds \(3 minutes\)
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.intraday\_assignment\_horizon\_offset

</td><td>

Specifies the time offset \(in minutes\) added to the current time when calculating the window start for tasks that have no defined window start.-   Type: Non-zero integer
-   Default value: 60
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.intraday\_max\_retry\_count

</td><td>

Specifies how many times the solution processor retries submitting an intraday optimization job.-   Type: Integer
-   Default value:1
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.intraday\_minimum\_frequency

</td><td>

Defines how frequently intraday optimization runs.-   Type: Non-zero integer
-   Default value \(in minutes\): 15
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.intraday\_policy

</td><td>

Specifies the default policy for intraday optimization. This can be overridden at the group level.-   Type: String
-   Default value: None
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.intraday\_qualifier\_type

</td><td>

Specifies whether intraday optimization runs by assignment group or territory.-   Type: Choice list
-   Default value: Assignment group
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.intraday\_window

</td><td>

Defines the default schedule that controls when intraday optimization can run.-   Type: String
-   Default value: None
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.max\_agent\_count

</td><td>

Limits the number of technicians considered during on‑demand and intraday optimization runs.-   Type: Non-zero integer
-   Default value: 50000
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.max\_task\_count

</td><td>

Limits the number of tasks considered during on‑demand and intraday optimization runs.-   Type: Non-zero integer
-   Default value: 50000
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.processing\_time\_per\_task

</td><td>

Specifies the maximum processing time, in seconds, that the optimizer can use to compute a solution.-   Type: Non-zero integer
-   Default value: 150
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.run\_summary\_packet\_size

</td><td>

Controls how many records are grouped when generating optimization run details.-   Type: Non-zero integer
-   Default value: 10
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.scheduled\_state\_count\_of\_task

</td><td>

The number of work order tasks that can be in a scheduled state before being assigned to a technician.-   Type: Non-zero integer
-   Default value: 1
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.schedule\_optimization\_qualifier\_type

</td><td>

Specifies whether schedule optimization runs by assignment group or territory.-   Type: String
-   Default value: Assignment group
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.schedule\_state\_type

</td><td>

Determines how tasks are scheduled. The choices are duration or number of tasks.-   Type: Choice list
-   Default value: Duration
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.scheduling\_resolution\_time

</td><td>

The number of seconds Schedule Optimization uses to round task start times, travel times, and end times.For example, a value of 60 rounds all start times, travel times, and end times to the nearest minute. A value of 300 rounds them to the nearest 5 minutes.

-   Type: Non-zero integer
-   Default value: 1 \(second\)
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.logging.verbosity

</td><td>

Sets the level of detail captured in Schedule Optimization logs for each run. The choices are info, debug, warn, and error.-   Type: Choice list
-   Default value: Error
-   Location: System Properties list \[sys\_properties\] table

**Note:** The 'maint' role is required to edit this property. This role is exclusive to internal users. Contact support to make changes.

</td></tr><tr><td>

sn\_schedule\_optim.so\_max\_solution\_threshold

</td><td>

Maximum number of ML solutions that can run simultaneously. When workload distribution is enabled with multiple jobs or multiple optimization modes run concurrently, increase this value.-   Type: Non-zero integer
-   Default value: 3
-   Location: System Properties list \[sys\_properties\] table

**Note:** The 'maint' role is required to edit this property. This role is exclusive to internal users. Contact support to make changes.

</td></tr><tr><td>

sn\_schedule\_optim.enable\_qualifier\_split

</td><td>

Determines which optimization modes use split qualifiers to distribute workloads across parallel jobs. Choices:

-   None – No distribution; all qualifiers processed in a single job.
-   Only Batch – Distribute qualifiers only for batch optimization runs.
-   Only Intraday – Distribute qualifiers only for intraday optimization runs.
-   Both – Distribute qualifiers for both batch and intraday optimization runs.

**Note:** Split qualifiers work with batch, intraday, and prioritized optimization but not on-demand optimization.

-   Type: choice
-   Default value:none
-   Location: System Properties list \[sys\_properties\] table

</td></tr><tr><td>

sn\_schedule\_optim.qualifier\_distribution\_splits

</td><td>

Number of splits to distribute qualifiers across parallel optimization jobs for each batch or intraday configuration. Higher split counts reduce processing time per job but require more ML capacity.If running multiple optimization modes simultaneously adjust `sn_schedule_optim.so_max_solution_threshold` to accommodate the total number of concurrent ML solutions needed.

-   Type: Integer
-   Default value: 1
-   Location: System Properties list \[sys\_properties\] table

**Note:** The 'maint' role is required to edit this property. This role is exclusive to internal users. Contact support to make changes.

</td></tr><tr><td>

sn\_schedule\_optim.maximum\_matrix\_size

</td><td>

Determines the maximum number of locations that can be queried to a third‑party map provider when computing travel estimates.-   Type: Integer
-   Default value: 40000
-   Location: System Properties list \[sys\_properties\] table

</td></tr></tbody>
</table>## Performance-related Schedule Optimization properties

The following is the list of solution processing properties that are available with the Schedule Optimization plugin. To access these properties, navigate to **All** &gt; **System Properties** &gt; **All Properties**.

<table id="table_iqs_ntj_21c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_1.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_1.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_1-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_2.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_2.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_2-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_3.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_3.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_3-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_4.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_4.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_4-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_5.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_5.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_5-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_6.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_6.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_6-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_7.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_7.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_7-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_8.claim\_limit

</td><td>

This property controls the number of Data Processing events that are captured and processed in a single background transaction. If the property is set to 100, the event handler will grab and process the first 100 Data Processing events from the queue in one background transaction.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.data\_queue\_8.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.data\_queue\_8-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_1.claim\_limit

</td><td>

Controls the number of Solution Processing events grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_1.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_1.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_2.claim\_limit

</td><td>

Controls the number of Solution Processing events grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_2.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_2.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_3.claim\_limit

</td><td>

Controls the number of Solution Processing events grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_3.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_3.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_4.claim\_limit

</td><td>

Controls the number of Solution Processing events grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_4.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_4.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_5.claim\_limit

</td><td>

Controls the number of Solution Processing events grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_5.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_5.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_6.claim\_limit

</td><td>

Controls the number of Solution Processing events grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_6.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_6.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_7.claim\_limit

</td><td>

Controls how many Solution Processing events are grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_7.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_7.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_8.claim\_limit

</td><td>

Controls the number of Solution Processing events grabbed by its event handler and processed in a single background transaction.-   Type: Integer
-   Default value: 500

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_queue\_8.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_queue\_8.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

sn\_schedule\_optim.data\_processor\_number\_of\_queues

</td><td>

Number of queues for data processing

Enables performance improvement for end to end optimization.-   Type: Integer
-   Default value: 4

</td></tr><tr><td>

sn\_schedule\_optim.solution\_processor\_number\_of\_queues

</td><td>

Number of queues for solution processing \(task updates\).Increases the number of custom queues \(up to 8\) for processing optimization solution and speeding up optimization by allowing more parallel processing during solution processing flow.

-   Type: Integer
-   Default value: 4

</td></tr><tr><td>

sn\_schedule\_optim.solution\_processor\_packet\_size

</td><td>

Packet size to group events for solution processing \(task updates\).Sets the packet size for grouping events in solution processing, defining the capacity of each custom queue. It aims to distribute solution processing as widely as possible across the available custom queues specified in sn\_schedule\_optim.solution\_processor\_number\_of\_queues."

-   Type: Integer
-   Default value: 10

</td></tr><tr><td>

sn\_schedule\_optim.map\_vendor\_call\_types

</td><td>

Controls whether a synchronous or asynchronous call type is made to the map vendor. Changing the default value of sync to async can improve performance and may result in more outbound requests.-   Type: String
-   Default value: "beans": "sync"

</td></tr><tr><td>

sn\_fsm\_map\_integr.logging.verbosity

</td><td>

Captures additional logs for troubleshooting purposes. It is used for integration calls to map providers such as Beans.ai or Google, providing detailed insights to help diagnose and resolve issues.-   Type: Choice
-   Default value: info

</td></tr><tr><td>

sn\_schedule\_optim.qualifier\_data\_agent\_entity\_split

</td><td>

Indicates how many sets of agents will be processed simultaneously in an optimization run, improving performance.-   Type: Non-zero integer
-   Default value: 2

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_1.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_1.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_1.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_2.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_2.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_2.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_3.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_3.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_3.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_4.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_4.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_4.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_5.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_5.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_5.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_6.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_6.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_6.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_7.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_7.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_7.-   Type: True/False
-   Default value: False

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_8.claim\_limit

</td><td>

Specifies the number of break processing events in a single background transaction when updating technician schedule attributes such as travel duration and travel home duration.-   Type: Integer
-   Default value: 100

</td></tr><tr><td>

com.glide.event\_manager.sn\_schedule\_optim.event\_attr\_queue\_8.even.load.distribution.enabled

</td><td>

Controls balanced events load distribution for custom queue sn\_schedule\_optim.event\_attr\_queue\_8.-   Type: True/False
-   Default value: False

</td></tr></tbody>
</table>**Note:** The 'maint' role is required to edit any performance-related properties. This role is exclusive to internal users. Contact support to make changes.

**Parent Topic:**[Schedule Optimization components](schedule-optimization-components.md)

**Related topics**  


[Configuring Schedule Optimization](../concept/schedule-optimization-engine.md)

[Optimizing technician schedules at set intervals throughout the day](../task/optimize-your-schedules-intraday.md)

[Configuring log levels for detailed optimization analysis](../task/configuring-log-levels-for-detailed-optimization-analysis.md)


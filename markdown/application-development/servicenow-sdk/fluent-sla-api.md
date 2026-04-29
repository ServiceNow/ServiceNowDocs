---
title: Service Level Agreement API - ServiceNow Fluent
description: The Service Level Agreement API defines service level agreements \[contract\_sla\] that set the amount of time for a task to reach a specified condition, ensuring that tasks are resolved according to the service levels agreed between a service provider and customer.Create an SLA definition \[contract\_sla\] that controls the timing, conditions, workflows, and other information required to create and progress task SLAs.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api]
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Service Level Agreement API - ServiceNow Fluent

The Service Level Agreement API defines service level agreements \[contract\_sla\] that set the amount of time for a task to reach a specified condition, ensuring that tasks are resolved according to the service levels agreed between a service provider and customer.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about SLAs, see [Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Sla object

Create an SLA definition \[contract\_sla\] that controls the timing, conditions, workflows, and other information required to create and progress task SLAs.

<table id="table_sla_object" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. A name for the SLA definition.

</td></tr><tr><td>

table

</td><td>

String

</td><td>

The name of the table to which the SLA applies. Default: incident

</td></tr><tr><td>

type

</td><td>

String

</td><td>

The type of service level agreement. The type is used for reporting purposes only. Valid values:

-   SLA: A service level agreement between a service provider and an external customer.
-   OLA: An operational level agreement between internal teams within the same organization.
-   Underpinning contract: A contract with an external vendor that underpins the service delivered to the customer.

 Default: SLA

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the SLA definition is active and can be matched against task records. Valid values:

-   true: The SLA definition is active.
-   false: The SLA definition is inactive and isn’t matched against task records.

Default: true

</td></tr><tr><td>

target

</td><td>

String

</td><td>

The stage of the task that the SLA measures. The target is used for filtering, searching, and reporting purposes only.Valid values:

-   response: The SLA measures the time to first respond to a task.
-   resolution: The SLA measures the time to resolve a task.

</td></tr><tr><td>

duration

</td><td>

Object

</td><td>

The time duration within which the task must reach the target condition. Use the `Duration()` function to specify the duration.This property is required if the value of the durationType property is empty.

Format:

```javascript
duration: Duration({ days: Number, hours: Number, minutes: Number, seconds: Number })
```

</td></tr><tr><td>

durationType

</td><td>

Reference or String

</td><td>

The sys\_id of a relative duration \[cmn\_relative\_duration\], such as Breach on Due Date or End of next business day, to use instead of a user-specified duration. To define a relative duration, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

relativeDurationWorksOn

</td><td>

String

</td><td>

The record type from which the relative duration is calculated.This property only applies if the value of the durationType property is set.

Valid values:

-   Task record: The relative duration is calculated from the task record.
-   SLA record: The relative duration is calculated from the SLA record.

 Default: Task record

</td></tr><tr><td>

schedule

</td><td>

Reference or String

</td><td>

The sys\_id of a schedule \[cmn\_schedule\] for the time periods during which the SLAs accumulate business time. To define a schedule, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).This property is required if the value of the scheduleSource property is `sla_definition`.

</td></tr><tr><td>

scheduleSource

</td><td>

String

</td><td>

The source from which the schedule is obtained.Valid values:

-   sla\_definition: The schedule is specified in the SLA definition using the schedule property.
-   task\_field: The schedule is obtained from a field on the task record specified with the scheduleSourceField property.
-   no\_schedule: No schedule is used, and the SLA runs continuously \(24x7\).

 Default: sla\_definition

</td></tr><tr><td>

scheduleSourceField

</td><td>

String

</td><td>

The field from the task that provides the schedule.This property is required if the value of the scheduleSource property is `task_field`.

</td></tr><tr><td>

conditions

</td><td>

Object

</td><td>

Encoded query conditions that control the timing of an SLA. For example, `'priority=1^state!=6'` matches tasks with a priority of 1 that aren’t in a closed state.For more information about SLA conditions, see [Create an SLA definition](https://www.servicenow.com/docs/access?context=t_CreateAnSLADefinition&version=australia&pubname=australia-it-service-management&ft:locale=en-US). For information about filter queries, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Format:

```javascript
conditions: {
  start: 'String',
  stop: 'String',
  pause: 'String',
  resume: 'String',
  reset: 'String',
  cancel: 'String',
}
```

</td></tr><tr><td>

advancedConditionType

</td><td>

String

</td><td>

The type of advanced condition logic to apply.Valid values:

-   none: No advanced condition logic is applied.
-   advanced: A custom advanced condition script is used.
-   advanced\_journal: Advanced condition logic based on journal entries is used.
-   advanced\_system: Advanced condition logic based on system events is used.
-   advanced\_journal\_and\_system: Advanced condition logic based on both journal entries and system events is used.

 Default: none

</td></tr><tr><td>

conditionType

</td><td>

String

</td><td>

The sys\_id of an SLA condition \[sla\_condition\_class\] that determines when transitions between different stages of each task SLA.

</td></tr><tr><td>

resetAction

</td><td>

String

</td><td>

The action to take on the current task SLA record when the reset condition is met.Valid values:

-   cancel: The current task SLA record is canceled and a new one is created.
-   complete: The current task SLA record is marked as complete and a new one is created.

 Default: cancel

</td></tr><tr><td>

whenTo

</td><td>

Object

</td><td>

Settings that control when a paused SLA resumes and when an SLA cancels.-   resume: The behavior that controls when a paused SLA resumes timing.

Valid values:

    -   on\_condition: The SLA resumes when the task record matches the condition defined with the resume property of the conditions object.
    -   no\_match: The SLA resumes when the task record no longer matches the pause condition defined with the pause property of the conditions object.
Default: on\_condition

-   cancel: The behavior that controls when an active SLA is canceled.

Valid values:

    -   on\_condition: The SLA is canceled when the task record matches the condition defined with the cancel property of the conditions object.
    -   no\_match: The SLA is canceled when the task record no longer matches the start condition defined with the start property of the conditions object.
    -   never: The SLA is never canceled regardless of task record state.
Default: on\_condition


 Format:

```javascript
whenTo: {
  resume: 'String',
  cancel: 'String',
}
```

</td></tr><tr><td>

retroactive

</td><td>

Object

</td><td>

Settings that control whether the SLA start time is set to a point in the past based on a specified field value.-   start: Flag that indicates whether retroactive start is enabled. When enabled, the SLA start time is set to the value of the field specified in setStartTo rather than the time when the start condition was first met.

Default: false

-   setStartTo: The field on the task record whose value is used as the SLA start time when retroactive start is enabled. This property is required if the value of the start property is true.
-   pause: Flag that indicates whether retroactive pause is enabled when retroactive start is active. When enabled, any time that the task was in a paused state before the SLA was attached is subtracted from the elapsed time.

Default: true


Format:

```javascript
retroactive: {
  start: Boolean,
  setStartTo: 'String',
  pause: Boolean,
}
```

</td></tr><tr><td>

timezoneSource

</td><td>

String

</td><td>

The source from which the time zone for SLA calculations is obtained. Valid values:

-   task.caller\_id.time\_zone: The time zone of the caller on the task record.
-   task.caller\_id.location.time\_zone: The time zone of the caller's location on the task record.
-   task.cmdb\_ci.location.time\_zone: The time zone of the configuration item's location on the task record.
-   task.location.time\_zone: The time zone of the location on the task record.
-   sla.timezone: The time zone specified with the timezone property.

 Default: task.caller\_id.time\_zone

</td></tr><tr><td>

timezone

</td><td>

String

</td><td>

The time zone to use for SLA calculations, such as `US/Pacific`.This property is required if the value of the timezoneSource property is `sla.timezone`.

</td></tr><tr><td>

overrides

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of another SLA definition \[contract\_sla\] that this SLA definition overrides.

</td></tr><tr><td>

workflow

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a workflow \[wf\_workflow\] to run when the SLA reaches a milestone or breaches. To define a workflow, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

flow

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a flow \[sys\_hub\_flow\] to run when the SLA reaches a milestone or breaches. To define a flow, use the [Flow API - ServiceNow Fluent](fluent-flow-api.md#).Default: Default SLA flow \(828f267973333300e289235f04f6a7a3\)

</td></tr><tr><td>

vendor

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a company \[core\_company\] that is the vendor for an underpinning contract SLA. To define a company, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

domainPath

</td><td>

String

</td><td>

The domain path that determines which domain owns the SLA in a multi-domain environment.Default: The global domain \(/\)

</td></tr><tr><td>

enableLogging

</td><td>

Boolean

</td><td>

Flag that indicates whether debug logging is enabled for the SLA definition.Valid values:

-   true: Debug logging is enabled.
-   false: Debug logging is turned off.

Default: false

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { Sla, Duration } from '@servicenow/sdk/core'

Sla({
    $id: Now.ID['incident-p1-resolution'],
    name: 'P1 Incident Resolution',
    table: 'incident',
    target: 'resolution',
    duration: Duration({ hours: 4 }),
    schedule: 'b1992362eb601100fcfb858ad106fe16',
    conditions: {
        start: 'priority=1',
        stop: 'state=6',
        pause: 'state=3',
        resume: 'state!=3',
    },
    whenTo: {
        resume: 'on_condition',
    },
    resetAction: 'cancel',
})
```


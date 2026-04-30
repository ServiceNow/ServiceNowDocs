---
title: The incident events business rule
description: The incident events business rule comes with the system and defines a number of events that can be triggered by different actions in the Incident table.
locale: en-US
release: yokohama
product: System Events
classification: system-events
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [System events reference, System Events, Configure core features, Administer the ServiceNow AI Platform]
---

# The incident events business rule

The incident events business rule comes with the system and defines a number of events that can be triggered by different actions in the Incident table.

![Incident events business rule snippet](../image/IncidentEvents.png "Incident events business rule")

This business rule defines several events, three of which are triggered after a record in the Incident table is inserted or updated. The first script is:

```
if (current.operation() != 'insert' && current.comments.changes()) {
gs.eventQueue("incident.commented", current, gs.getUserID(), gs.getUserName());
}
```

The condition in this script requires that a change be made to the **Comments** field in an existing \(not inserted\) incident record. If this condition is true, then the platform adds the `incident.commented` event to the event queue.

The second condition requires that a record be inserted before the event is added to the queue.

```
if (current.operation() =='insert') {
```

The third condition is true whenever the incident record is updated \(including updates to the **Comments** field, as specified by the first script\).

```
if (current.operation() == 'update')
```

The then part of each script, the gs.eventQueue function, adds the event to the event queue. This statement uses the following syntax, set off with braces:

```
gs.eventQueue("incident.updated", current, gs.getUserID(), gs.getUserName());
```

The gs.eventQueue function takes the following parameters:

|Field|Input Value|
|-----|-----------|
|Name|The name of the event triggered, set in quotation marks.|
|Record|The record referenced when the condition in the script evaluates to true. Usually this is expressed as current, meaning the current record the business rule is working on. If the business rule is being triggered as part of a scheduled job, use a GlideRecord argument in its place.|
|Parm 1|An optional parameter you can use to pass system or record information with the event. For example, the GlideSystem API call gs.getUserID\(\) passes the Sys ID of the user who acted on the current record as a string value. Other scripts can reference this string value as parm1 using the format `${event.parm1}`.|
|Parm 2|An optional parameter you can use to pass system or record information with the event. For example, the GlideSystem API call gs.getUserName\(\) passes the user name of the user who acted on the current record. Other scripts can reference this string values as parm2 using the format `${event.parm2}`.|

**Note:** The gs.EventQueue function works directly with the backend and therefore business rules that are called by gs.EventQueue\(\) are not invoked.

**Parent Topic:**[System events reference](system-events-reference.md)


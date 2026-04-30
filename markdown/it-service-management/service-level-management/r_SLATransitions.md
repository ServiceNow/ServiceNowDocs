---
title: SLA transitions
description: SLA records pass through a series of transitions during processing.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Service Level Management, IT Service Management]
---

# SLA transitions

SLA records pass through a series of transitions during processing.

The following transitions exist for an SLA:

-   Attach: when an SLA is created and bound to a task.
-   Pause: when an SLA should temporarily stop tracking time.
-   Resume: when an SLA should resume tracking elapsed time.
-   Complete: when an SLA is marked complete.
-   Reattach: when an SLA is marked completed and a new copy is reapplied.
-   Cancel: when an SLA is cancelled.

SLA conditions determine what action is performed on a task SLA record.

|SLA condition|Resultant action on task SLA record|
|-------------|-----------------------------------|
|If Start condition matches and both Stop and Cancel conditions don't match|Attach|
|If Start condition matches, and **When to Cancel** is set to **Start conditions are not met**|Cancel if one or more of the specified start conditions no longer match.|
|If Start condition matches, and **When to Cancel** is set to **Cancel conditions are met**|Cancel when cancel conditions match.|
|Pause condition matches|Pause|
|If Pause condition matches, and **When to Resume** is set to **Pause conditions are not met**|Resume if one or more of the specified paused conditions no longer match.|
|If Pause condition matches, and **When to Resume** is set to **Resume conditions are met**|Resume if one or more of the specified resume conditions match.|
|Start and Reset|Reattach|
|Stop|Complete|
|Cancel|Cancel|

![SlA transition diagram](../image/SLAConditionsMethods.png "SLA condition methods when the default cancel and resume conditions are selected")

![SLA condition diagram](../image/SLM_SLAConsNotdefault.png "SLA Conditions Methods when the cancel and resume conditions are selected")

Each of these conditions is defined as a method within a Script Include, referenced by an SLA Conditions Rule record.

**Parent Topic:**[Service Level Management reference](../concept/service-level-management-reference.md)


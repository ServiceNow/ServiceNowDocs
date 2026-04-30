---
title: Assign equipment to a planned crew
description: Assign equipment to a planned crew to ensure they have tools for their work order tasks. Dispatchers can assign equipment through the ServiceNow AI Platform or Dispatcher Workspace. Crew leaders can assign equipment or modify their crews through the Now Mobile Agent application.Assign equipment to a planned crew through the ServiceNow AI Platform. A planned crew is a predefined group of agents and equipment.Assign equipment to a planned crew through Dispatcher Workspace. A planned crew is a predefined group of agents and equipment.Assign equipment to a planned crew through the Now Mobile Agent application. A planned crew is a predefined group of agents and equipment.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Scheduling and assigning equipment to tasks and crews, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Assign equipment to a planned crew

Assign equipment to a planned crew to ensure they have tools for their work order tasks. Dispatchers can assign equipment through the ServiceNow AI Platform or Dispatcher Workspace. Crew leaders can assign equipment or modify their crews through the Now Mobile Agent application.

**Parent Topic:**[Scheduling and assigning equipment to tasks and crews](../concept/assign-equipment-to-wot.md)

**Related topics**  


[Assign equipment to a task crew](create-a-task-crew-with-equipment.md)

[Assign an equipment instance to groups](assign-eq-instance-to-groups.md)

[Create a maintenance schedule for an equipment instance](create-maint-sched-for-eq-instance.md)

## Assign equipment to planned crews through the ServiceNow AI Platform

Assign equipment to a planned crew through the ServiceNow AI Platform. A planned crew is a predefined group of agents and equipment.

### Before you begin

Role required: wm\_ admin, wm\_dispatcher

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **My Crews**.

2.  Select the planned crew to add equipment to.

3.  In the **Equipment** related list, select **Add**.

4.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Equipment|The equipment instance.|
    |Effective from|Effective start date the equipment is assigned for.|
    |Effective to|Effective end date the equipment is assigned until.|
    |Active|Option that determines whether this instance is active and will appear on the dispatcher calendar.|

5.  Select **Submit**.


### Result

Equipment is added to the planned crew. This crew is eligible for tasks with equipment requirements that match the crew's equipment. An equipment instance can be assigned to only one crew at a time.

**Related topics**  


[Create crews in Field Service Management](create-crews-fsm.md)

## Assign equipment to planned crews through Dispatcher Workspace

Assign equipment to a planned crew through Dispatcher Workspace. A planned crew is a predefined group of agents and equipment.

### Before you begin

Role required: wm\_ admin, wm\_dispatcher

### Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click **Dispatcher Workspace**.

3.  Use either the dispatcher calendar or the dispatcher calendar sidebar to add equipment to a crew.

<table id="choicetable_pvs_vdv_dwb"><thead><tr><th align="left" id="d123568e350">

Method

</th><th align="left" id="d123568e353">

Action

</th></tr></thead><tbody><tr><td id="d123568e359">

**Dispatcher calendar**

</td><td>

1.  On the equipment instance to be assigned, select the More actions icon \(![More actions icon](../image/OverflowIcon.png)\).
2.  Select **Add to crew**.
3.  Select a crew to add the equipment to.


</td></tr><tr><td id="d123568e389">

**Dispatcher calendar sidebar**

</td><td>

1.  On the dispatcher calendar sidebar, select the Crews icon \(![Crew icon.](../image/crew-new.png)\).
2.  Select a crew to assign equipment to.
3.  On the **Equipment** tab, browse and select an equipment instance.


</td></tr></tbody>
</table>4.  Select **Update**.


### Result

Equipment is added to the planned crew. This crew is eligible for tasks with equipment requirements that match the crew's equipment. An equipment instance can be assigned to only one crew at a time.

**Related topics**  


[Create crews in Field Service Management](create-crews-fsm.md)

## Assign equipment to planned crews through the Now Mobile app

Assign equipment to a planned crew through the Now Mobile Agent application. A planned crew is a predefined group of agents and equipment.

### Before you begin

Role required: wm\_crew\_leader

### Procedure

1.  Navigate to **My work** &gt; **My crews**.

2.  Select a crew.

3.  Tap **Equipment**.

4.  Tap **Add equipment**.

5.  Select the equipment.

6.  Tap **Submit**.



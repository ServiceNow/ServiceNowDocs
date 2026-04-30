---
title: Work order task fields in the Field Service Contractor application
description: The Details tab in a work order task provides information about a task that helps an agent or manager to understand the task scope.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field Service Management reference, Field Service Management]
---

# Work order task fields in the Field Service Contractor application

The Details tab in a work order task provides information about a task that helps an agent or manager to understand the task scope.

|Field|Description|
|-----|-----------|
|Location|The geographical area where an agent executes the assigned task.|
|Initiated from|Parent task of the work order task.|
|Asset|Parts required to execute the task.|
|Scheduled start|Option to select date and time when the work on the task is expected to begin.|
|Estimated end|Estimated date when the work on the task will end. The date is automatically calculated based on the Scheduled start and Estimated work duration.|
|Estimated work duration|Option to select estimated time to complete the work. The duration can't exceed the total time of the window. This field is automatically set to an hour. If the task is in the Draft or Pending Dispatch states, you can edit this field.|
|Work type|Determines the type of work required to complete the task. Choices are as follows: Break Fix, Install, or Planned Maintenance|
|Under warranty|Indicates an existing warranty for one or more configuration items that are related with the task.|
|Description|Detail of the work to be performed at the work location. Give complete detail about the problem to avoid extra communication with the customer in the later stages of the work order life cycle.|
|Assignment group|Group that has the individual agent or vendor to complete the task. By default, this field shows the recommended assignment groups based on the location, asset, and skills for the task. If the field is empty, the system searches for the group covering the territory that includes the location of the task.|
|Assigned to|Shows the agent or manager who is currently assigned to the task|

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)


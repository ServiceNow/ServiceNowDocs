---
title: Task vs. request driven processing
description: All applications use either task-driven or request-driven processes for handling tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Facilities Service Management, Activate Facilities Service Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Task vs. request driven processing

All applications use either task-driven or request-driven processes for handling tasks.

Each application defaults to one or the other of these processing types, but you can switch between them as needed.

Task-driven processing means that the work order or request simply contains a list of tasks necessary for completing the overall work. When a work order record is created, an associated task record is automatically created. A request must have at least one task, and more tasks can be defined to handle all aspects of the request. As tasks are performed and completed, the request transitions through a series of states. After the last task is closed, the request automatically transitions to closed.

Request-driven processing means that tasks are assigned to a request, but closing all the tasks does not automatically close the request. A request does not require any tasks and can be opened and closed independently. Any tasks can be transitioned and assigned independently and to different agents than specified on the request. Even if all tasks are closed, the request can remain open and continue to be worked on. However, the request cannot be closed until all tasks are also closed. In request-driven processing, state transitions are based solely on the request.

**Parent Topic:**[Configure Facilities Service Management](../../facilities-service-management/task/t_ConfigureFacilities.md)


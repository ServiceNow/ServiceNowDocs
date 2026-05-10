---
title: Execute work order tasks
description: After the dispatcher dispatches work order tasks, the ServiceNow system automatically sends the tasks to the assigned agent's queue.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Execute work order tasks

After the dispatcher dispatches work order tasks, the ServiceNow system automatically sends the tasks to the assigned agent's queue.

The agent has the option to accept or reject the work order task. If the agent accepts the task, the task state automatically changes to **Accepted**. If the agent who accepts assignment of a work order task does not yet have a personal stockroom, the system creates a personal stockroom automatically with the name **Personal stockroom - &lt;first and last name of agent&gt;**. If the wm\_agent role is ever removed from the user, the personal stockroom is deleted.

The examples in this page illustrate the use of tasks with work orders; however, tasks can be used with any [Service Management application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/c_ServiceManagement.md). The ServiceNow system provides an agent with these methods for managing work order tasks:

-   [Agent task map](../task/t_ExecuteATaskFromTheAgentMap.md): The agent task map displays an agent's location and the location of that agent's tasks for the day in a familiar Google Map. The agent map is available when the Service Management Geolocation plugin \(com.snc.service\_management.geolocation\) is active. This map allows for the general scheduling of tasks and provides estimates of an agent's location. Precise agent locations and some automatic features are available when your organization purchases a [Google Maps API for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_Geolocation.md) key and enters it into the system.
-   [Task queue](../task/t_ExecuteATaskFromTheQueue.md): It the task map is not available, an agent can manage assigned tasks and their schedule directly from a queue accessed from the application navigator.


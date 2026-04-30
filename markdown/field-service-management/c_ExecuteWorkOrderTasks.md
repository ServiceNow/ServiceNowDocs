---
title: Execute work order tasks
description: After the dispatcher dispatches work order tasks, the ServiceNow system automatically sends the tasks to the assigned agent's queue.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Execute work order tasks

After the dispatcher dispatches work order tasks, the ServiceNow system automatically sends the tasks to the assigned agent's queue.

The agent has the option to accept or reject the work order task. If the agent accepts the task, the task state automatically changes to **Accepted**. If the agent who accepts assignment of a work order task does not yet have a personal stockroom, the system creates a personal stockroom automatically with the name **Personal stockroom - &lt;first and last name of agent&gt;**. If the wm\_agent role is ever removed from the user, the personal stockroom is deleted.

The examples in this page illustrate the use of tasks with work orders; however, tasks can be used with any [Service Management application](https://www.servicenow.com/docs/access?context=c_ServiceManagement&version=xanadu&pubname=xanadu-service-management-for-the-enterprise&ft:locale=en-US). The ServiceNow system provides an agent with these methods for managing work order tasks:

-   [Agent task map](../task/t_ExecuteATaskFromTheAgentMap.md): The agent task map displays an agent's location and the location of that agent's tasks for the day in a familiar Google Map. The agent map is available when the Service Management Geolocation plugin \(com.snc.service\_management.geolocation\) is active. This map allows for the general scheduling of tasks and provides estimates of an agent's location. Precise agent locations and some automatic features are available when your organization purchases a [Google Maps API for Business](https://www.servicenow.com/docs/access?context=c_Geolocation&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) key and enters it into the system.
-   [Task queue](../task/t_ExecuteATaskFromTheQueue.md): It the task map is not available, an agent can manage assigned tasks and their schedule directly from a queue accessed from the application navigator.

-   **[Accept or reject a work order task](../task/t_AcceptOrRejectAWorkOrderTask.md)**  
Accept a work order task if you are ready to work on that task. Reject the task and provide a reason if you cannot work on that task.
-   **[Execute a task from the agent map](../task/t_ExecuteATaskFromTheAgentMap.md)**  
As an agent, you can accept or reject tasks assigned to you using features in the agent task map, or take on unassigned tasks near you if your schedule permits.
-   **[Execute a task from the queue](../task/t_ExecuteATaskFromTheQueue.md)**  
If the agent task map is not used in your organization, you can manage assigned tasks from the task queue.
-   **[Onsite arrival and check-in](../../field-service-management/reference/onsite-arrival-and-check-in.md)**  
The Onsite Arrival and Check-in process ensures accurate task location confirmation and effective time tracking.
-   **[Record an incidental expense](../task/t_RecordAnIncidentalExpense.md)**  
Record incidental expenses associated with your business travel through the Field Service application to execute work order tasks.
-   **[Complete a questionnaire for a work order or task](../../field-service-management/task/complete-wo-or-task-questionnaire.md)**  
Complete a questionnaire for a work order or work order task. You can access and complete questionnaires from the Work Order or Work Order Task forms.
-   **[Close a work order task as complete](../task/t_CloseAWorkOrderTaskAsComplete.md)**  
Only agents can close work order tasks assigned to them.
-   **[Close a work order task as incomplete](../task/t_CloseAWorkOrderTaskAsIncomplete.md)**  
Close a work order task as incomplete if there is work pending on the task.
-   **[Cancel a work order task](../task/t_CancelAWorkOrderTask.md)**  
The **Cancel Task** option is appropriate if a work order task is no longer necessary or is a duplicate of another work order task.
-   **[View asset usage](../task/t_RecordAssetUsage.md)**  
The Field Service Management application tracks the consumable and non-consumable parts that are used or changed during the execution of work order tasks.

**Parent Topic:**[Managing work orders and work order tasks](../../field-service-management/concept/managing-work-orders.md)


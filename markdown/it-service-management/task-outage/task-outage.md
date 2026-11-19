---
title: Task Outage
description: CI unavailability, or outage, is the actual down time of a CI. Whenever there is an outage for any of the CI items, the outage information is stored in the Outage \[cmdb\_ci\_outage\] table. The Task-Outage table \[task\_outage\] maintains the mapping between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/task-outage/task-outage.html
release: zurich
product: Task Outage
classification: task-outage
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IT Service Management]
---

# Task Outage

CI unavailability, or outage, is the actual down time of a CI. Whenever there is an outage for any of the CI items, the outage information is stored in the Outage \[cmdb\_ci\_outage\] table. The Task-Outage table \[task\_outage\] maintains the mapping between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.

-   **[Activate Task-Outage Relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/task-outage/activate-task-outage.md)**  
Activate the Task-Outage Relationship plugin \(com.snc.task\_outage\) to track outage duration.
-   **[Add the Outage UI action to another task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/task-outage/t_AddTheUIActionToAnotherTaskForm.md)**  
By default, the **Create Outage** UI action is available on the incident and problem forms, and can be added to other task forms. For new instances from Jakarta only, this feature is also available on the change request form.
-   **[Associate a task with an outage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/task-outage/t_AssociateATaskToAnOutage.md)**  
You can associate multiple tasks with a defined outage.
-   **[Create an outage from a task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/task-outage/t_CreateAnOutageFromATask.md)**  
Create an outage from a task record to understand the down time of a configuration item.
-   **[Domain separation and task outage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/task-outage/domain-separation-task-outage.md)**  
Domain separation is supported in task outage. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/r_ITServiceManagement.md)


---
title: Change requests and project tasks
description: Large-scale changes approved by your change approval board \(CAB\) require new or existing projects to be implemented.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Change requests and project tasks

Large-scale changes approved by your change approval board \(CAB\) require new or existing projects to be implemented.

To bridge the gap between change management and project management, the instance allows you to link one or more change requests to a project task. You can link an existing change request to a project task or create a new change request directly from a project task.

When you link a project task to a change request record, a new project task link record is created. It provides the actual link between the project task record and the change request record. The project task link copies all attributes of the change request record. It then becomes a child task of the project task that you linked to the change request. The rules that govern the relationship between the project task and the project task link are the same as the rules for all parent and child tasks.

![Project tasks linked to change requests](../image/Project_change1.png "Project tasks linked to change requests")

**Note:** A project task cannot have both task link records and child project tasks. When a project task is linked to a change request, you cannot also create child tasks for that project task. Likewise, when a project task has child tasks, you cannot link the parent project task to a change record.

The project task link record is read only. You can view the project task links from a related list on the Project Task form.

![Project Tasks Links related list](../image/Project_task_links_related_list.png "Project Tasks Links related list")

You can also link multiple change requests to a single project task. In this case, a project task link record is created for each link and all the project task link records become child tasks of the project task.

![Project tasks links](../image/Project_change2.png "Project tasks links")

-   **[Change request project task relationship](../reference/r_ChangeReqProjTaskRelship.md)**  
The rules that apply to all parent-child tasks also govern the relationship between project task and the project task link.
-   **[Link change requests to a project task](../task/t_LinkChangesToAProjectTask.md)**  
Link change requests to tasks on the Project Task form. You can link change requests only to project tasks that have no child tasks.

**Parent Topic:**[Project tasks](c_ProjectTasks.md)

**Related topics**  


[Project task relationships and dependencies](c_ProjectTaskRelationDepend.md)

[Scheduling conflicts between project tasks](scheduling-conflicts.md)

[Create a project task](../task/t_CreateAProjectTask.md)

[Create a milestone](../task/t_CreateMilestones.md)

[Project task checklists](c_project-task-checklists.md)

[Accept or reject project task notifications](../task/accept-project-task-notifications.md)

[Task resources](c_TaskResources.md)


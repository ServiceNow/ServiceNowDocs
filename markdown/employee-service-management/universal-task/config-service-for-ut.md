---
title: Configuring your service for Universal Task
description: You can configure the UI actions and related lists for the Universal Task application so that you can view and create universal tasks for your service. Services are the various departments in your organization, such as IT, HR, and Legal.
locale: en-US
release: yokohama
product: Universal Task
classification: universal-task
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Configuring your service for Universal Task

You can configure the UI actions and related lists for the Universal Task application so that you can view and create universal tasks for your service. Services are the various departments in your organization, such as IT, HR, and Legal.

1.  [Assign Universal Task admin role](../task/assign-ut-admin-role.md)  
Assign the sn\_uni\_task.admin role to the application administrators so that they can integrate and configure Universal Task. Roles control access to features, capabilities, and data.
2.  [Create UI actions for your service with Universal Task](../task/config-uiactions-for-ut.md)  
Create UI actions for your service so that agents can create universal tasks.
3.  [Add a Universal Task related list](../task/create-relatedlist-ur.md)  
Add a Universal Task related list to a service-specific form in both the ServiceNow AI Platform and Agent Workspace to let agents view a universal task for the request.
4.  [Add a Task tab on the Standard Ticket page](../task/config-stdtktpage-for-ut.md)  
Add a Task tab on the Standard Ticket page to let employees view the tasks that are assigned to them by the agents.
5.  [Define the agent criteria for Universal Task](../task/ut-config-extn-point-agent.md)  
Define the criteria for an agent so that the agent can access the parent table for Universal Task. The default criteria is that agents must have write access to the parent table.
6.  [Configure Universal Task for your service](../task/config-ut-for-service.md)  
Configure the Universal Task application for your service so that you can create and assign tasks to employees.
7.  [Configure the catalog items for your service](../task/config-catalog-task.md)  
Filter the catalog items that you want to show in the Submit Catalog Item task for your service.
8.  [Configure the roles to view employee forms](../task/ut-config-empform-view-roles.md)  
Configure the roles to enable your agents to view the employee responses in the completed Universal Task employee forms.
9.  [Configure the extension points for Universal Task](../task/configure-extnsn-points.md)  
Provide the implementation for childTaskCancelled, childTaskCompleted, childTasksClosed of the scripted extension point to execute the custom logic of the service, when a universal task is canceled, completed, or closed.
10. [Display the universal tasks for a request in Now Mobile](../task/ut-mobile-config-tasktab.md)  
Display all the universal tasks that are assigned for a particular request by simply configuring the **Tasks** tab in Now Mobile.
11. [Hide the template bar on the Universal Task form](../task/ut-hide-template-bar.md)  
Hide the template bar for the Universal Task form because it does not include Universal Task templates.
12. [Remove the Universal Task admin role from the admin role](../task/ut-remove-admin-role.md)  
After system configuration, remove the Universal Task Admin role \(sn\_uni\_task.admin\) from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive information via forms, lists and UI.

**Parent Topic:**[Setting up and configuring Universal Task](set-up-universal-task.md)


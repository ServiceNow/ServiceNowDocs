---
title: Setting up work orders and tasks
description: When work is required, create a work order to provide information for the Field Service agents to fulfill the request. Create work order tasks to break down the tasks required to complete the work order.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Field Service Management]
---

# Setting up work orders and tasks

When work is required, create a work order to provide information for the Field Service agents to fulfill the request. Create work order tasks to break down the tasks required to complete the work order.

You can use Field Service Management and only set up work orders and work order tasks to start work. Or you can set up additional configurations to automate some of the process around creating and managing work orders and work order tasks.

## Configuration overview

The steps for setting up work orders and tasks are:

1.  [Configuring work orders](configure-work-orders.md)

    Configure Field Service Management to use a task-driven process, wherein each work order encapsulates a list of essential tasks. Upon the creation of a work order, a corresponding task record is instantly generated. Task-driven processing can provide structure and clarity for intricate projects.

    Work orders in Field Service Management store information about requested work, including customer names and addresses, locations where work is to be performed, and any associated configuration items. Work orders can include one or more tasks that contain specific details about the work to be performed, such as required agent skills or part requirements. Work orders are the driving force behind Field Service Management. They define what Field Service agents must do to complete their jobs.

2.  [Configuring work order tasks](configure-work-order-task.md)

    Categorize work orders are comprised of at least one, but usually multiple, work order tasks. You can categorize work order tasks by type so that work order tasks of the same type are consistent, like if a certain type of task always requires a specific assignment group. Additionally, you can require agents to complete questionnaires before, during, or after completing a task. For example, if you want agents to complete a safety checklist before starting a task, you can use questionnaires. Work order tasks also allow for automatic time recording that tracks and translates time worked on a task into a time card.

3.  \(Optional\) [Configuring Field Service Work Configurations](configuring-work-configs.md)

    Customize the information captured on a work order task to better suite similar but different workflows. For example, maintenance and installations can have a fixed cost associated with them, but break-fix tasks may need to capture additional information related to the cost and duration of the task. With Field Service work configurations, you can set up these task types to capture specific information.

4.  \(Optional\) [Configuring Planned Work Management](configuring-planned-work-management.md)

    Manage flexible work plans for any recurring activity that requires regular maintenance. For example, you can use planned Work management to schedule maintenance, inspections, or audits. You can install the Planned Work Management application \(com.snc.fsm\_planned\_work\_management\) if you have the admin role.

5.  \(Optional\) [Configuring the auto-population of access hours in a work order task](configuring-access-hours.md)

    Define default access hours for a work order task based on customer preferences such as account, location, or asset, enables the auto-population of the access hours for the task. For example, you can set the access hours for a business to guarantee that work order tasks are only assigned to the location when it’s open. You can activate the Field Service Management Access Hours Management plugin \(com.snc.fsm\_access\_hours\) for Field Service Management if you have the admin role.

6.  \(Optional\) [Activate linear assets support in Field Service Management](../task/activate-linear-assets.md)

    Enable effective management of assets like roads, telephone lines, or fiber cables. You can enable the Field Service Management application to support linear assets by activating the Enterprise Asset Management plugin \(com.sn\_eam\) if you have the admin role.

7.  \(Optional\) [Configuring Playbooks for Field Service Management](configuring-playbooks-fsm.md)

    Enable agents to manage the life cycle of work order tasks by guiding them through sequences of activities. Playbooks show detailed workflows associated with a specific type of work order task and the activities that must be completed to resolve that task.

8.  \(Optional\) [Configuring Field Service Management Customer Experience](Configuring-cust-exp.md#)

    Provide customers with timely updates about their reported issues, enabling them to track the location of agents and provide agent feedback. You can install the Field Service Management Customer Experience plugin \(com.snc.fsm\_customer\_experience\) if you have the wm\_admin role.

9.  \(Optional\) [Request task management](../../planning-and-policy/concept/c_RequestTasksMgmt.md)

    Split requests into separate tasks. This can be helpful if you want to assign different parts of a task to different people, assign parts of a task to people in different locations, or schedule parts of a task to be completed at different times.

10. \(Optional\) [Configuring Field Service Quality Management](config-quality-mgmt.md)

    Add the "Reviewer" role to Field Service Management. The reviewer can review tasks and provide feedback. You can install the Field Service Management plugin \(com.sn\_fsm\_quality\) if you have the wm\_admin role.


**Note:** As Field Service Management is built on ServiceNow Mobile Platform, its access is primarily role-driven. The roles are configured to be more flexible and less restrictive.

Users with the wm\_agent role can work with operational records and perform actions such as update certain task fields, record the task time, and cancel tasks even if they are not assigned to them, unless restricted by Access Control Lists \(ACL\) or query rules. To enforce stricter controls on the wm\_agent role, you can:

-   Enforce access control at record and field levels. For more information, see [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   Apply pre-query filtering. For more information, see [CSM Query Rules](https://www.servicenow.com/docs/access?context=csm-query-rules&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).
-   Apply dynamic filtering. For more information, see [Before Query business rules](https://www.servicenow.com/docs/access?context=bp-before-query-business-rules&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   Apply restrictions at the UI level. For more information, see [Using UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

To enforce strict separation between different departments or to separate sensitive data, domain separation is recommended. It ensures data isolation, domain-specific access controls, and controlled data sharing.


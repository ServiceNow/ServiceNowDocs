---
title: Task Plan Templates in Care Team Work Management
description: Understand how task plan templates can be leveraged from Customer Service Management in Care Team Work Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Task Plan Templates in Care Team Work Management

Understand how task plan templates can be leveraged from Customer Service Management in Care Team Work Management.

Care Team Work Management enables for the creation of custom task plan templates to define the repeatable tasks and records that must be created for care team agents. When the template is applied, these tasks and records are automatically created.

For information about how task plan templates work, see [Task Plan Templates](https://www.servicenow.com/docs/access?context=task-plan-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

## Creating task plans for Care Team Work Management

When creating a task plan template, you must create a **Task plan configuration** for your task plans to pre-fill information into task plan template fields.

For more information, see [Create a task plan template configuration](https://www.servicenow.com/docs/access?context=task_plan_template_configurations&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

You can create one or more template items, such as a task or record, for a task plan template. When the task plan template is applied, these records are automatically created. For more information, see [Create a template item](https://www.servicenow.com/docs/access?context=create-task-plan-template-item&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

Multiple template items can be created from the same configuration. For example, multiple Orchestration tasks can be generated from one single configuration. Or, a task plan for a medical device audit might be configured to generate Biomed cases as child cases to the parent Orchestration case.

The following additional healthcare operations case types are available to be configured as template items under Orchestration cases:

-   Healthcare Operations cases
-   Biomed cases
-   Facilities cases
-   EVS cases
-   Healthcare IT cases

## Playbook Record Generator

For a task plan template to open in a Playbook, a Playbook Record Generator must be associated in the Task Plan Template Configuration.


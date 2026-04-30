---
title: Use Playbooks in Project workspace
description: Plan your project stages and assign specific actions to each stage using Playbooks.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Use Playbooks in Project workspace

Plan your project stages and assign specific actions to each stage using Playbooks.

## Before you begin

Role required: admin or project\_manager

As a system administrator, ensure that a playbook is activated or created before use.

## About this task

A playbook defines the standard stages of a project \(for example, Initiation, Planning, Execution, Monitoring, and Closure\) and includes activities or action items to complete at each stage.

There are two playbooks for Project Workspace. This task topic follows the Project default playbook. It’s a PMBOK standard playbook comprising five stages: Initiation, Planning, Execution, Monitoring and Delivering, and Closure. Each stage consists of activities, action items, or steps that guide the project manager in successfully completing the project.

You can view the **Playbook** menu only if a playbook is active and the project matches the trigger condition defined for that playbook. The playbook is displayed only when the project meets the defined trigger conditions. Two playbooks are available in Workflow Studio for Project Workspace.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and [Create a project](create-project-from-project-workspace.md).

2.  To use an existing playbook or create a playbook, follow these steps:

    -   To create a new playbook, you can define the trigger condition in Workflow Studio. For more information, see [Triggers](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
    -   To use an existing playbook:

        1.  Select **Playbooks** from the menu.
        2.  Select **Mark complete**, or **Skip**, or **Save** for each stage.
        **Note:**

        You can select **Save** to save the stage or **Skip** to skip the stage and move to next stage. When you select **Mark Complete** or **Skip**, the activity becomes read-only. Once all activities in a stage are completed or skipped, the stage is marked complete. Use the Restart option \(available at both activity and stage levels\) to revisit or edit completed or skipped activities.

    For more information on how to use playbooks, see [Building playbooks](https://www.servicenow.com/docs/access?context=building-a-process&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) and [Designing playbooks](https://www.servicenow.com/docs/access?context=playbook-experience-admins&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


**Parent Topic:**[Managing projects with Project Workspace](../concept/use-projects-pw.md)

**Related topics**  


[Running playbooks](https://www.servicenow.com/docs/access?context=playbook-agents-and-fulfillers&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

[Playbooks across ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=integrating-with-process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

[Playbooks reference](https://www.servicenow.com/docs/access?context=process-automation-designer-reference&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

[Playbooks configuration](../concept/configure-playbooks-pw.md)

[Playbooks in Project Workspace](../concept/playbooks-in-pw.md)


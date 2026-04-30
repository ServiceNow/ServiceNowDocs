---
title: Playbooks configuration
description: Configure playbooks to organize project workflows, maintain consistency, and keep projects on track.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: concept
last_updated: "2025-10-14"
reading_time_minutes: 1
breadcrumb: [Configuring projects with Project Workspace, Configure, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Playbooks configuration

Configure playbooks to organize project workflows, maintain consistency, and keep projects on track.

Define a trigger condition in Workflow Studio to use a Playbook, either by selecting an existing one or creating a Playbook. For more information on how to configure a playbook, see.

In Project Workspace, Playbooks are triggered by record creation, record update, or both. For example, a Playbook created for projects is associated with project records, and the Playbook tab appears when a project meets the trigger condition. For more information on how to configure a playbook, see [Configuring playbooks](https://www.servicenow.com/docs/access?context=setting-up-process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

There are two pre-defined project management playbooks available in the Workflow studio:

-   Project default
-   Stage-gate default

To configure playbooks, perform these tasks:

1.  Navigate to **Workflow Studio** and select **Playbooks**.
2.  Create and configure playbooks as per your requirement. For more information, see [Create and configure playbooks](https://www.servicenow.com/docs/access?context=setting-up-process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
3.  Activate one of the two pre-defined playbooks for the Project Workspace and define an appropriate trigger condition. For more information, see [Activate playbooks](https://www.servicenow.com/docs/access?context=activate-process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) and [Triggers](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

Multiple playbooks can be enabled at a time, and the trigger should be defined in such a way that each project is mapped to only one type of playbook. To activate a playbook, see [Activate playbooks](https://www.servicenow.com/docs/access?context=activate-process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Note:**

When a project template is applied or project is created from a demand, the project information is automatically copied into the project record and reflected in the Playbook.

**Parent Topic:**[Configuring projects with Project Workspace](../../pw-resource-management/concept/configure-projects-pw.md)

**Related topics**  


[Building playbooks](https://www.servicenow.com/docs/access?context=building-a-process&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

[Designing playbooks](https://www.servicenow.com/docs/access?context=playbook-experience-admins&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

[Playbooks in Project Workspace](playbooks-in-pw.md)

[Use Playbooks in Project workspace](../task/use-playbooks-pw.md)


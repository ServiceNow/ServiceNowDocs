---
title: Getting started with Playbooks
description: Learn the basics of designing an automated process for your organization. Get an overview of how Workflow Studio Playbooks work in the ServiceNow AI Platform.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Building playbooks, Use, Workflow Studio, Build workflows]
---

# Getting started with Playbooks

Learn the basics of designing an automated process for your organization. Get an overview of how Workflow Studio Playbooks work in the ServiceNow AI Platform®.

## Playbooks

Playbooks in Workflow Studio are ServiceNow AI Platform representations of your manual cross-enterprise workflows. By creating a Workflow Studio playbook on the platform, you're digitizing these workflows. A playbook in Workflow Studio has two dimensions: the playbook and their associated process executions.

-   **Playbooks**

    A playbook is where a playbook owner configures and organizes multiple instances of Workflow Studio content into a coherent business process. A playbook consists of a trigger and a sequence of stages, which are made up of a sequence of activities.

-   **[Process executions](process-executions.md)**

    A process execution is a single, runtime instance of a playbook.


## Building a playbook

When you design your business process in Playbooks, you're creating a playbook.

Each playbook consists of a trigger as well as stages and activities. Triggers define the conditions that, when met, start running your playbook. Stages and activities represent stages and individual steps in your overall business process. In the Playbooks design environment, you can organize these stages and Playbooks into a sequence that reflects how your business process runs.

When you're done creating your playbook, activate it so that it runs when triggered.

![Create a digitized representation of your business process, known as a playbook.](../images/getting-started-process-definition.png)

## What happens when a playbook runs

When your activated playbook is triggered, the system creates a process execution, which represents a single, running instance of your playbook.

When your playbook starts running, a process execution is created. The system runs each activity in your playbook until the process execution is complete. As each activity runs, automated record operations occur on the ServiceNow AI Platform.

If an administrator has set up Playbook Experience for your playbook, then agents and fulfillers can run the playbook. Agent or fulfillers go through each activity in the playbook, which is associated with a record in a Workspace.

In summary, your playbook runs when:

1.  The system creates a process execution.
2.  Playbook Experience is configured and the playbook is rendered for agents.
3.  Automated operations on records that are associated with your process execution occur on the ServiceNow AI Platform.

![When your activated playbook is triggered, the system creates a process execution, a playbook can render for agents, and automated record operations on the ServiceNow AI Platform occur.](../images/getting-started-process-execution.png)

## Learn more about Playbooks

If you're ready to start digitizing your business process with Playbooks in Workflow Studio, try checking out these resources:

-   [Design your first automated process](../task/design-automated-process.md)
-   [Create a playbook](../task/create-process-definition.md)

-   **[Design an automated process](../task/design-automated-process.md)**  
Transform an example manual business process into a well-designed, automated process that runs on the ServiceNow AI Platform®.

**Parent Topic:**[Building playbooks](building-a-process.md)


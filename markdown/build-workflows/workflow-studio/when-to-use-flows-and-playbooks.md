---
title: When to use flows and playbooks
description: Use these general guidelines to determine when to create a flow or a playbook.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Playbooks, Explore, Workflow Studio, Build workflows]
---

# When to use flows and playbooks

Use these general guidelines to determine when to create a flow or a playbook.

## When to use flows

Flows, subflows, and actions are the basic building blocks of process automation. Flows run when their trigger conditions are met, and each flow in turn runs a sequence of actions, flow logic, and subflows. The actions, flow logic, and subflows within a flow are what create and update data.

A flow is a good fit for process automations that met these criteria.

-   **Expect few to no manual user interactions**

    As long as a flow has the input data it needs, it can run to completion without any user interaction. Some flow logic and actions require users to make record changes, but a flow can automatically pause until its wait conditions are met. Process automations that depend on user interactions such as reading a knowledge base article, going through a checklist, and gathering feedback are harder to manage with flows. Flows don't directly provide any UI elements for users to interact with. Flows depend on users knowing how to find an existing UI and making any needed changes. For example, a record-based flow depends on a user making a change in a specific record such as a case or an incident.

-   **Expect to run at high volumes**

    An instance can run hundreds to thousands of flows per second. With flow reporting being disabled by default, an instance can run a high volume of flows before it sees any performance impact. If you expect to run a process automation at high volumes, a flow is a good fit over a playbook because it requires less overhead and system resources.

-   **Expect to run few to no subflows**

    The more subflows a flow calls, the more difficult it becomes to manage from the flows interface. While you can use conditional flow logic or a decision table to choose a subflow to run, playbooks offer a better user experience for running a sequence of subflows.


## When to use playbooks

Playbooks are built on activities, which use prebuilt flows, subflows, and actions as their building blocks.

A playbook is a good fit for process automations that met these criteria.

-   **Expect several manual user interactions**

    Playbooks provide UI elements for users to interact with. The playbook experience guides users to make any changes required to advance the playbook.

-   **Expect to run at low volumes**

    Playbooks require more system resources to run because they generate UI elements and store more execution details.

-   **Expect to run many subflows**

    Playbooks offer a better user experience for running a sequence of subflows.


**Parent Topic:**[Exploring playbooks](../../process-automation-designer/concept/process-automation-designer.md)


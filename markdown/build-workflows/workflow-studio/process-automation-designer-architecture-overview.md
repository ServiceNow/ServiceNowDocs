---
title: Playbook Experience
description: Understand how Workflow Studio Playbooks work in the ServiceNow AI Platform to automate cross-functional processes and consolidate them into task-oriented views for your end users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/process-automation-designer-architecture-overview.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Playbook, Explore, Workflow Studio, Build workflows]
---

# Playbook Experience

Understand how Workflow Studio Playbooks work in the ServiceNow AI Platform® to automate cross-functional processes and consolidate them into task-oriented views for your end users.

**All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks** is the design environment where playbook owners build playbooks. Meanwhile, the runtime experience is where end users, such as playbook agents, follow the playbook to complete a business process. To learn more about the Playbook designer, see [Playbook builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/exploring-process-automation-designer.md).

## Runtime experience

Workflow Studio produces these runtime components for Playbooks:

-   **Process executions**

    A process execution stores the details of running a playbook in a context record. You can use a process execution to troubleshoot and verify that playbooks run as expected.

-   **Activity executions**

    An activity execution stores the details of running an activity instance in a context record. You can use an activity execution to troubleshoot and verify that playbooks run as expected.

-   **Playbook runtime**

    Playbook runtime is when a playbook runs for an agent or fulfiller. A playbook runs for agents only after Playbook Experience administrators configure how and where the playbook appears.


\[Omitted image "process-definition-runtime-processing.png"\] Alt text: Sequence of playbook processing.

During runtime for a playbook, your instance:

1.  Evaluates any conditions specified in the trigger definition and processes the trigger.
2.  Processes the [Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/system-events/events.md) and starts running the playbook in the background.
3.  Builds the automation plans from each activity into an entire process plan.
4.  Runs the process plan for your playbook.
5.  Stores the process execution information in the Process Execution \[sys\_pd\_context\] table.
6.  Provides data for the running playbook view that agents and fulfillers experience.

**Parent Topic:**[Exploring Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/process-automation-designer.md)


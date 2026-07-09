---
title: Exploring playbooks
description: Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. Build the underlying processes for playbooks that Playbook Experience agents and fulfillers use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/process-automation-designer.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Exploring playbooks

Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. Build the underlying processes for playbooks that Playbook Experience agents and fulfillers use.

**Note:**

Starting in the Xanadu release, the following updates were made:

-   Playbooks is now part of [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/workflow-studio.md). Workflow Studio gives you a streamlined way to author, configure, and monitor playbooks, flows, subflows, actions, and decision tables in one place.
-   Processes are now called Playbooks, though Playbook Experience remains a separate application that is not accessible from within Workflow Studio yet.
-   The core Playbooks builder in Workflow Studio is available with the ServiceNow AI Platform® by default, but the latest updates are available for download through the application in the ServiceNow® Store.

## Playbooks benefits

Workflow Studio Playbooks enables you, as a business playbook owner, to organize Workflow Studio content into unified and digitized cross-enterprise processes. With Playbooks, you gain these benefits:

-   Connect multiple flows and actions into an end-to-end business workflow.
-   Reuse existing Workflow Studio flows, subflows, or actions to automate playbook activities.
-   Organize playbook activities in a digitized task board or diagram interface.
-   Guide agents and fulfillers through complicated playbooks from start to finish, improving customer experience and task resolution. Build your playbooks in Workflow Studio, and then design and embed your Playbook Experience in legacy workspace, UI Builder, ServiceNow Mobile Platform, Service Portal, and more.
-   Consolidate separate business processes across the organization.
-   Define a consistent record life cycle from creation to completion.
-   Pass data between the activities and stages of a business process.
-   Specify the conditions and the order in which activities and stages run.
-   Visualize and manage the activities and stages of your process.

## Creating a well-designed playbook

The automated business processes that you design guide your end users and help them focus on the tasks and information that matter to them. A well-designed playbook can do these things:

-   Start up, or trigger, automatically for the types of records that your end users care about
-   Reuse activities from existing [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/workflow-studio.md) content
-   Has well-defined stages that end users can follow for a record
-   Clearly show the next steps that end users must take to move through a record's life cycle

## Playbooks content

Playbooks has these components:

-   **Playbooks**

    A playbook is a ServiceNow AI Platform® representation of a cross-enterprise business process for your organization. A playbook owner is responsible for creating and maintaining a playbook.

-   **Triggers**

    A trigger specifies when to start running your playbook.

-   **Stages**

    A stage is a grouped sequence of activities in a playbook. A playbook owner creates a stage to specify a logical grouping of activities. A stage in your overall business process.

-   **Activities**

    An activity defines the [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/workflow-studio.md) content that powers the playbook's automation. An activity can also specify the user-facing experience that the playbook produces when it runs.


For more information about how to use and navigate the Playbooks user interface, see [Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-process-automation-designer.md).

## Getting started

Before you get started with Playbooks, familiarize yourself with any features that your business uses to automate operations on the ServiceNow AI Platform, such as [flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-flows.md), [subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-subflows.md), and [actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-actions.md).

If you're a playbook owner who wants to learn the basics of digitizing your business process, check out the following resources:

-   [Get started with ServiceNow® Process Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/getting-started-process-automation.md)
-   [Get started with processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/getting-started-processes.md)
-   [Design your first automated process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/design-automated-process.md)
-   [View your process executions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-executions.md)

If you're a ServiceNow Process Automation administrator who wants to set up and customize Playbooks, check out the following resources:

-   [Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-automation-designer-triggers.md)
-   [Process definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-definitions.md)
-   [Activity definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/activity-definitions.md)

-   **[Playbooks User Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-automation-designer-architecture-overview.md)**  
Understand how Workflow Studio Playbooks work in the ServiceNow AI Platform® to automate cross-functional processes and consolidate them into task-oriented views for your end users.
-   **[Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-process-automation-designer.md)**  
Playbooks are a component in Workflow Studio. Workflow Studio gives you a streamlined way to author, configure, and monitor playbooks, flows, subflows, actions, and decision tables in one place.
-   **[Playbook generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/playbook-assist-landing.md)**  
Use Now Assist to generate playbooks from text directions or images. For example, you can enter directions to generate a playbook outline for managing customer support cases. Playbook Assist is part of the Now Assist for Creator application.
-   **[Getting started with Process Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/getting-started-process-automation.md)**  
Learn how Process Automation applications can help you use the ServiceNow AI Platform® to transform your manual business processes into digitized, automated workflows.
-   **[Domain separation and Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/process-automation-designer-domain-separation.md)**  
Data separation is supported for Playbooks. The domain value of the triggering input record determines the domain context. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[When to use flows and playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/when-to-use-flows-and-playbooks.md)**  
Use these general guidelines to determine when to create a flow or a playbook.
-   **[Playbooks across ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/integrating-with-process-automation-designer.md)**  
Playbooks capabilities are available in other ServiceNow® products and for specific industries.

**Parent Topic:**[Exploring Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-workflow-studio.md)


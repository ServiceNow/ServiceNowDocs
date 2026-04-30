---
title: Exploring Workflow Studio
description: Work with playbooks, flows, subflows, actions, data streams, and decision tables from a single consolidated interface. See operational details of your workflow applications and configure integration connections and credentials.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Workflow Studio, Build workflows]
---

# Exploring Workflow Studio

Work with playbooks, flows, subflows, actions, data streams, and decision tables from a single consolidated interface. See operational details of your workflow applications and configure integration connections and credentials.

## Homepage

The Workflow Studio homepage displays all the workflow applications available for authoring and editing.

![Parts of the Workflow Studio homepage.](../images/workflow-studio-homepage.png "Sample Workflow Studio homepage")

The Workflow Studio homepage consists of these elements.

-   **1. Homepage**

    Use the homepage to create and view workflows. You can see a list of workflows by type, a list of workflows you last worked on, a list of recent workflow updates, and a list of information resources.

-   **2. Workflow types**

    Select a workflow type to see a list of available items you can edit. Options include playbooks, flows, subflows, triggers, actions, data stream actions, and decision tables.

-   **3. Create a workflow**

    Select a workflow component to create. Options include playbooks, flows, subflows, actions, data stream actions, and decision tables.

-   **4. Current workflow list**

    See the list of workflow items available to edit. Each list shows the total number of workflow items available, a set of list controls, and a separate list row for each workflow item. List options include refresh list, list actions, copy URL, show filter panel, and delete.

-   **5. Pick up where you left off**

    See the list of workflow items that the current user last worked on. Quickly resume working on a workflow item.

-   **6. Latest updates**

    See the list of workflow items that have most recently been added or updated. See who worked on an item and when the updates were made.

-   **7. Resources**

    Learn more about Workflow Studio and its related workflow applications. Resources include links to the product documentation, ServiceNow videos, the ServiceNow Community site, the Centre of Excellence site, and the Developer Portal.


## Operations

The Workflow Studio operations page displays a usage dashboard and execution details for the workflow components that are currently running and have completed running.

![Parts of the Workflow Studio operations page.](../images/workflow-studio-operations.png "Sample Workflow Studio operations page")

The Workflow Studio operations page consists of these elements.

-   **8. Operations**

    Use the operations page to see dashboards and execution details by workflow type.

-   **9. Workflow types**

    Select a workflow type to see available dashboards and execution details. Options include playbooks and flows.

-   **10. Dashboards, Monitoring, and Setup**

    Select a dashboard to see operational charts such as most executed playbooks and playbook executions by state. Only users with the admin role can view an operations dashboard. Select a monitoring option to see execution details. Select a setup option to see settings and properties.


## Integrations

The Workflow Studio integrations page displays connection details for Integration Hub spokes. You can use this page to configure inbound and outbound spoke connections.

![Parts of the Workflow Studio integrations page.](../images/workflow-studio-integrations.png "Sample Workflow Studio integrations page")

The Workflow Studio integrations page consists of these elements.

-   **11. Integrations**

    Use the integrations page to add, configure, or view available connections.

-   **12. Integration types**

    See a list of available and configured spokes and connections. Configure or create a spoke to integrate data. Use the connection card to configure a connection or review its details.


## Create button

![Create button and its available options](../images/workflow-studio-create-button-and-menu-options.png "Create button and options menu")

You can create new workflow items from any Workflow Studio page rather than just the Homepage. Use the Create button on the tab header to display a list of available workflow components.

-   Playbook
-   Flow
-   Subflow
-   Trigger
-   Action
-   Data Stream
-   Decision table

## Choosing between playbooks and flows

Flows, subflows, and actions are the basic building blocks of a process automation. Playbooks are built on flows, subflows, and actions, and come with a set of out-of-the-box activities driven by subflows that are already built. If you're trying to decide whether your automation should be a playbook rather than just a flow, start by determining if your flow needs user interaction.

-   If your process automation requires user interaction, does it need manual user interaction? Examples of manual user interactions are a user reading a knowledge base article, going through a checklist, and gathering feedback.
    -   If yes, use a playbook.
    -   If no, does your process automation have several user interactions? Examples of user interaction are changing record field values such as changing the incident state or adding task work notes.
        -   If yes, consider using a playbook for a better user experience.
        -   If no, use a flow. Flows use less data storage in your instance.
-   If your process automation doesn't require user interaction, is it a sequence of subflow calls?
    -   If yes, is it hard to manage or difficult to view the flow?
        -   If yes, consider using a playbook for a better user experience. Stages in playbooks are easier to view and also have additional configuration options.
        -   If no, use a flow. Flows use less data storage in your instance.
    -   If your process automation does not require any user interaction, keep it as a flow. Flows use less data storage in your instance.

**Note:** You can also use flows that trigger a playbook just for interactive steps.

If you're trying to determine if a playbook should be a flow instead, start by determining whether your playbook is triggered 10s, 100s, or even 1000s of times per second.

-   If your playbook is triggered 10s, 100s, or 1000s of times per second, are there any user interactions?
    -   If yes, do the user interactions happen during every single run?
        -   If yes, use a playbook. Playbooks offer visibility into where you're at in a process, particularly business processes with manual user steps.
        -   If no, create a flow that triggers a playbook for the user interactions.
    -   If no, use a flow. Flows use less data storage in your instance.
-   If your playbook is not triggered very often, keep it as a playbook. Playbooks offer visibility into where you're at in a process, particularly business processes with manual user steps.

To learn more about the differences between flows and playbooks, see [When to use flows and playbooks](when-to-use-flows-and-playbooks.md). For general guidelines of using flows, subflows, and actions, see [General guidelines for Workflow Studio flows, subflows, and actions](../../flow-designer/reference/design-considerations-consolidated.md).

You can reference decision tables in flows, subflows, actions, and playbooks. Data streams are not used in flows, subflows, actions, playbooks, or decision tables. To learn more about data streams, see [Data Stream actions and pagination](https://www.servicenow.com/docs/access?context=data-stream-actions&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

## Differences from previous releases

Workflow Studio combines playbooks, flows, subflows, actions, decision tables, and Integration Hub integrations into a single builder application. Each of the prior workflow applications retain their functionality and their user interface to create and edit workflow objects. Workflow Studio introduces these changes.

-   **Access Workflow Studio from duplicate menu items**

    Workflow Studio uses the existing menu items for the separate workflow builder applications to open the corresponding workflow object type. For example, selecting the Process Automation Designer menu item opens the playbooks list from the Workflow Studio homepage.

-   **Configure integration connections**

    Workflow Studio enables you to configure integrations in the same user interface as you build integration components. For example, you can create a data stream action and also define its connection details.

-   **Create workflow components from any page**

    Beginning with the Xanadu release, Workflow Studio allows you to create a workflow component from any page rather than just the Homepage.

-   **Display each workflow type in a separate tab**

    Workflow Studio displays each workflow object type in its own tab. For example, playbooks open in a playbook tab and flows open in a flow tab.

-   **Edit different workflow types simultaneously**

    Workflow Studio combines all workflow object types into a single user interface. You can work on related workflow objects simultaneously rather than switch between separate workflow builder applications. For example you can create a flow that includes the Make a decision flow logic and also create the decision table used by that decision.

-   **Set application specific settings from the existing property pages**

    Workflow Studio relies on the existing system properties pages to add and configure setting for each workflow application. For example, open the flows properties page to configure the behavior of flows, subflows, and actions.

-   **View all available execution details**

    Workflow Studio contains execution details for all workflow object types. You no longer have to switch between applications to see execution details for a particular object type.


-   **[Exploring playbooks](../../process-automation-designer/concept/process-automation-designer.md)**  
Workflow Studio playbooks enable process owners to author cross-enterprise workflows and create a single, unified process. Build the underlying processes for playbooks that Playbook Experience agents and fulfillers use.
-   **[Exploring flows](exploring-flows.md)**  
Flows automate a repeatable multi-step process. When the flow trigger conditions are met, the flow runs a sequence of reusable actions and flow logic to complete the process.
-   **[Exploring subflows](../reference/exploring-subflows.md)**  
Subflows automate a repeatable multi-step process that also produces an output needed by another process. When a playbook, flow, or script calls a subflow, the subflow runs a sequence of reusable actions and flow logic to complete the process and produce output values.
-   **[Exploring actions](exploring-actions.md)**  
Actions automate a repeatable task or operation within a flow. Flows run actions by passing them data as inputs. Actions run a sequence of steps to complete the task, and pass data to the flow as outputs.
-   **[Exploring Decision Tables](../../decision-table/concept/decision-designer-overview.md)**  
Decision tables in Workflow Studio enable developers to decouple decision logic from their code by creating and maintaining decision rules.

**Parent Topic:**[Workflow Studio](../reference/workflow-studio.md)


---
title: Exploring flows
description: Flows automate a repeatable multi-step process. When the flow trigger conditions are met, the flow runs a sequence of reusable actions and flow logic to complete the process.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-04-21"
reading_time_minutes: 11
breadcrumb: [Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Exploring flows

Flows automate a repeatable multi-step process. When the flow trigger conditions are met, the flow runs a sequence of reusable actions and flow logic to complete the process.

Overview of flows in Workflow Studio 

## Flows overview

![Parts of a flow including a trigger, flow steps, and a result](../../flow-designer/images/MMASSET0020954-flows-infographic.svg)

A flow is an automated process consisting of a trigger, a sequence of reusable actions, and flow logic. The trigger specifies when to run the flow. The actions perform a sequence of operations on your data. For example, the **VTB Sample Flow** creates and assigns a VTB card whenever a priority 1 incident is created.

Flows consist of the following components.

-   **Trigger**

    A trigger specifies when to run the flow. When the trigger conditions are met, the system runs the flow using the data provided by the trigger. Workflow Studio supports a variety of trigger types such as record, Service Catalog requests, and scheduled triggers. For a description of available trigger types, see

    -   [Workflow Studio flow trigger types](../../flow-designer/reference/flow-triggers.md)
    -   [Saved flow triggers](../../flow-designer/concept/saved-flow-triggers.md)
-   **Flow execution details**

    A flow execution details page allows a flow author to view run-time information about an action or flow directly from the design environment. You can view details such as the current state, actions or steps run, output values generated, and errors produced. See [Flow execution details](../../flow-designer/concept/flow-execution-details.md).

-   **Flow error handler**

    A flow error handler enables a flow to catch and report errors from the flow execution details. Run a sequence of actions and subflows to identify and correct issues. For example, have flows log output values, send notifications, and run corrective subflows when they produce an error. See [Flow error handler](../../flow-designer/concept/flow-error-handler.md).

-   **Subflows**

    A subflow is an automated process consisting of a sequence of reusable actions, data inputs, and outputs. In contrast to flows, subflows do not have a trigger but instead run when called from a flow, from another subflow, or from a script. Building and managing subflows requires that you have some familiarity with the ServiceNow AI Platform tables and fields that the application or process uses. Process analysts can create subflows using available actions or use an existing subflow as a template. See [Building subflows](../../flow-designer/concept/subflows.md).

-   **Actions**

    An action is a reusable operation that enables process analysts to automate ServiceNow AI Platform features without having to write code. For example, the **Create Record** action allows process analysts to generate records in a particular table with particular values when certain conditions occur. ServiceNow core actions like Create Record require some familiarity with ServiceNow AI Platform tables and fields. Action designers can create application-specific actions to pre-set configuration details. For example, creating a Create Incident Task action ensures that the process analyst uses the correct table and field configuration each time the action is used. You can add application-specific actions by activating the associated spoke. See [Workflow Studio actions](../../flow-designer/concept/flow-actions.md).

-   **Spokes**

    A spoke is a scoped application containing Workflow Studio actions and subflows for managing specific tables. For example, the **ITSM Spoke** contains actions for managing Incident and Problem records. You can activate additional spokes from the ServiceNow Store or activating the appropriate plugin. Building your own spoke requires familiarity with application development on the ServiceNow AI Platform. For a list of available spokes, see [Spokes](../../flow-designer/concept/spokes.md).


This topic describes the basic tasks involved in creating a flow using Workflow Studio. For detailed instructions for creating a flow, see [Create a flow in Workflow Studio](../../flow-designer/task/create-flow.md).

## Sections of a flow

![Four sections of a flow: trigger, actions, error handler, and data panel.](../../flow-designer/images/flow-sections.png)

A flow consists of four sections.

-   **1. Trigger section**

    The Trigger section is where you select and define when the flow runs. Each trigger type defines when a flow starts and the starting data available to it. There are triggers for record operations, dates, and application operations.​

    Flows support record-based, schedule-based, and application-based trigger types. For more information about available trigger types, see [Workflow Studio flow trigger types](../../flow-designer/reference/flow-triggers.md).

-   **2. Action section**

    The Actions section is where you select and configure the steps that make up your flow. You can add [actions](../../flow-designer/concept/actions.md), [flow logic](../../flow-designer/concept/flow-logic.md), and [subflows](../../flow-designer/concept/subflows.md) to a flow by opening the associated picker.

    Sequential numbers appear next to each item in the design canvas. Action numbers start with 1 and then increment by 1 as you add more items to the flow.

-   **3. Error handler section**

    The Error handler section of the flows is where you can enable the flow to catch and correct errors. For more information about using the error handler section, see [Flow error handler](../../flow-designer/concept/flow-error-handler.md).

-   **4. Data panel**

    The Data panel stores any data gathered or generated by the flow as variables. Each data variable has its own pill that Flow designers can use to drag the variable value to an action input or output. Flows generate the pill name based on the contents and its data type. The system specifies the variable data type next to the pill.

    ![Example flow data in the data panel.](../../flow-designer/images/data-pane-example.png "Example flow data in the data panel")


## Action configuration

Add an action to a flow by opening the action picker. Configure an action by specifying its input values, which may be data from the flow trigger or the output of other actions. Enter values for inputs directly, or use data from the Data panel to configure an action's inputs. At the start of a flow, the data may be limited to the flow trigger or subflow inputs. As you add actions to a flow, the output values of each action appear as data pills in the Data panel.

## Component pickers

In the Actions section of a flow, you can select the **Action**, **Flow logic**, or **Subflow** options to open a picker for that component type. You can either enter text in the search window to search for a component, or browse the categories to find a component that you want to add to your flow.

![Use the action picker to find actions that you can add to your flow.](../../flow-designer/images/action-picker.png "Action picker menu")

The Action picker consists of several features to make finding actions easier.

-   **Search actions**

    The Action picker filters the list of actions it displays as you type. The picker only displays actions that match your search query.

-   **Most recent**

    The Action picker displays a list of the most recent actions that you have selected during this session.

-   **Popular**

    The Action picker displays a list of actions that other users have frequently used.

-   **Installed Spokes**

    Some applications include spokes which add application-specific actions. Spoke actions are typically read-only but can be copied and customized. The Action picker groups actions by the application scope that they belong to. Select a spoke to see its list of actions.

    -   **ServiceNow Core actions**

        Your instance comes with a collection of core actions, or frequently used ServiceNow AI Platform operations, that can be added to any flow.

    -   **Global spoke actions**

        Developers may create custom actions in the Global application scope to make them available to all applications. ServiceNow provides some actions in the Global scope for use in any flow.

    -   **Custom actions**

        Developers may also create custom actions in an application scope that they own. Custom actions appear in the action picker under the application scope of the spoke.


## Descriptions of flow data

See a natural language description of the data each component of a flow uses. Understand what data flow triggers, actions, and flow logic blocks use without having to open their configuration details.

![Example flow with detailed descriptions of data](../../flow-designer/images/example-flow-data-descriptions.png "Example flow with descriptions of data")

For example, this flow uses these descriptions.

-   **Trigger description**

    The create record trigger describes the conditions that must be met to start the flow.

    `Incident Created where (Short description starts with [demo], and Assigned to is not empty )`

-   **Action description**

    The Look Up Records action describes the filter conditions it uses to find records.

    `Look Up Incident Records where (Caller is [Trigger - Record Created > ... > Caller], and Active is true)`

-   **Flow logic description**

    The If flow logic describes the conditions which must be met to run the actions it contains.

    `If [1 - Look Up Records > Count] is greater than 1`


## Flows benefits

Flows provide process owners and developers these benefits:

-   Automates repetitive work to improve efficiency and experience.
-   Describes a workflow in natural language to help non-technical users understand what it does.
-   Displays a workflow as a diagram to help builders see available paths and connections.
-   Enables creating and testing a workflow from a single interface to ensure it works as expected.
-   Promotes process automation by enabling subject matter experts to develop and share reusable actions with flow authors.
-   Reduces upgrade costs, with upgrade-safe ServiceNow AI Platform logic replacing complex custom script.
-   Reduces development costs by providing a library of reusable actions.
-   Scales with separate subscriptions for integration and Robotic Process Automation \(RPA\) functionality.

|Benefit|Feature|Users|
|-------|-------|-----|
|Build an automated workflow from an existing library of automated operations.|Flow|Application developer, process owner, or administrator|
|Run an automated workflow when a set of trigger conditions are met.|Flow|Application developer, process owner, or administrator|
|Use a set of trigger conditions as input data to run an automated workflow.|Flow|Application developer, process owner, or administrator|

-   **[Getting started with flows](../../flow-designer/task/getting-started-flow.md)**  
Create a sample flow with a trigger and base system actions that requires an approval.
-   **[Flow action numbering](../../flow-designer/concept/flow-action-numbering.md)**  
The action outline displays a whole number besides each action and flow logic block in a flow. You can update flows containing legacy action numbering from within Workflow Studio.
-   **[Workflow Studio Landing page](../../flow-designer/concept/flow-designer-home-landing-page.md)**  
Access or create actions, flows, subflows, or their execution details.
-   **[Workflow Studio data](../../flow-designer/concept/data-population.md)**  
Each time you add an action to a flow, Workflow Studio adds a data pill to store its results. The data pill name indicates its sequence in the flow and its data type.
-   **[Flow diagramming view](../../flow-designer/concept/flow-diagramming-view.md)**  
Create and view flows as diagrams. See the paths a flow can follow and the connections between elements.
-   **[Flow execution details](../../flow-designer/concept/flow-execution-details.md)**  
View run-time information about an action or flow directly from the design environment, such as the current state, items run, and values produced. Open related records from embedded ServiceNow AI Platform editors or in a new tab.
-   **[Flow roles](../../flow-designer/concept/flow-roles.md)**  
Create flows and subflows that run with specific roles. Assigning roles enables you to create user-initiated flows that run with their own roles rather than the user's roles.
-   **[Domain separation and Workflow Studio](../../flow-designer/concept/flow-designer-domain-separation.md)**  
Domain separation is supported in Workflow Studio. Workflow Studio supports domain separation of business logic, which lets each tenant domain have its own flows, actions, and subflows. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Architecture Overview](../../flow-designer/concept/flow-designer-arch-overview.md)**  
Understand how Workflow Studio works within the ServiceNow AI Platform to activate, trigger, and process flows and actions.
-   **[Default read-only flows](../../flow-designer/concept/default-read-only-flows.md)**  
Open existing flows in a read-only state to protect them from accidental changes. While a flow is in a read-only state, you can only review, test, deactivate, or request to edit it.
-   **[Flow debugger](../../flow-designer/concept/flow-debugger.md)**  
Debug flows and subflows from a dedicated Workflow Studio tab. Set breakpoints and step through a paused flow to review configuration and runtime values.
-   **[Saved flow triggers](../../flow-designer/concept/saved-flow-triggers.md)**  
Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.

**Parent Topic:**[Exploring Workflow Studio](exploring-workflow-studio.md)


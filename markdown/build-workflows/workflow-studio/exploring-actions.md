---
title: Exploring actions
description: Actions automate a repeatable task or operation within a flow. Flows run actions by passing them data as inputs. Actions run a sequence of steps to complete the task, and pass data to the flow as outputs.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Exploring actions

Actions automate a repeatable task or operation within a flow. Flows run actions by passing them data as inputs. Actions run a sequence of steps to complete the task, and pass data to the flow as outputs.

## Actions overview

Automate a repeatable task within a flow as a sequence of related steps. Enable flow authors to add actions to multiple flows with minimal configuration.

A reusable action includes these components.

-   **Inputs**

    Inputs are data variables used in your action. For example, if an action step creates a record in the incident table, your input might be a reference to the incident table. Once added as an input, the table and its fields are available to steps and outputs in the flow.

    Each input you define for an action becomes a configuration option in the Workflow Studio interface. To use the action in a flow, flow designers must define a value for each mandatory input. The more inputs an action has, the more data flow designers must define and the more familiar they must be with the underlying data model to use the action effectively.

    Inputs provide advanced options based on their data type. All inputs have advanced options to add a hint or provide a default value. Use advanced options to guide flow designers through adding and configuring an action to a flow. For example, create a choice input to provide flow designers with a pre-defined list of configuration options to choose from. For more information about the configuration options available to particular data types, see [field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **Outputs**

    Outputs are data variables that represent the results of the action. These results are available to other actions in a flow.

-   **Steps**

    A step is a single reusable operation within an action. For example, the **Create Record** step allows action designers to specify the table and field values to use during record creation. Step configuration requires subject matter expertise with application tables, fields, and business logic. Application developers or IT generalists add steps to actions from the Workflow Studio action design environment. Workflow Studio provides a set of ServiceNow core steps to automate ServiceNow AI Platform processes. You can add application-specific steps by activating the associated spoke.


## Workflow to create actions using Workflow Studio

The following illustration describes the basic tasks involved in creating a subflow using Workflow Studio. For detailed instructions for creating a subflow, see [Create an action in Workflow Studio](../../flow-designer/task/create-action.md).

## Actions benefits

Using Workflow Studio, you can:

-   Create application-specific actions with pre-set configuration details, enabling process analysts to easily add actions to a flow with little configuration.
-   Create scripted actions that appear code-less when added to a flow.
-   Build integrations using Integration Hub.

|Benefit|Feature|Users|
|-------|-------|-----|
|Build an automated operation from an existing library of automated steps.|Action|Application developer, integration owner, or process owner|
|Run an automated operation on demand.|Action|Application developer, integration owner, or process owner|
|Use data from other automated operations as inputs.|Action|Application developer, integration owner, or process owner|
|Pass data to other automated operations as outputs.|Action|Application developer, integration owner, or process owner|
|Stream data in a sequence of pages.|Data Stream Action|Integration owner|

-   **[Conversational actions](../../flow-designer/concept/conversational-actions.md)**  
Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio.

**Parent Topic:**[Exploring Workflow Studio](exploring-workflow-studio.md)


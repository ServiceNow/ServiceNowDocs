---
title: Stages and activities
description: In Playbooks, an activity represents one step in your overall business process. You can sequence many activities together in the stages of your process.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Building playbooks, Use, Workflow Studio, Build workflows]
---

# Stages and activities

In Playbooks, an activity represents one step in your overall business process. You can sequence many activities together in the stages of your process.

## Stages

Group activities by the stages of your business process, and sequence activities in an order that makes sense for your cross-enterprise workflow. A stage is made up of many sequenced activities that are grouped in a logical way. In the Playbooks Board view of the design environment, you can add a stage to your playbook by clicking **+ Add stage**. In the Diagram view, select the **+** icon on connectors \(lines\) to add a stage.

## Activities

In Playbooks, an activity represents one step in your overall business process. In the system, an activity is one instance of an activity definition. For more information on activity instances and activity definitions, see the [Playbook Experience](process-automation-designer-architecture-overview.md) and [activity definitions](activity-definitions.md).

## Adding an activity to your playbook

In the Playbooks Board view of the design environment, select **+ Add activity** to open the activity picker. In the Diagram view, select the **+** icon on connectors \(lines\) to open the activity picker. In the activity picker, you can search for an activity to add or select one from the list of Common Activities. To choose an activity for a custom application, first select the application and then select the activity from the resulting list within the picker.

Additionally, you can add an activity just using an [automation asset](automation-assets.md).

If there isn't an activity that fits your use case, you can create your own activity definition to add to the activity picker. For more information, see [create an activity definition](../task/create-activity-definition.md).

## Interactive and Non-Interactive activities

Activity categories include:

-   **Interactive Activities**

    When an interactive activity runs, it prompts a user for input in your playbook as it runs. For more information, see [Interactive activities](interactive-activities.md).

-   **Non-Interactive Activities**

    When a non-interactive activity runs, it runs entirely behind-the-scenes and requires no user input. For more information, see [Non-Interactive activities](non-interactive-activities.md).

-   **Optional Activities**

    An optional activity can be inserted by agents and fulfillers during a playbook run. For more information, see [Optional activities](optional-activities.md#).


## Stage and activity details

When you select an activity, the side panel should open. Under the **Details** tab of the side panel, you can add names, descriptions, and start rules to the stages and activities in your playbook. Click the show or hide additional options button to show or hide additional properties for your currently selected stage or activity. The basic details for each stage and activity include:

-   **Label**

    You can enter a display name for your stage or activity. This name appears during playbook runtime.

    **Note:** Keep your stage and activity names brief, as the system truncates long names.

-   **Description**

    Optionally, enter a description for your activity or stage. This description only appears within Playbooks and isn't visible during playbook runtime.

-   **Start Rule**

    Under **Schedule** &gt; **Start Rule**, select a start rule for when your stage should start running:

    -   **When process starts**: Your stage starts running as soon as the playbook starts.
    -   **After specific stages**: Your stage starts running after specified stage\(s\) have finished running.
    Under **Schedule** &gt; **Start Rule**, select a start rule for when your activity should start running:

    -   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
    -   **After specific activities**: Your activity starts running after specified activities have finished running.
-   **Run condition**

    Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.


## Activity inputs

Under the **Automation** tab of the side panel, each activity has inputs you can configure:

-   To change default inputs and outputs for the activity, open and edit the source flow in Workflow Studio by selecting the **Open link** icon \(![Open link icon](../images/external-link-icon.png)\) next to the **Automation** field.

    For more information on how to work with the default inputs and outputs for activities in Playbooks, see [Create an action as an activity automation plan](../task/create-automation-plan.md).

    **Note:** You must have the appropriate user roles to access Workflow Studio and Workflow Studio. For more information, see [User access to Workflow Studio flows](../../flow-designer/concept/user-access-flow-designer.md).

-   **Inputs** are data that you provide so that the activity runs and performs its function appropriately. For example, a Record activity that notifies a customer of an application rejection will have message inputs for the email address, subject, body, and more.
-   Expected **Outputs** are displayed at the bottom of the Automation tab.

## Creating static and dynamic values for activity inputs

You can add dynamic data to an activity input. Click the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\) and navigate, or dot-walk, to the data pill whose dynamic value you want to use when your activity runs. You can select dynamic data from fields in the input record. If your activity has a start rule of **After specific activities**, you can also select dynamic data from the outputs of other activities in your playbook. For more information on dot-walking to related fields and records on the ServiceNow AI Platform, see [selecting fields on related tables using dot-walking](https://www.servicenow.com/docs/access?context=c_DotWalking&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

**Note:** You can dot-walk to fields in a Reference but not in a Document ID or Sys ID.

The inputs for interactive activities typically provide data that renders in a playbook for an agent to interact with. The inputs for non-interactive activities can render in a playbook but don't require any user input in order to run. For more information, see [Interactive activities](interactive-activities.md) and [Non-Interactive activities](non-interactive-activities.md).

## Design considerations

Refer to these design considerations when working with stages and activities:

-   **Keep ServiceNow AI Platform state models in mind when designing your playbook**

    Some record types already have state models that describe their life cycle. Use any existing state model as a template for the design of your playbook. For more information, see [State Management](https://www.servicenow.com/docs/access?context=state-model&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


-   **[Add and configure a stage in a playbook](../task/add-configure-stage.md)**  
Add and configure a stage in your playbook.
-   **[Activity definitions](activity-definitions.md)**  
Activity definitions describe how the activities in your playbook get the data that they need when your playbook runs.
-   **[Add and configure an activity in a playbook](../task/add-configure-activity.md)**  
Add and configure an activity in your playbook.
-   **[Use AI agent as an activity](../task/ai-agent-as-activity.md)**  
Use an existing AI agent as an activity in your playbook to automate tasks. The AI agent gathers the required context, performs the work, and produces outputs that subsequent activities can consume.
-   **[Automation Assets](automation-assets.md)**  
Include all automation assets in the activity picker to add a subflow, flow, or action directly to your playbook without having to create an activity definition.
-   **[Start with delay input properties](../reference/start-with-delay-properties.md)**  
Specify a duration of time to wait before running an activity or a stage whose start rule and conditions have been met. Give users time to act during automated playbooks. Give users time to wait for a specific date and time to complete actions.
-   **[Optional activities](optional-activities.md#)**  
Enable your agents and fulfillers to add additional activities as they go through a playbook.
-   **[Decision activities](../task/create-a-decision-activity.md)**  
Create and define branches with different conditions for different paths between activities.
-   **[Decision stages](../task/create-decision-stage.md)**  
Create and define branches with different conditions for different paths between stages.
-   **[Questionnaire activity](../reference/questionnaire-activity.md)**  
Collects inputs from a user during a playbook run to use later in the playbook.
-   **[Parallel branches](../task/create-parallel-activity.md)**  
Add branches for activities and stages that run in parallel to another branch of activities and stages.
-   **[Add dynamic inputs to an activity](../task/add-dynamic-inputs-to-activity.md)**  
Configure your activity to show a certain set of fields based on the value of another input, such as a selected catalog item, selected decision table, or even a REST API response.
-   **[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)**  
Use playbook activity state mapping to override the status of a playbook card.

**Parent Topic:**[Building playbooks](building-a-process.md)


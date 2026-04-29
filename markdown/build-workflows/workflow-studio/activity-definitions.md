---
title: Activity definitions
description: Activity definitions describe how the activities in your playbook get the data that they need when your playbook runs.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Activity definitions

Activity definitions describe how the activities in your playbook get the data that they need when your playbook runs.

Activity definitions provide default configurations and values for your activities so that they can run properly when your playbook is triggered. Each activity definition contains some basic configuration details, as well as an automation plan and activity experience.

The Activity Definition \[sys\_pd\_activity\_definition\] table lists the definitions for the activities that you can add to a playbook in Workflow Studio. To access these activity definitions, navigate to **Process Automation** &gt; **Process Automation Administration** &gt; **Activity Definitions**.

## Fields

Each activity definition record has these basic fields:

<table id="table_ezy_jn4_rlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name of the activity to display to users in Workflow Studio.

</td></tr><tr><td>

Table

</td><td>

Name of the table whose records the activity can access as inputs. Typically, this table is either the Task \[task\] or Global \[global\] table.

</td></tr><tr><td>

Application

</td><td>

Application scope that the activity can run in.

</td></tr><tr><td>

Accessible From

</td><td>

Options include:-   **All application scopes** - Users can access this activity from any application scope.
-   **This application scope only** - Users can access this activity from the application scope that you specify in the **Application** field only.

</td></tr><tr><td>

Description

</td><td>

Optional description for the activity.

</td></tr><tr><td>

Required Roles

</td><td>

A list of user roles that are allowed to access activities that use this activity definition.

</td></tr></tbody>
</table>## Automation plan

Each activity definition has an automation plan. The automation plan for an activity definition specifies:

-   The Workflow Studio flow or action, which drives the activity's automation
-   The activity's inputs, which are the data that the activity needs to run your playbook

Activity designers can configure the visibility of each activity input.

-   **Include in standard modal**

    Hides the input from the properties panel. Playbook designers can only see the input from the standard modal when they select the **Show advanced properties** option.

-   **Include in standard modal and configuration panel**

    Displays the input in the properties panel. Playbook designers can also see the input from the standard modal when they select the **Show advanced properties** option.

-   **Admin visibility only**

    Hides the input from users who do not have the admin or playbook.admin roles.


## Activity experience

Each activity also has an optional activity experience. The activity experience specifies an experience type, associated record, and details for what data to render in the activity's associated playbook card. Activity experience configurations only apply to activities that you add to a playbook which has an associated Playbook user experience.

-   **Experience type**

    An experience type defines the data, or properties, that describe how the activity renders as a playbook card at runtime. For example, a Record experience type tells the system that the activity can display a title, tagline, description, footer, and service level agreement \(SLA\) information in the Playbook card when your activated playbook runs. For more information, see [UI Layouts](experience-types.md).

-   **Associated record**

    The associated record defines the record whose data can render within a Playbook card at runtime. The associated record is dynamic, which means that it changes frequently as the playbook progresses. Because of this dynamic nature, you may want to use the data pill picker \(![Data pill picker](../images/data-pill-picker-icon.png)\) to map the associated record to output record data within the underlying subflow or action specified in the automation plan.

-   **Data to render in the Playbook card**

    You can specify the data to render in the Playbook card in the sections under the Associated Record section. To add dynamic data to fields that render in this user-facing view, use the data pill picker ![Data pill picker](../images/data-pill-picker-icon.png) next to a data field and navigate, or dot-walk, to the appropriate data pill. The data pill should point to data within the subflow or action specified in the activity definition's automation plan.

    **Note:** An activity experience contains many sections where you can specify the data to appear within the Playbook card. These sections vary depending on the experience type that you select. For example, a Record experience type has Details, Form, Attachments, and Features sections, while a Knowledge experience type has Knowledge, Details, and Features sections. For more information, see [UI Layouts](experience-types.md).

-   **Actions to render in the Playbook card**

    You can specify the Playbook actions that you want to render in an activity's Playbook card using the Playbook Experience Action Assignment Map related list. A Playbook action displays as a button in the Playbook card's footer. Playbook actions can run server scripts, dispatch client actions, or render UI components. For more information.

    To add a Playbook action to your activity definition, select **New** in the Playbook Experience Action Assignment Map related list. Then, choose a Playbook action from the **Action Assignment** list. Next, choose a Playbook user experience that you want the Playbook action to appear in from the **Playbook Experience** list, and then click **Submit**.


## Design considerations

Refer to these design considerations when working with activity definitions:

-   **Avoid calling triggered Workflow Studio flows in an activity's automation plan**

    To prevent unintentionally running a flow outside of Playbooks, you can use only subflows or actions in activity automation plans. Alternatively, you can set the flow's trigger to only run if not already running. For more information, see [Workflow Studio flow trigger types](../../flow-designer/reference/flow-triggers.md).

-   **Specify default input values in your activity definitions**

    Preconfiguring default input values for your activity definitions reduces the time and complexity needed for a playbook owner to create a playbook.


-   **[Create an activity definition](../task/create-activity-definition.md)**  
Specify the action or subflow you want an activity to run. Configure the inputs you want playbook designers to set when adding the activity to a playbook. Select the experience you want end users to have when the activity runs.
-   **[Create an action as an activity automation plan](../task/create-automation-plan.md)**  
Create an example action to configure and run as an activity from Playbooks.
-   **[UI Layouts](experience-types.md)**  
A UI Layout describes what properties and components to use when an activity renders as a card in a Playbook Experience.

**Parent Topic:**[Stages and activities](process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](../task/add-configure-stage.md)

[Add and configure an activity in a playbook](../task/add-configure-activity.md)

[Automation Assets](automation-assets.md)

[Start with delay input properties](../reference/start-with-delay-properties.md)

[Optional activities](optional-activities.md#)

[Decision activities](../task/create-a-decision-activity.md)

[Decision stages](../task/create-decision-stage.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Parallel branches](../task/create-parallel-activity.md)

[Add dynamic inputs to an activity](../task/add-dynamic-inputs-to-activity.md)

[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)


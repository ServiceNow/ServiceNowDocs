---
title: Manage access to Workflow Studio flow features
description: Restrict access to individual Workflow Studio flow features by user role. Specify what additional roles a user must have to access an individual feature such as copy a flow.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 11
breadcrumb: [User access to flows, Configure flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Manage access to Workflow Studio flow features

Restrict access to individual Workflow Studio flow features by user role. Specify what additional roles a user must have to access an individual feature such as copy a flow.

## Before you begin

Create any custom roles that you want to use for feature access. When you specify which roles are required to access a feature, you can select the roles from a list of existing roles.

Role required: admin

## About this task

Features are elements of the Workflow Studio UI. When feature filtering is turned off, users with the flow\_designer role have access to all of the Workflow Studio features. When feature filtering is turned on, you can specify which roles a user must have to access individual features.

**Note:** Your users must have the flow\_designer role to create and edit flows. You can specify the additional roles that a user must have to access particular features or content.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Administration** &gt; **Feature Access List**.

2.  For each feature on the list, select the edit icon \(![Edit icon.](../images/view-edit-icon.png)\) next to the feature.

3.  Enter the role or roles that are required to access the feature.

    **Note:** Add the flow\_designer role to each feature on the Feature Access List. Your users must have the flow\_designer role to access the Workflow Studio features.

    You can use these options to restrict access to Workflow Studio action authoring features.

    |Feature|Description|
    |-------|-----------|
    |"If step fails..." Step Option|Continue running the next step or go to an error evaluation. For more information, see ["If step fails..." Step Option](../concept/action-error-evaluation.md).|
    |Action preferences|Configure action preferences.|
    |Action Reporting Settings|Configure action execution detail settings.|
    |Code snippet|Generate a code snippet to call an action. For more information, see [Code snippet](flow-design-code-snippet.md).|
    |Configure connections|Configure a connection through the Connections dashboard. For more information, see [Configure a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/dashboard-configure-connection.md).|
    |Copy action|Copy an action to give it a new name and move it to another application scope. For more information, see [Copy an action](copy-action.md).|
    |Error Evaluation|Enable actions to catch step failures and continue running. Identify when specific error conditions occur and return your own action status code, status message, and error state. For more information, see [Error Evaluation](../concept/action-error-evaluation.md).|
    |Executions|View the runtime information about an action from the design environment such as the current state, actions, or steps run, and values produced. For more information, see [Executions](../concept/flow-execution-details.md).|
    |Manage natural language title|Change the default title for an action by adding styled and dynamic text. For more information, see [Manage natural language title](manage-natural-language-title.md).|
    |Manage security|Manage access to Workflow Studio actions.|
    |Properties|Configure how the system processes flows. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Publish|Publish an action so that other users can use the action.|
    |Save|Save an action.|
    |See related flows|See a list of flows that contain a custom action. For more information, see [See related flows for action](see-related-flows-for-action.md).|
    |Test|Test an action before publishing it for other users. For more information, see [Test an action](test-action.md).|

    You can use these options to restrict access to Workflow Studio flow authoring features.

    |Feature|Description|
    |-------|-----------|
    |Activate|Activate a flow to make it available to other users. For more information, see [Activate](flow-activate.md).|
    |Code snippet|Generate a code snippet to call a flow. For more information, see [Code snippet](flow-design-code-snippet.md).|
    |Configure connections|Configure a connection through the Connections dashboard. For more information, see [Configure a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/dashboard-configure-connection.md).|
    |Copy flow|Copy a flow to give it a new name and move it to another application scope. For more information, see [Copy a flow](copy-flow.md).|
    |Deactivate|Deactivate a flow to make it unavailable to other users.|
    |Diagramming View|Create and view flows as diagrams. You can see the paths a flow can follow and the connections between elements. For more information, see [Diagramming View](../concept/flow-diagramming-view.md).|
    |Edit Flow|Make a flow editable. For more information, see [Edit a flow](flow-edit.md).|
    |Executions|View runtime information about a flow from the design environment such as the current state, actions, or steps run, and data pill values produced. For more information, see [Executions](../concept/flow-execution-details.md).|
    |Flow Error Handler|Enable flows to catch errors. Run a sequence of actions and subflows to identify and correct issues. For more information, see [Flow Error Handler](../concept/flow-error-handler.md).|
    |Flow Preferences|Enable or disable user preferences for flows. For more information, see [User preferences for flows](../reference/flow-preferences.md).|
    |Flow Reporting Settings|Choose whether to generate execution details for all flows and actions run, just for individual flows and actions, or just when you test a flow or action. For more information, see [Activate flow reporting](enable-flow-reporting.md#).|
    |Manage flow catalog variables|Create Service Catalog variables that are only available to a specific Service Catalog triggered-flow. Flow-specific variables are available to the catalog tasks and actions in the flow. For more information, see [Manage flow catalog variables](create-flow-catalog-variables.md).|
    |Manage natural language title|Change the default title for a flow by adding styled and dynamic text. For more information, see [Manage natural language title](manage-natural-language-title.md).|
    |Manage security|Manage access to Workflow Studio actions.|
    |Properties|Configure how the system processes flows. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Save|Save a flow.|
    |Stages|Configure when stages display to a user, define stage state labels, and add stages to a flow within Workflow Studio. For more information, see [Stages](add-stages.md).|
    |Test|Test a flow before publishing it for other users. For more information, see [Test a flow](flow-test.md).|

    You can use these options to restrict access to Workflow Studio subflow authoring features.

    |Feature|Description|
    |-------|-----------|
    |Code snippet|Generate a code snippet to call a subflow. For more information, see [Code snippet](flow-design-code-snippet.md).|
    |Configure connections|Configure a connection through the Connections dashboard. For more information, see [Configure a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/dashboard-configure-connection.md).|
    |Copy subflow|Copy a subflow to give it a new name and move it to another application scope. For more information, see [Copy a subflow](copy-subflow.md).|
    |Diagramming View|Create and view subflows as diagrams. You can see the paths a flow can follow and the connections between elements. For more information, see [Diagramming View](../concept/flow-diagramming-view.md).|
    |Edit Subflow|Make a subflow editable. For more information, see [Edit a flow](flow-edit.md).|
    |Executions|View runtime information about a subflow from the design environment such as the current state, actions, or steps run, and data pill values produced. For more information, see [Executions](../concept/flow-execution-details.md).|
    |Flow Reporting Settings|Choose whether to generate execution details for all subflows and actions run, just for individual subflows and actions, or just when you test a subflow or action. For more information, see [Activate flow reporting](enable-flow-reporting.md#).|
    |Manage natural language title|Change the default title for a subflow by adding styled and dynamic text. For more information, see [Manage natural language title](manage-natural-language-title.md).|
    |Manage security|Manage the access to subflows.|
    |Properties|Configure how the system processes subflows. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Publish|Publish a subflow so that other users can use the subflow. For more information, see [Test](test-subflow.md).|
    |Save|Save a subflow.|
    |See related flows|See a list of flows that call a specific subflow. For more information, see .|
    |Stages|Configure when stages display to a user, define stage state labels, and add stages to a subflow within Workflow Studio. For more information, see [Stages](add-stages.md).|
    |Subflow Preferences|Enable or disable user preferences for subflows. For more information, see [User preferences for flows](../reference/flow-preferences.md).|
    |Test|Test a subflow before publishing it for other users. For more information, see [Test a subflow](test-subflow.md).|

    You can use these options to restrict access to Workflow Studio flow template authoring features.

    |Feature|Description|
    |-------|-----------|
    |Activate|Activate a flow template.|
    |Deactivate|Deactivate a flow template to make it unavailable to other users.|
    |Edit template|Make a flow template editable.|
    |Manage flow catalog variables|Create Service Catalog variables that are only available to a specific Service Catalog triggered-flow. For more information, see [Manage flow catalog variables](create-flow-catalog-variables.md).|
    |Properties|Configure how the system processes flow templates. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Save|Save a flow template.|

4.  Continue adding roles to each feature on the list.

5.  Select **OK**.

6.  To turn on the feature access for your users, select the **Enable feature access filtering?** option.

    After the feature access is enabled, your users must have the required roles before they can access the features. If a user doesn't have the required roles for a feature, the feature does not work for that user.


## What to do next

Assign your users with the roles to access features.


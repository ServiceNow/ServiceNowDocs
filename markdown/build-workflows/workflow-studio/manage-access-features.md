---
title: Manage access to Workflow Studio flow features
description: Restrict access to individual Workflow Studio flow features by user role. Specify what additional roles a user must have to access an individual feature such as copy a flow.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [User access to flows, Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
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

2.  For each feature on the list, click the edit icon \(![Edit icon.](../images/view-edit-icon.png)\) next to the feature.

3.  Enter the role or roles that are required to access the feature.

    **Note:** Add the flow\_designer role to each feature on the Feature Access List. Your users must have the flow\_designer role to access the Workflow Studio features.

    You can use these options to restrict access to Workflow Studio action authoring features.

    |Feature|Description|
    |-------|-----------|
    |Copy action|Copy an action to give it a new name and move it to another application scope. For more information, see [Copy an action](copy-action.md).|
    |Error Evaluation|Enable actions to catch step failures and continue running. Identify when specific error conditions occur and return your own action status code, status message, and error state. For more information, see [Error Evaluation](../concept/action-error-evaluation.md).|
    |Manage natural language title|Change the default title for an action by adding styled and dynamic text. For more information, see [Manage natural language title](manage-natural-language-title.md).|
    |Manage security|Manage access to Workflow Studio actions.|
    |Executions|View the runtime information about an action from the design environment such as the current state, actions, or steps run, and values produced. For more information, see [Executions](../concept/flow-execution-details.md).|
    |Save|Save an action.|
    |Publish|Publish an action to allow other users to use the action.|
    |Configurations|Manage Workflow Studio configurations.|
    |"If step fails..." Step Option|Continue running the next step or go to an error evaluation. For more information, see ["If step fails..." Step Option](../concept/action-error-evaluation.md).|
    |Code snippet|Generate a code snippet to call an action. For more information, see [Code snippet](flow-design-code-snippet.md).|
    |Test|Test an action before publishing it for other users. For more information, see [Test an action](test-action.md).|
    |Properties|Configure how the system processes flows. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Configure connections|Configure a connection through the Connections dashboard. For more information, see [Configure a connection](https://www.servicenow.com/docs/access?context=dashboard-configure-connection&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).|

    You can use these options to restrict access to Workflow Studio flow authoring features.

    |Feature|Description|
    |-------|-----------|
    |Manage natural language title|Change the default title for a flow by adding styled and dynamic text. For more information, see [Manage natural language title](manage-natural-language-title.md).|
    |Manage flow catalog variables|Create Service Catalog variables that are only available to a specific Service Catalog-triggered-flow. Flow-specific variables are available to the catalog tasks and actions in the flow. For more information, see [Manage flow catalog variables](create-flow-catalog-variables.md).|
    |Properties|Configure how the system processes flows. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Copy flow|Copy a flow to give it a new name and move it to another application scope. For more information, see [Copy a flow](copy-flow.md).|
    |Test|Test a flow before publishing it for other users. For more information, see [Test a flow](flow-test.md).|
    |Configure connections|Configure a connection through the Connections dashboard. For more information, see [Configure a connection](https://www.servicenow.com/docs/access?context=dashboard-configure-connection&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).|
    |Activate|Activate a flow to make it available to other users. For more information, see [Activate](flow-activate.md).|
    |Deactivate|Deactivate a flow to make it unavailable to other users.|
    |Configurations|Manage Workflow Studio configurations.|
    |Code snippet|Generate a code snippet to call a flow. For more information, see [Code snippet](flow-design-code-snippet.md).|
    |Executions|View runtime information about a flow from the design environment such as the current state, actions, or steps run, and data pill values produced. For more information, see [Executions](../concept/flow-execution-details.md).|
    |Flow Error Handler|Enable flows to catch errors. Run a sequence of actions and subflows to identify and correct issues. For more information, see [Flow Error Handler](../concept/flow-error-handler.md).|
    |Manage security|Manage access to Workflow Studio actions.|
    |Stages|Configure when stages display to a user, define stage state labels, and add stages to a flow within Workflow Studio. For more information, see [Stages](add-stages.md).|
    |Diagramming View|Create and view flows as diagrams. You can see the paths a flow can follow and the connections between elements. For more information, see [Diagramming View](../concept/flow-diagramming-view.md).|

    You can use these options to restrict access to Workflow Studio subflow authoring features.

    |Feature|Description|
    |-------|-----------|
    |Manage flow catalog variables|Create Service Catalog variables that are only available to a specific Service Catalog-triggered-flow. Flow-specific variables are available to the catalog tasks and actions in the flow. For more information, see [Manage flow catalog variables](create-flow-catalog-variables.md).|
    |Code snippet|Generate a code snippet to call a subflow. For more information, see [Code snippet](flow-design-code-snippet.md).|
    |Save|Save a subflow.|
    |Manage security|Manage the access to subflows.|
    |Properties|Configure how the system processes subflows. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Manage natural language title|Change the default title for a subflow by adding styled and dynamic text. For more information, see [Manage natural language title](manage-natural-language-title.md).|
    |Configure connections|Configure a connection through the Connections dashboard. For more information, see [Configure a connection](https://www.servicenow.com/docs/access?context=dashboard-configure-connection&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).|
    |Copy subflow|Copy a subflow to give it a new name and move it to another application scope. For more information, see [Copy a subflow](copy-subflow.md).|
    |Test|Test a subflow before publishing it for other users. For more information, see [Test a subflow](test-subflow.md).|
    |Publish|Publish a subflow to allow other users to use the subflow. For more information, see [Test](test-subflow.md).|
    |Configurations|Manage Workflow Studio configurations. For more information, see [Configure a connection](https://www.servicenow.com/docs/access?context=dashboard-configure-connection&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).|

    You can use these options to restrict access to Workflow Studio flow template authoring features.

    |Feature|Description|
    |-------|-----------|
    |Save|Save a flow template.|
    |Properties|Configure how the system processes flow templates. For more information, see [Properties](../reference/flow-designer-system-properties.md).|
    |Deactivate|Deactivate a flow template to make it unavailable to other users.|
    |Manage flow catalog variables|Create Service Catalog variables that are only available to a specific Service Catalog-triggered-flow. For more information, see [Manage flow catalog variables](create-flow-catalog-variables.md).|
    |Activate|Activate a flow template.|

4.  Continue adding roles to each feature on the list.

5.  Click **OK**.

6.  To turn on the feature access for your users, select the **Enable feature access filtering?** option.

    After the feature access is enabled, your users must have the required roles before they can access the features. If a user doesn't have the required roles for a feature, the feature does not work for that user.


## What to do next

Assign your users with the roles that they need to access your features.

**Parent Topic:**[User access to Workflow Studio flows](../concept/user-access-flow-designer.md)


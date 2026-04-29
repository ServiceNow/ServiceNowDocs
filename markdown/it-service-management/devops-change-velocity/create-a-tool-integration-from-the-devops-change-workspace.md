---
title: Create a tool integration from the DevOps Change Workspace
description: Create a tool integration from the DevOps Change Workspace for integrating additional orchestration, planning, and coding tools that are not available by default in the DevOps Change Velocity application.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Create a tool integration from the DevOps Change Workspace

Create a tool integration from the DevOps Change Workspace for integrating additional orchestration, planning, and coding tools that are not available by default in the DevOps Change Velocity application.

## Before you begin

Complete the tasks specified in [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md).

Role required: sn\_devops.admin or sn\_devops.tool\_owner

Set the application scope to the custom application.

## About this task

Watch this video to understand how to create a tool integration from the DevOps Change Workspace.

Create a tool integration from the DevOps Change Workspace 

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace**.

2.  In the DevOps workspace, navigate to **Administration** &gt; **Integrations** &gt; **Tool integrations**.

3.  Select **New**.

    Alternatively, you can open an existing tool integration record, and then select **Edit** \(for a custom tool integration that is not supported in the base system\).

    **Note:** For planning tools that are not supported in the base system, you can select **Edit** in the tool integration record to navigate to the Transformation step, where you can add any additional field. For planning tools that are supported in the base system, you can select **Edit field mappings** to add any additional field. For information on adding additional fields for supported planning tools, see [Add custom fields for a planning tool integration](add-custom-field-for-a-planning-tool-integration.md).

    The Details step is displayed.

4.  In the Tool details step, fill in the following:

    |Field|Description|
    |-----|-----------|
    |Tool label|Name of the tool integration.|
    |Integration version|API version of the tool integration.|

    ![Details step in tool integration creation](../image/custom-tool-details.png)

5.  Add an image of the tool’s logo by selecting **+Add file**.

6.  In the Tool type capabilities section, select the capability that your tool supports in the **Capabilities** field.

    |Capability|Description|
    |----------|-----------|
    |**Orchestration**|Tool that automated and coordinates the execution of complex processes in the software development life cycle.|
    |**Plan**|Tool that helps plan and manage the software development life cycle.|
    |**Code**|Tool that helps programmers write, edit, and manage code.|

    **Note:** A tool can be mapped to multiple tool type capabilities. Tool integration is supported for orchestration, plan, and code capabilities.

7.  Select **Next**.

    A tool integration record is created.

8.  In the Actions step, select the required actions for the tool capabilities selected in the previous step. ![Actions step in tool integration creation](../image/custom-tool-actions.png)

    **Note:** Tool capability actions are defined processes that enables the DevOps Data Model to communicate with and import data from the tool integration. Each tool type capability needs its own set of actions.

9.  Select **Next**.

    Integration capability records for the selected actions are created with default values.

10. In the Configurations step, add any additional configurations that are needed for your tool by selecting **Add field**. ![Configurations step in tool integration creation](../image/custom-tool-configurations.png)

    The fields configured here will be displayed as parameters for the playbook whenever you are onboarding a tool.

11. Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Field name|Name of the configuration.|
    |Order|Sequence in which this configuration is processed.|
    |Label|Label of the configuration.|
    |Mandatory|If marked true, this will appear as a connection detail when connecting an instance of this tool integration.|
    |Field type|Type of the field, which can be string or password|
    |Default value|Default value of this configuration.|
    |Help text|If this configuration is mandatory, then the help text appears for this field in connection details when connecting an instance of this tool.|

12. Select **Next**.

    A tool integration configuration record is created for the additional field.

13. In the Transformation step, review the transformation for each tool capability action, and add any custom field to the tool integration.

    A generic transform script is provided for each tool action. You can extend the generic script which calls the transformer-based mapping or create record transformers and manually map it to the fields. To extend, you can create a new script by extending the DevOpsGenericIntegrationHandlerSNC class to override the required method, and use this newly created script in the transform script.

    -   Enter the resource path API endpoint in the **Resource path** field if you use the generic script. ![Transformation step in tool integration creation](../image/custom-tool-transformation-script.png)
    -   If not already available, create a record transformer for the Notification, Discover, and Import actions for each of the capabilities by selecting the **Create a record transformer**, and add record transformer rules to map fields in your tool to fields in the DevOps Data Model. For information on creating a record transformer and manually mapping it to the field, see [Add custom fields for a planning tool integration](add-custom-field-for-a-planning-tool-integration.md). ![Transformation step - Record transformer section in tool integration creation](../image/custom-tool-record-transformer.png)
14. In Next steps, you can validate your tool integration by connecting to an instance of the tool through the playbook experience, and you can also view the tool integration record. ![Next steps in tool integration creation](../image/custom-tool-next-steps.png)

    **Note:** On selecting the **Connect to a tool** button, you will see the newly created tool integration in the list of tools available to connect.


## What to do next

[Creation of webhooks to send inbound events to DevOps Change Velocity using token](create-webhooks-to-send-inbound-events-to-devops-change-velocity-using-token.md)

-   **[Creation of webhooks to send inbound events to DevOps Change Velocity using token](create-webhooks-to-send-inbound-events-to-devops-change-velocity-using-token.md)**  
You must create webhooks to send inbound events to DevOps Change Velocity using token based authentication.

**Parent Topic:**[User-created integrations in DevOps Change Velocity](../concept/dev-ops-tool-integration.md)


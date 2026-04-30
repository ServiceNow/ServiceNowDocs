---
title: Create a DevOps tool integration
description: To create a DevOps tool integration, your integration developer configures DevOps tool integration settings, and a Workflow Studio subflow to collect and transform data from the source tool. Then your DevOps admin configures your DevOps tool connections.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Create a DevOps tool integration

To create a DevOps tool integration, your integration developer configures DevOps tool integration settings, and a Workflow Studio subflow to collect and transform data from the source tool. Then your DevOps admin configures your DevOps tool connections.

## Before you begin

**Note:** When creating an integration as a scoped app, the system admin must assign these roles to the integration developer so the integration developer is able to create tool integration and integration capability records for the specific scope.

-   Developer role for the scoped app
-   DevOps admin role

Role required: sn\_devops.admin

## About this task

Creating a DevOps tool integration procedure involves configuration by both your integration developer and your DevOps admin.

-   Your integration developer creates a tool integration record in DevOps, a Workflow Studio [subflow](../concept/creating-dev-ops-subflows.md), a tool capability mapping, and an integration capability record in DevOps to map the capabilities and actions together.

    **Note:** Notification, connect, and discover capabilities are supported.

-   Your DevOps admin sets up DevOps connections \(planning or coding tool\), and configures the source tool with the webhook and credentials.

This procedure provides detailed steps to create your DevOps tool integration.

## Procedure

1.  Integration developer:

    Configure the source tool integration capabilities and actions, and a subflow.

    1.  Navigate to **DevOps** &gt; **Integrations** &gt; **Tool Integrations** and create a record to define the tool you are integrating \(source tool\).

        **Note:** Do not edit the tool integration records provided with the DevOps application.

<table id="table_ets_r12_v3b"><tbody><tr><td>

Tool label

</td><td>

Sample Code Tool

</td></tr><tr><td>

Table

</td><td>

Code Tool \[sn\_devops\_tool\]

</td></tr><tr><td>

Use packageable integrations

</td><td>

Selected

</td></tr><tr><td>

Integration version

</td><td>

1.0

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr></tbody>
</table>    2.  Navigate to **Flow Designer** &gt; **Designer** and [create a subflow](../concept/creating-dev-ops-subflows.md) to collect and transform data from the tool you are integrating \(source tool\).

        **Note:** The **Run As** field must be set to System User, and the **Inputs** label must be set to current variable.

<table id="table_vxw_n4j_v3b"><tbody><tr><td>

Name

</td><td>

Code Tool Notification

</td></tr><tr><td>

Application

</td><td>

Sample Integration App

</td></tr><tr><td>

Accessible From

</td><td>

All application scopes

</td></tr><tr><td>

Description

</td><td>

Code tool for integration app

</td></tr><tr><td>

Run As

</td><td>

System User

</td></tr></tbody>
</table>        The subflow must contain Get More Data via API calls, and/or transform the original payload. Copy the transformed payload into the inbound events record.

        **Note:** Do not edit the DevOps main flow.

    3.  Navigate to **DevOps** &gt; **Integrations** &gt; **Tool Capability Mappings** and create a record to map the tool integration record to the tool type capability.

<table id="table_egd_jyw_wkb"><tbody><tr><td>

Tool integration

</td><td>

Sample tool

</td></tr><tr><td>

Tool type capability

</td><td>

Code

</td></tr></tbody>
</table>    4.  Navigate to **DevOps** &gt; **Integrations** &gt; **Integration Capabilities** and create a record to specify the action for the tool capability mapping.

        **Note:** Do not edit the integration capability records provided with the DevOps application.

<table id="table_yly_xnc_djb"><tbody><tr><td>

Tool integration

</td><td>

Sample Code Tool

</td></tr><tr><td>

Capability mapping

</td><td>

Sample Code Tool-Code

 **Note:** Do not edit tool type capability records.

</td></tr><tr><td>

Action

</td><td>

Notification

 **Note:** Do not edit tool action records.

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr><tr><td>

Timeout \(ms\)

</td><td>

Timeout for the corresponding subflow. If execution of the subflow exceeds this value, a timeout exception occurs.

 Value is in milliseconds \(ms\). Default is 45,000 \(45 seconds\).

</td></tr><tr><td>

Subflow name

</td><td>

x\_snc\_sample\_integ.code\_tool\_notification

 The name is prefixed by the scope name and a dot \(.\) before the actual subflow name.

 For example, given:

-   `connect_code_tool` subflow
-   `my_app_scope` scope
The value for this field is `my_app_scope.connect_code_tool`.

 **Note:** If the **Subflow name** field is left blank for a Notification capability, default handling of notifications occurs.

See [Notification tool capability action](../concept/dev-ops-tool-integration.md#section_h44_1bx_zjb).

</td></tr><tr><td>

Domain

</td><td>

global

</td></tr></tbody>
</table>2.  DevOps admin:

    Configure the connection from DevOps to the source tool.

    1.  The tool record must contain:

        -   Reference to the tool integration record created by the integration developer \(in the **Tool** field\)
        -   Tool label
        -   Connection alias \(connection and credential\)
    2.  Copy the notification \(webhook\) created on the DevOps planning tool to the source tool service hook of the notification endpoint and set the credentials to devops.integration.user.

    You can view the state of integration events in the Inbound Event list \(**DevOps** &gt; **Administration** &gt; **Inbound Events**\).

    The inbound event record state is set to **Processed** once the object has been inserted into the DevOps Core table. Event states include New, In Progress, Processed, Unmatched, and Error.

3.  If the tool integration record and the subflow are created in a different scope, the DevOps admin must create two new Cross scope privileges records to allow the app to access the inbound events table.

    Navigate to **System Applications** &gt; **Application Cross-Scope Access** and create read and write cross scope privileges records to allow your app to access the inbound events table.

    |Field|Read|Write|
    |-----|----|-----|
    |Source Scope|Auto populated based on the current application|
    |Target Scope|DevOps|
    |Target Name|sn\_devops\_inbound\_event|
    |Target Type|Table|
    |Operation|Read|Write|
    |Status|Allowed|


## Example

![DevOpsToolIntegration](../image/dev-ops-tool-integration.png "DevOps tool integration")

![SubflowProperties](../image/dev-ops-subflow-properties.png "Workflow Studio subflow properties")

![Subflow](../image/dev-ops-subflow.png "Workflow Studio subflow")

![NotificationFlow](../image/dev-ops-notification-flow.png "Workflow Studio DevOps Integration - Notification flow")

![DevOps User Integration Mapping](../image/dev-ops-user-integration-map.png "DevOps tool capability mapping")

![IntegrationCapability](../image/dev-ops-integration-capability.png "Integration capability")

![IntegrationPlanningTool](../image/dev-ops-integration-planning-tool.png "Planning tool")

![CrossScopeAccess](../image/dev-ops-cross-scope-access.png "Cross scope access records (read and write)")

**Parent Topic:**[User-created integrations in DevOps Change Velocity](../concept/dev-ops-tool-integration.md)


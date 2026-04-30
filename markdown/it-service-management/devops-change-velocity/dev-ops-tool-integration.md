---
title: User-created integrations in DevOps Change Velocity
description: User-created integrations are for integrating additional planning, coding, and test tools that are not available by default in the DevOps Change Velocity application.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# User-created integrations in DevOps Change Velocity

User-created integrations are for integrating additional planning, coding, and test tools that are not available by default in the DevOps Change Velocity application.

The DevOps Change Velocity application includes tool definitions for integrating some common planning, coding, and [DevOps test tool integration](dev-ops-test-tool-integration.md), but you can also set up user-created integrations for additional tools in your DevOps environment.

## Integration objects

DevOps tool integration consists of these objects.

![DevOpsToolIntegrationsImage](../image/dev-ops-user-integrations.png)

## Tool capability actions

-   **Connect** action:

    When connecting, the subflow for the specific tool is called and the connection state is updated. The connection status message is shown on the form.

    See [Connect capability subflow](creating-dev-ops-subflows.md#section_tkj_jzf_1kb) for more details.

-   **Discover** action:

    When discovering, an import request record is created and the subflow for the specific tool is called \(as defined in the Integration Capability record\). **Detail** and **Status** fields in the Import Request record are updated with the number of items discovered, updated, and failed.

    The transformed payload consists of an array of objects as a JSON string. Elements vary depending on the tool type.

    See [Discover capability subflow](creating-dev-ops-subflows.md#section_sgn_lzf_1kb) for more details.

-   **Import** action:

    Import action does not support historical import functionality.

-   **Lookup** action:

    The Lookup main flow is provided to support artifact tool type in a subflow created by your integration developer.

-   **Notification** \(webhook\) action:

    The source tool is configured manually \(by your integration developer\) to send raw data to the ServiceNow instance. The raw payload is then transformed into a standard JSON object using a subflow.

    See the [Notification capability subflow](creating-dev-ops-subflows.md#section_ep4_txg_w3b) and the [DevOps - POST /devops/tool/\{capability\}](https://www.servicenow.com/docs/access?context=devops-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) endpoint of the [DevOps API](https://www.servicenow.com/docs/access?context=devops-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) for more details.

    **Note:** If a subflow is not specified, default handling of notifications occurs \(`original payload` is automatically copied to `transformed payload`\).

    This behavior is useful when the transactional data of the tool is supported by ServiceNow DevOps as is.

    See the expected standard payloads in the [Notification capability subflow](creating-dev-ops-subflows.md#section_ep4_txg_w3b) for more details.


## DevOps integration configuration overview

Tool integration configuration can be completed by your integration developer and your DevOps admin.

-   **Integration developer**
    -   Create a tool integration record in DevOps to define the tool you are integrating \(source tool\).
    -   Create a Workflow Studio [subflow](creating-dev-ops-subflows.md) to collect and transform data from the tool you are integrating \(source tool\).
    -   Create a tool capability mapping record in DevOps to map the tool integration record to the tool type capability.

        **Note:** Notifications \(webhook\) capability is supported. Connect and discover capabilities are also supported.

    -   Create an integration capability record in DevOps to specify the action for the tool type capability.
-   **DevOps admin**
    -   Create a \(planning, coding, or test\) tool record in DevOps to connect to the tool you are integrating \(source tool\).

        **Note:** The tool integration record must be specified in the **Tool** field of the tool record.

    -   Configure the source tool with the webhook and credentials.

## Inbound events

An inbound event serves as a staging area for the notifications flow that supports reprocessing of failed payloads. Meaning, a record in an error state from a failed integration or transformation can be retried.

If an Inbound Event record is in the **Error** state, the flow was not able to insert the record successfully into the core DevOps tables.

Common errors can be resolved with these actions.

<table id="table_xhy_k4f_2jb"><thead><tr><th>

Error

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Missing required fields

</td><td>

The transformed payload does not match the standard payload.

 Refer to the standard and JSON payloads provided.

</td></tr><tr><td>

Repository not marked for tracking

</td><td>

The commit cannot be inserted.

 The DevOps admin needs to track the repository.

</td></tr><tr><td>

\[Subflow\] has not been published within application scope \[app\_scope\]

</td><td>

The subflow is created but not published yet.

</td></tr><tr><td>

Timeout exception

</td><td>

The subflow takes more time than the value set in the property: **com.glide.hub.flow\_api.default\_execution\_time**

 See [FlowAPI - executeSubflowQuick\(String name, Map inputs, Number timeout\)](https://www.servicenow.com/docs/access?context=ScriptableFlowAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) for more details.

 **Note:** The execution of the subflow exceeds the value set in the **Timeout** field in the Integration Capability record.

</td></tr><tr><td>

Did not find a matching subflow for notification capability and \[tool\_integration\_sys\_id\] tool integration

</td><td>

The flow was not able to find the matching subflow.

 Verify the integration setup procedure.

</td></tr><tr><td>

Payload does not match the expected capability.

</td><td>

The **Original payload** \(payload being sent\) is a different **Capability** type than the tool type capability configured in your tool capability mapping.

 The payload type must match the tool type capability configured in your tool integration.

</td></tr></tbody>
</table>**Note:** An inbound event record is not created when any of the following conditions occur:

-   Source tool has not passed the tool ID as a query parameter.
-   Source tool has passed on a tool ID, but there is no matching tool ID in the instance.

## Tool mappings

A tool can be mapped to multiple capabilities.

<table id="table_w5z_p31_2jb"><thead><tr><th>

Tool Integration

</th><th>

Tool Type Capability

</th><th colspan="2">

Tool Capability Mapping

</th></tr></thead><tbody><tr><td>

-   Agile Development 2.0
-   Azure DevOps
-   Bitbucket
-   GitHub
-   GitHub Enterprise
-   GitLab
-   Jenkins
-   Jira
-   Rally

</td><td>

-   Plan
-   Code
-   Orchestration
-   Artifact
-   Test

</td><td colspan="2">

Plan

-   Agile Development 2.0 - Plan
-   Azure DevOps - Plan
-   Jira - Plan
-   Rally - Plan

 Code

-   Azure DevOps - Code
-   Bitbucket - Code
-   GitHub - Code
-   GitHub Enterprise - Code
-   GitLab - Code

 Orchestration

-   Azure DevOps - Orchestration
-   Jenkins - Orchestration
-   GitLab - Orchestration

 Test

-   Azure DevOps - Test
-   Jenkins - Test

</td></tr></tbody>
</table>A tool capability mapping can be mapped to multiple actions.

<table id="table_ep4_qcw_wkb"><thead><tr><th>

Tool Capability Mapping

</th><th>

Tool Action

</th><th colspan="2">

Integration Capability

</th></tr></thead><tbody><tr><td>

-   Agile Development 2.0 - Plan
-   Azure DevOps - Plan
-   Azure DevOps - Code
-   Azure DevOps - Orchestration
-   Bitbucket - Code
-   GitHub - Code
-   GitHub Enterprise - Code
-   GitLab - Code
-   GitLab - Orchestration
-   Jenkins - Orchestration
-   Jira - Plan
-   Rally - Plan

</td><td>

-   Connect
-   Discover
-   Import
-   Lookup
-   Notification

</td><td colspan="2">

Agile Development 2.0-   Agile Development 2.0 - Plan - Connect
-   Agile Development 2.0 - Plan - Discover
-   Agile Development 2.0 - Plan - Import
-   Agile Development 2.0 - Plan - Notification

 Azure DevOps

-   Azure DevOps - Plan - Connect
-   Azure DevOps - Plan - Discover
-   Azure DevOps - Plan - Notification
-   Azure DevOps - Code - Discover
-   Azure DevOps - Code - Notification
-   Azure DevOps - Orchestration - Discover
-   Azure DevOps - Orchestration - Notification

 Bitbucket

-   Bitbucket - Code - Connect
-   Bitbucket - Code - Discover
-   Bitbucket - Code - Import
-   Bitbucket - Code - Notification

 GitHub

-   GitHub - Code - Connect
-   GitHub - Code - Discover
-   GitHub - Code - Import
-   GitHub - Code - Notification

 GitHub Enterprise

-   GitHub - Code - Connect
-   GitHub - Code - Discover
-   GitHub - Code - Import
-   GitHub - Code - Notification

 GitLab

-   GitLab - Code - Connect
-   GitLab - Code - Discover
-   GitLab - Code - Notification
-   GitLab - Orchestration - Notification

 Jenkins

-   Jenkins - Orchestration - Connect
-   Jenkins - Orchestration - Discover
-   Jenkins - Orchestration - Import
-   Jenkins - Orchestration - Notification

 Jira

-   Jira - Plan - Connect
-   Jira - Plan - Discover
-   Jira - Plan - Import
-   Jira - Plan - Notification

 Rally

-   Rally - Plan - Discover
-   Rally - Plan - Import
-   Rally - Plan - Notification
-   Rally - Plan - Connect
-   Rally - Plan - Validate

</td></tr></tbody>
</table>Multiple test types can be mapped to each tool integration.

<table id="table_cc3_z5l_vlb"><thead><tr><th>

Test Type

</th><th>

Tool Integration

</th><th>

Test Type Mapping

</th></tr></thead><tbody><tr><td>

Unit: JUnit, XUnit, NUnit, Unit test

 Functional:

-   Integration
-   Regression
-   Smoke
-   System
-   User Acceptance

 Performance: Load

</td><td>

-   Azure DevOps
-   Jenkins
-   GitLab
-   GitHub
-   GitHub Enterprise

</td><td>

Azure DevOps

-   Azure DevOps - JUnit
-   Azure DevOps Nunit
-   Azure DevOps Xunit
-   Azure DevOps Unit test
-   Azure DevOps - Integration
-   Azure DevOps - Regression
-   Azure DevOps - Smoke
-   Azure DevOps - System
-   Azure DevOps - User Acceptance
-   Azure DevOps - Load

 Jenkins

-   Jenkins - JUnit
-   Jenkins - Integration
-   Jenkins - Regression
-   Jenkins - Smoke
-   Jenkins - System
-   Jenkins - User Acceptance
-   Jenkins - Load

 GitLab

-   GitLab - JUnit
-   GitLab - Integration
-   GitLab - Regression
-   GitLab - Smoke
-   GitLab - System
-   GitLab - User Acceptance
-   GitLab - Load

 GitHub and GitHub Enterprise

-   GitHub - JUnit
-   GitHub Nunit
-   GitHub Xunit
-   GitHub Unit test
-   GitHub - Integration
-   GitHub - Regression
-   GitHub - Smoke
-   GitHub - System
-   GitHub - User Acceptance
-   GitHub - Load

</td></tr></tbody>
</table>-   **[DevOps test tool integration](dev-ops-test-tool-integration.md)**  
Test tool integration lets you view test results in DevOps for Jenkins, Azure DevOps, GitHub, GitHub Enterprise, and GitLab unit, functional, and performance tests.
-   **[DevOps user-created security tool integration](devops-security-tool-integration.md)**  
You can integrate additional security tools that are not supported in the base system in DevOps Change Velocity.
-   **[DevOps user-created orchestration tool integration](devops-user-created-orchestration-tool-integration.md)**  
Integrate DevOps Change Velocity with any orchestration tool that is not supported in the base system.
-   **[Create a DevOps tool integration](../task/set-up-dev-ops-integrations.md)**  
To create a DevOps tool integration, your integration developer configures DevOps tool integration settings, and a Workflow Studio subflow to collect and transform data from the source tool. Then your DevOps admin configures your DevOps tool connections.
-   **[Creating DevOps subflows](creating-dev-ops-subflows.md)**  
For user-created integrations, create a DevOps Workflow Studio subflow to collect and transform data from the tool you are integrating.
-   **[Add custom fields for a planning tool integration](../task/add-custom-field-for-a-planning-tool-integration.md)**  
Add custom fields into your planning tool integration to improve configurability and access business-specific information, which facilitates more informed decision-making.
-   **[Create a tool integration from the DevOps Change Workspace](../task/create-a-tool-integration-from-the-devops-change-workspace.md)**  
Create a tool integration from the DevOps Change Workspace for integrating additional orchestration, planning, and coding tools that are not available by default in the DevOps Change Velocity application.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)


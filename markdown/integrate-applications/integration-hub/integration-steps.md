---
title: Integration steps
description: Enable custom actions to integrate with external systems by activating Integration Hub, which adds integration steps to the Workflow Studio interface.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Build integrations, Integration Hub, Workflow Data Fabric]
---

# Integration steps

Enable custom actions to integrate with external systems by activating Integration Hub, which adds integration steps to the Workflow Studio interface.

Integration steps can run on the instance or a MID Server. A MID Server is required to communicate with or move data between a ServiceNow instance and external applications, data sources, and services in your network.

**Note:** Only Flow Designer admin and Connection admin can execute flows using Integration Hub.

Steps that perform operations on record data run on the instance, while steps that integrate with systems in your network run on a MID Server. If a step requires a MID Server to run, the instance delegates flow processing to the appropriate MID Server by sending the process plan in a REST call. The MID Server executes the action or step in the process plan and returns results. View log messages and execution status from the instance or the MID Server.

## Available integration steps

These integration steps are available from Workflow Studio - Building custom actions.

<table id="table_ypl_5zs_rcb"><thead><tr><th>

Integration step

</th><th>

Description

</th><th>

Step runs from

</th></tr></thead><tbody><tr><td>

[JDBC step](../../flow-designer/reference/jdbc-step.md)

</td><td>

Create a reusable action to send SQL commands to a relational database.

</td><td>

MID Server

</td></tr><tr><td>

[JSON Builder step](../../flow-designer/reference/json-build-step-action-designer.md)

</td><td>

Create a JSON payload to use in another step. Enter values or use data pills to produce a dynamic payload. This step supports several data types, including objects and arrays for nested structures.

</td><td>

Instance

</td></tr><tr><td>

[Payload Builder step](../../flow-designer/reference/payload-build-step-action-designer.md)

</td><td>

Enable action designers to easily create name-value pairs in JSON and XML payloads using dynamic data.

</td><td>

-   Instance
-   MID Server

</td></tr><tr><td>

[PowerShell step](../../flow-designer/reference/powershell-step-action-designer.md)

</td><td>

Run PowerShell scripts on remote machines from your ServiceNow instance through a MID Server.

</td><td>

MID Server

</td></tr><tr><td>

[REST step](../../flow-designer/reference/rest-request-action-designer.md)

</td><td>

Send an outbound REST web service request to an external system.

</td><td>

-   Instance
-   MID Server

</td></tr><tr><td>

[SOAP step](../../flow-designer/reference/soap-step-action-designer.md)

</td><td>

Enable action designers to send outbound SOAP web service requests to external systems.

</td><td>

-   Instance
-   MID Server

</td></tr><tr><td>

[SSH step](../../flow-designer/reference/ssh-step-action-designer.md)

</td><td>

The SSH step executes SSH commands on an external \*nix system through a ServiceNow® MID Server. The step also stores scripts and commands for the \*nix systems.

</td><td>

MID Server

</td></tr><tr><td>

[XML parser step](../../flow-designer/reference/xml-parser-step-action-designer.md)

</td><td>

Identify structured data from an XML payload without having to write script. Map incoming XML elements to a complex object output that you can use in other steps or actions. At runtime, values from an XML payload populate the complex object output.

</td><td>

-   Instance
-   MID Server

</td></tr></tbody>
</table>## Training

Complete a step-by-step training on using the REST step in the [REST in IntegrationHub developer training](https://developer.servicenow.com/dev.do#!/learn/courses/tokyo/app_store_learnv2_rest_tokyo_rest_integrations/app_store_learnv2_rest_tokyo_rest_in_integrationhub/app_store_learnv2_rest_tokyo_rest_in_integrationhub_objectives).

## Connection attributes

Define connection-specific variables that you can use in Integration Hub integration steps. When using an integration step, you must establish a connection with an external system. Use a Connection &amp; Credential alias instead of defining the connection inline. An alias enables you to update the connection details once without having to reconfigure every action. Any action step that uses an alias inherits the attributes associated with it. Workflow Studio displays attributes as data pills that you can drag into your action step. For example, you can create a page size attribute that becomes a REST step query parameter. For more information about connection attributes, see Create connection attributes for IntegrationHub.

## MID Server connection aliases

Action designers can set MID Server selection attributes using a connection record associated with an alias and associate the alias with an integration step. When the flow runs, the system uses the attributes to determine which MID Server runs the step. Learn more about Introduction to credentials, connections, and aliases.

## MID Server and MID Cluster selection

For most integration steps, you can specify a MID Server or MID Cluster for the step to use when it runs. For a MID Server, you can select one you've configured or have the system choose one by selecting **Auto-Select MID Server** from the step's MID Selection list. To learn more about how a MID Server is selected during runtime, see MID Server selection. For MID Clusters, you can select a load-balancing or fail-over cluster for the step. For more information on MID Clusters, see Configure a MID Server cluster. The Payload Builder step and XML Parser step do not support MID Server selection.

When specifying a MID Server, Flow designers should avoid shifting the execution environment from one MID Server to another when a flow runs. Either configure each MID Server to perform operations on multiple endpoints, or provide multiple capabilities to each MID Server in your network. You may need a user with the connection\_admin role to update the connection records associated with an action, or a network administrator to update the MID Server network configuration.

## Design considerations

Design integration steps using the following guidelines.

-   Avoid shifting the execution environment between the instance and the MID Server multiple times. Where possible, group similar action steps. For example, group core steps that perform record operations and integration steps that run on the MID Server.
-   When creating a spoke that uses an integration step, include a Connection and Credential alias record with the appropriate connection type. Before anyone can use the spoke, a user with the connection\_admin role must associate the alias record to a connection record that supports the connection type. If defining the connection inline, use inputs to enable the process analyst to define the connection information when adding the action to a flow.
-   The MID Server does not have access to all the values in a GlideRecord object, it only has access to the sys\_id reference. Inputs of type Reference do not work on a MID Server. Instead, create action inputs that contain the necessary GlideRecord values.

## Roles

To create integration steps, a user must have the action\_designer or admin roles. If running steps on a MID Server, the MID Server user must have the connection\_admin and credential\_admin roles to access the connection and credential information associated with the step.


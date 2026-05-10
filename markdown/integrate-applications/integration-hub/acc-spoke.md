---
title: Agent Client Collector Spoke
description: Automate the process of executing commands on agents or configuration items \(CI\) using the ServiceNow Agent Client Collector spoke. Agent Client Collector framework allows you to execute commands on the systems where it is installed and sends output data to the ServiceNow instance through the MID Server.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Agent Client Collector Spoke

Automate the process of executing commands on agents or configuration items \(CI\) using the ServiceNow Agent Client Collector spoke. Agent Client Collector framework allows you to execute commands on the systems where it is installed and sends output data to the ServiceNow® instance through the MID Server.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Agent Client Collector spoke v1.1.5 is the latest version.

## Supported versions

This spoke was built for Agent Client Collector framework v2.2.0, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ITOM Visibility License \(com.snc.itom.vis.license\)
-   Agent Client Collector Framework v2.2.0 \(sn\_agent\)

    **Note:** To enable Agent Client Collector to execute commands, ensure that `ACC_ALLOW_LIST=0` for Linux environments or `ACC_ALLOW_LIST=False` for Windows environments.


**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Agent Client Collector spoke provides sample subflows to demonstrate automating Agent Client Collector framework tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Managing Compliance for Remote Workers|Manages compliance for remote workers and sends an email to the system administrator when one or more specified compliance conditions are violated.|
|Restart Agent|Verifies the status of an agent and restarts the agent if the status is down.|
|SNH CyberAttack Detection|Applies SigHealth CyberAttack Detection for Windows server and send an email to the system administrator when a threat is detected.|
|Install Agent on Linux|Installs Agent Client Collector on a Linux hosts.|
|Install Agent on Windows|Installs Agent Client Collector framework on multiple windows hosts.|

## Spoke actions

The Agent Client Collector spoke provides actions to automate Agent Client Collector tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_oc2_ryf_p4b"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Get Agent Status

</td><td>

Get the status of an agent.

</td></tr><tr><td>

Get Logged on Users

</td><td>

Retrieves the list of all logged-in users and the related metadata for the specified host system.

</td></tr><tr><td>

Get Network Statistics

</td><td>

Retrieves the list of all network interfaces and the related metadata for the specified host system.

</td></tr><tr><td>

Get Running Processes

</td><td>

Retrieves the list of all running processes and the related metadata for the specified host system.

</td></tr><tr><td>

Get Running Services

</td><td>

Retrieves the list of all running services in Windows OS and the related data for the specified host system.

</td></tr><tr><td>

Get System Details

</td><td>

Retrieves the hardware and software details of the specified agent.

</td></tr><tr><td>

Restart Agent

</td><td>

Restarts an agent.

</td></tr><tr><td>

Run Command on Agent

</td><td>

Runs a command on a given agent host. **Note:** Use caution while executing commands.

</td></tr><tr><td>

Run Osquery on Agent

</td><td>

Runs the specified Osquery on the specified agent host.

</td></tr><tr><td>

Install Agent on Linux

</td><td>

Installs Agent Client Collector framework on a Linux host.

</td></tr><tr><td>

Install Agent on Windows

</td><td>

Installs Agent Client Collector framework on windows host.

</td></tr></tbody>
</table>**Note:** To use the Install Agent on Linux and Install Agent on Windows spoke actions, navigate to **Agent Client Collector Spoke** &gt; **CIDR Ranges**, create a record to specify the required IP address or range of IP addresses.

For information about setting up the spoke, see [Set up the Agent Client Collector spoke](../task/setup-acc.md).

## MID Server requirements

To use these actions, your instance must have a MID Server set up and configured to use PowerShell. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md). For more information about the MID Server, see [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).


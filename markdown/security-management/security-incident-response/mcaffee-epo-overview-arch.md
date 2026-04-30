---
title: McAfee ePO integration
description: The McAfee ePO integration endpoint detection and response \(EDR\) capability that helps Security Operations Center \(SOC\) analysts identify cyberthreats and repair the damage caused by malicious files.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# McAfee ePO integration

The McAfee ePO integration endpoint detection and response \(EDR\) capability that helps Security Operations Center \(SOC\) analysts identify cyberthreats and repair the damage caused by malicious files.

## Overview

There are two sets of McAfee ePO capabilities used in this integration, the capabilities that invoke actions, such as isolating a host and initiating a malware scan, and the capabilities that run queries to gather system details and threat events. Both types of capabilities, the actions and the queries, are invoked from your ServiceNow AI Platform® instance. You can group these capabilities together so that they automatically run when a specific type of security event occurs, or, you can invoke them manually from a ServiceNow AI Platform® security incident.

The following McAfee ePO capabilities are available for this integration.

-   **Get system details**

    Gather system details that include operating system details.

-   **Initiate malware scan**

    Based on scan configuration and scheduling, initiate a scan of an impacted endpoint.

-   **Isolate/Unisolate host**

    Remove a system from network access for investigation and restore access to the network.

-   **List threat events**

    Gather compliance status and the most current threat events.


## Key features

This integration includes the following key features.

-   Supports automated triggering of McAfee ePO queries that are based on incident conditions.
-   Supports launching McAfee ePO capabilities manually from ServiceNow AI Platform® Security Incident Response \(SIR\) security incidents that perform on-demand actions.
-   The flexibility to create multiple profiles for triggering different types of McAfee ePO and ServiceNow AI Platform® Security Operations capabilities. These profiles gather threat event information or perform actions based on the conditions of specific incident categories such as malware.
-   Validate your profile configuration with a preview of the McAfee ePO results on SIR security incidents.
-   If tagging is enabled, security tags identify which McAfee ePO capabilities are initially launched by a workflow and when the queries or actions are successfully completed.
-   A complete audit trail of the McAfee ePO queries and actions is posted in the work notes on SIR security incidents, and commands from the ServiceNow AI Platform® are logged in the McAfee ePO console.
-   Supports multiple McAfee ePO consoles.

## ServiceNow Plugins

The com.snc.si\_dep plugin is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before installing and activating the other Security Operations applications.

The following Security Operations applications must be installed and activated from the ServiceNow Store. Install and then activate one application at a time in the order listed below to ensure a smooth installation:

1.  Security Integration Framework
2.  Security Support Common
3.  Security Support Orchestration
4.  Security Incident Response
5.  Security Incident Response Workspace

For more information on setting up your ServiceNow AI Platform instance for the integration, see [Set up your ServiceNow AI Platform instance for the McAfee ePO integration](../reference/mcaffee-epo-setup-now.md).

## The ServiceNow extension plugin

The ServiceNow Security Operations Extension for McAfee ePO℠ extension plugin is required for this integration. You install this ServiceNow plugin in your McAfee ePO console. For more information, see [Set up your ServiceNow AI Platform instance for the McAfee ePO integration](../reference/mcaffee-epo-setup-now.md).

## MID Server

This integration requires an installed and configured MID Server in your ServiceNow AI Platform® instance to connect to the McAfee ePO server \(console\). See the [ServiceNow Product Documentation website](https://servicenow.com/docs) for more information about MID Servers.

## Supported versions of McAfee

The integration supports version 5.9.1 &amp; 5.10 of McAfee ePO. It supports McAfee Agent: MA 5.5.1.388 For more information about McAfee products and the ePolicy Orchestrator, see the [McAfee product website](https://www.mcafee.com/en-us/index.html).

The integration supports the version 10.5 of the McAfee Endpoint Security Threat Prevention product. If you are not running version 10.5, consult with your McAfee ePO administrator to see if your version can support on-demand scans via tag actions.

McAfee ePO security tags are used in this integration. You are required to create these tags in your McAfee ePO console. For more information on these tags, see [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](../task/mcafee-epo-setup-mcafee.md).

## References

<table id="table_axk_n23_2gb"><thead><tr><th>

Reference

</th><th>

Document Identifier

</th><th>

Document Title

</th></tr></thead><tbody><tr><td>

1

</td><td>

McAfee product website

</td><td>

[McAfee product website](https://www.mcafee.com/en-us/index.html)

</td></tr><tr><td>

2

</td><td>

McAfee Business Product Documentation for ePolicy Orchestrator Cloud

</td><td>

[McAfee Product Documentation](https://docs.mcafee.com/bundle?value=225)

</td></tr><tr><td>

3

</td><td>

ServiceNow Product documentation website

</td><td>

[ServiceNow Product Documentation website](https://servicenow.com/docs)

</td></tr></tbody>
</table>For a checklist to track your progress with setting up, installing, and verifying results for the integration, see [Checklist for the McAfee ePO integration](../task/mcafee-epo_checklist.md).

For a smooth installation of the application and to help you verify expected results, follow the topics in the order they are presented.

1.  [Integration architecture for McAfee ePO](mcafee-epo-integration-architecture.md)  
The following topic is an overview of the system architecture and lists key features of the integration. This section also provides information about the setup steps that you are required to complete in your ServiceNow AI Platform instance and in the McAfee ePolicy Orchestrator \(McAfee ePO\) console prior to installing the application from the ServiceNow Store.
2.  [Checklist for the McAfee ePO integration](../task/mcafee-epo_checklist.md)  
Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.
3.  [Set up your ServiceNow AI Platform instance for the McAfee ePO integration](../reference/mcaffee-epo-setup-now.md)  
The following section lists the setup tasks that you’re required to complete in your ServiceNow AI Platform® instance prior to installing the application for the McAfee ePO integration.
4.  [Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](../task/mcafee-epo-setup-mcafee.md)  
The following section lists the setup steps that you are required to complete in your McAfee ePO console prior to installing the application from the ServiceNow Store for the integration.
5.  [Install the application and configure a server for the McAfee ePO integration](../task/mcaffe-epo-install.md)  
Before you invoke the workflows for the integration, install and configure the McAfee ePO application from the ServiceNow Store on your ServiceNow AI Platform instance. The configuration is required to connect to the McAfee ePO console.
6.  [Edit security tags in the ServiceNow AI Platform for the McAfee ePO integration](../task/mcafee-epo-match-tags.md)  
As part of the setup for the integration, edit the security tag names that you created in your McAfee ePO console in your ServiceNow AI Platform instance. Edit the tag names in your ServiceNow AI Platform instance so that they match the names of the tags in your McAfee ePO console.
7.  [Create an approval group](../task/create-approval-group-mcafee.md)  
Create an approval group for the McAfee ePO for Security Operations integration that can approve requests for isolating host machines, restoring them to the network.
8.  [McAfee ePO integration capability profiles](mcafee-epo-creating-profiles.md)  
As a user with the security incident administrator \(sn\_si.admin\) role, you create profiles for the McAfee ePO capabilities in your ServiceNow AI Platform® instance. You group queries or actions in profiles and determine which McAfee ePO capabilities you want to run when a new security incident is created.
9.  [Trigger McAfee ePO profile manually from a security incident](../task/mcafee-epo-submit-ih-fm-si.md)  
Trigger a capability profile manually from a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
10. [Trigger additional actions in McAfee ePO integration](../task/configure-additional-actions-mcafee.md)  
The List Threat Events and Initiate Malware Scan capabilities can be triggered from Run Additional Actions.​
11. [Using McAfee ePO integration in Analyst Workspace](../task/using-mcafee-integration-aws.md)  
Use the McAfee ePO integration to leverage the McAfee ePO capabilities on the SIR Analyst workspace.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

**Related topics**  


[Integration architecture for McAfee ePO](mcafee-epo-integration-architecture.md)


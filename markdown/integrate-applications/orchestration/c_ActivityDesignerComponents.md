---
title: Orchestration custom activity templates
description: Orchestration provides customizable activity templates to create and manage custom activities in the Workflow Editor.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Orchestration activity designer, Classic Orchestration, Data and Automation]
---

# Orchestration custom activity templates

Orchestration provides customizable activity templates to create and manage custom activities in the Workflow Editor.

You create and update different types of Orchestration activities with the Activity Designer using activity templates for SSH, PowerShell, REST, SOAP, JMS, SFTP, JDBC, JavaScript Probes, and Probes.

Hundreds of workflows can share these activities simultaneously. Before you change an activity, you should check the workflows that they are part of by clicking the form menu icon \(![form menu icon](../../../common/image/Form_MenuIcon.png)\) and selecting **Used In**. Any central change to a versioned activity automatically updates across workflows unless you have [pinned that activity](https://www.servicenow.com/docs/access?context=c_ActivityPinning&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

All the Orchestration Core activities are built using the Activity Designer in scoped applications. Custom activities can be developed in the global scope or their own application scope even if that scope is different from the scope of the workflow. Use [Activity scoping](c_ActivityScoping.md) when build your own activity packs.

-   **[Create a JDBC activity](../task/t_CreateAJDBCActivity.md#)**  
Create a custom JDBC activity to automate SQL commands and stored procedure calls to relational databases from workflow.
-   **[Create a SOAP web service activity](../task/t_CreateASOAPWebServiceActivity.md)**  
Use this template to create a custom SOAP activity.
-   **[Create a JavaScript Probe activity](../task/t_CreateAJavaScriptProbeActivity.md#)**  
Create a JavaScript Probe activity to instruct a MID server to execute server-side javascript.
-   **[Create a PowerShell activity](../task/t_CreateAPowershellActivity.md#)**  
Create a custom PowerShell activity return data to a workflow from a host using Microsoft PowerShell.
-   **[Create a REST web service activity](../task/t_CreateARESTWebServiceActivity.md#)**  
Use this procedure to create a custom REST web service Orchestration activity.
-   **[Create an SFTP activity](../task/t_CreateAnSFTPActivity.md#)**  
Create an activity that executes basic SFTP commands on a remote server.
-   **[Create a probe activity](../task/t_CreateAProbeActivity.md#)**  
Create an activity that runs a probe on the target host that is configured to return specific information..
-   **[Create an SSH activity](../task/t_CreateAnSSHActivity.md#)**  
Create an activity that extracts data from a target host that uses the SSH network protocol.
-   **[Create a run script activity](../task/t_CreateARunScriptActivity.md#)**  
Create an activity that runs any script.
-   **[Create a JMS activity](../task/t_CreateAJMSActivity.md#)**  
Create a custom JMS activity to retrieve or send messages to external systems using the Java Messaging Service.

**Parent Topic:**[Orchestration activity designer](c_WorkflowActivityDesigner.md)


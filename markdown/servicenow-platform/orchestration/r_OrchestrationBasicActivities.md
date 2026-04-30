---
title: Deprecated Orchestration activities
description: These Orchestration activities have been deprecated.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Activate Orchestration, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Deprecated Orchestration activities

These Orchestration activities have been deprecated.

## Run Probe

The Run Probe activity launches a MID Server probe on behalf of a document. All Orchestration activities that launch a probe on a target machine are based on the Run Probe activity. Your ServiceNow instance must have access to a MID Server configured to use SSH to run this activity.

**Important:** This activity is deprecated and is unavailable for new workflows. To replace the functionality of this probe, use the [Probe activity template](../../orchestration-activity-designer/task/t_CreateAProbeActivity.md#) to create a custom activity. Workflows from a previous release that use the Run Probe activity can continue to do so.

|Field|Description|
|-----|-----------|
|Probe|Select a MID Server probe from the list. This is the name of the probe as it appears in the discovery\_probes table.|
|Source for probe|Enter the IP address of the host system against which the probe runs \(the probe's target\).|
|Sensor script|The script to run using the results of the probe. The output from the probe is contained in a variable called *output*. Any error from the probe is contained in a variable called *error*.|

## SOAP Request

The SOAP Request activity executes a SOAP request on a target server.

**Important:** This activity is deprecated and is replaced by the [SOAP Message workflow activity](r_SOAPMessageActivity.md) activity. Workflows from a previous release that use the SOAP Request activity can continue to do so. However, this activity is not available for new workflows.

|Field|Description|
|-----|-----------|
|SOAP URL|The SOAP endpoint.|
|Username|User name for basic authentication credentials.|
|Password|Password for basic authentication credentials.|
|Envelope Script|Script for setting up parameters for the web service.|
|Sensor Script|The script to execute after the request has been made and a response has been received.|

-   **[Reactivate a deprecated activity](../task/t_ReactivateDeprecatedActivity.md)**  
Orchestration activities that were converted to activity packs are deprecated for upgraded and new instances but can be reactivated for use in new workflows.
-   **[SOAP Message workflow activity](r_SOAPMessageActivity.md)**  
The **SOAP Message** activity uses SOAP messages defined in the System Web Services plugin and can call the messages using a MID Server.
-   **[Probes used by Orchestration](../../../product/orchestration/reference/r_OrchestrationProbes.md)**  
Certain probes, controlled by MID Servers, perform Orchestration tasks on remote computers, such as restarting a server or creating virtual machines from templates.
-   **[PowerShell activities](../concept/c_OrchestrPowerShellActivities.md#)**  
PowerShell is built on the Windows .NET Framework and is designed to control and automate the administration of Windows machines and applications.
-   **[SSH activities](../concept/c_OrchestrationSSHActivities.md#)**  
SSH activities allow workflows to perform operations on Linux and Unix computers.

**Parent Topic:**[Activate Orchestration](../../../product/orchestration/task/t_ActivateOrchestration.md)


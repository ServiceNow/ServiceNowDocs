---
title: Non-persistent VDI parameters, scripts, and settings
description: Use this reference to find the Agent Client Collector mid-less installation command syntax, logon and logoff script file names and locations, and an installation command example when setting up a non-persistent VDI golden image.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/digital-end-user-experience-dex/non-persistent-vdi-scripts.html
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-05-12"
reading_time_minutes: 2
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Non-persistent VDI parameters, scripts, and settings

Use this reference to find the Agent Client Collector mid-less installation command syntax, logon and logoff script file names and locations, and an installation command example when setting up a non-persistent VDI golden image.

## Agent Client Collector mid-less installation command

Run the following command on the reference device to install Agent Client Collector in mid-less mode for non-persistent VDI use. Replace each placeholder with the value provided in your ServiceNow instance under **Agent Client Collector** &gt; **Agent Download**.

```
msiexec /i <path-to-msi> /quiet /qn /norestart CONNECT_WITHOUT_MID="true" ACC_CNC="<your-acc-gateway>:443" REGISTRATION_KEY="<your-registration-key>" INSTANCE_URL="<your-instance-url>" LOCALUSERNAME="SYSTEM"
```

The following table describes each parameter.

|Parameter|Description|
|---------|-----------|
|`/i <path-to-msi>`|Path to the Agent Client Collector MSI installer that you downloaded from the ServiceNow instance.|
|`/quiet /qn /norestart`|Installs the agent silently and prevents an automatic restart of the reference device after installation.|
|`CONNECT_WITHOUT_MID="true"`|Configures the agent to connect directly to the Agent Client Collector Cloud Native Connector \(CNC\) gateway without requiring a MID Server.|
|`ACC_CNC="<your-acc-gateway>:443"`|Hostname and port of your CNC gateway. Copy this value from the mid-less installation command in **Agent Client Collector** &gt; **Agent Download** on your ServiceNow instance.|
|`REGISTRATION_KEY="<your-registration-key>"`|Registration key issued by your ServiceNow instance for this agent.|
|`INSTANCE_URL="<your-instance-url>"`|Fully qualified URL of your ServiceNow instance, for example, `https://<instance>.service-now.com`.|
|`LOCALUSERNAME="SYSTEM"`|Configures the agent service to run as the local `SYSTEM` account. This setting is required for non-persistent VDI monitoring.|

## Logon and logoff scripts

The following table lists the file names, recommended locations, and purpose of the scripts that are required for non-persistent VDI sessions. Obtain these scripts from ServiceNow Customer Support before you configure the VDI pool.

If you place the PowerShell scripts in a location other than `C:\DEXScripts\`, update the corresponding `.cmd` wrapper to reference the new path.

|File name|Type|Recommended location|Purpose|
|---------|----|--------------------|-------|
|`logon_script.ps1`|PowerShell|`C:\DEXScripts\`|Restores the agent certificate from your persistent storage to the VDI when a session starts. Enables authentication without downloading a new certificate.|
|`logon_script.cmd`|CMD wrapper|Configured in your VDI management tool as the post-synchronization or session-start script|Calls `logon_script.ps1`. Update the path inside this file if you place the PowerShell script in a different location.|
|`logoff_script.ps1`|PowerShell|`C:\DEXScripts\`|Pushes residual metrics from the Agent Client Collector to the ServiceNow instance before the session disconnects.|
|`logoff_script.cmd`|CMD wrapper|Configured in your VDI management tool as the power-off or session-end script|Calls `logoff_script.ps1`. Update the path inside this file if you place the PowerShell script in a different location.|

## Non-persistent VDI settings in acc.yml

The following table lists the `acc.yml` settings that apply to a non-persistent VDI golden image. `acc.yml` is located at `C:\ProgramData\ServiceNow\agent-client-collector\`.

|Setting|Required value|Purpose|
|-------|--------------|-------|
|`persistence_type`|`non_persistent`|Defines that the agent runs on a non-persistent VDI.|
|`disable-asset`|`true`|Prevents the agent from re-using a single asset record across duplicate VDIs. Each duplicate VDI generates its own asset record on first start.|
|`agent-key-id`|Removed|Removed from the file before sealing the golden image so duplicate VDIs request a fresh key on first registration.|

**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-end-user-experience-dex/dex-console-reference.md)


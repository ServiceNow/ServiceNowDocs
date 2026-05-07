---
title: PowerShell probe version 2 system property
description: View detailed PowerShell credential information and view extended logging information.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [MID Servers for Orchestration, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# PowerShell probe version 2 system property

View detailed PowerShell credential information and view extended logging information.

Starting with the madrid release, there is a new system property for the PowerShell probe which enables the version 2 of the probe. This new version enables you to view detailed credential information on why PowerShell credentials fail or succeed. You can also view logging information for an ECC Queue payload and Workflow Context log.

**mid.server.rba\_powershell\_v2**

Enables the PowerShell probe version 2 for use with all PowerShell activities. The default value is true. If you choose false, the legacy PowerShell probe is used. Unless there are issues, use version 2, as the legacy version is going to be deprecated.

**Note:** This property only applies to Orchestration activities. Discovery probes are not affected.

You can access the property by selecting the MID Server Properties link in the navigation pane:

![Use PowerShell Probe v2](../image/powershell-probe-v2.png)

**Parent Topic:**[MID Servers for Orchestration](../../orchestration/concept/c_OrchestrationMID.md)


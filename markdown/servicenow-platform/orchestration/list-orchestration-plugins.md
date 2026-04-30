---
title: List of Orchestration plugins
description: This table lists all plugins available for Orchestration and their dependencies.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Activate Orchestration, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# List of Orchestration plugins

This table lists all plugins available for Orchestration and their dependencies.

These Orchestration plugins are available for purchase or can be requested as part of your Orchestration subscription. Contact your account representative for details.

<table id="table_t42_cgk_rw"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Orchestration \[com.snc.runbook\_automation\]

</td><td>

Main plugin for the Orchestration feature. This plugin extends Workflow to automate operations with external systems. Use this plugin to orchestrate business services, applications, and infrastructure.This plugin automates operations such as deployments, configurations, and information gathering. Orchestration can automate Web Services and uses MID Servers to execute commands on devices inside an enterprise's network.

</td><td>

-   Orchestration - ROI
-   Orchestration - Runtime

</td></tr><tr><td>

Orchestration - Active Directory \[com.snc.orchestration.ad\]

</td><td>

Installs the [Active Directory](../../../administer/orchestration-activities/concept/c_OrchActiveDirectoryActivities.md) activity pack. These activities create, delete, and manage objects in Windows Active Directory.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - Asset Lease Management \[com.snc.orchestration.asset\_lease\_management\]

</td><td>

Provides the software lease functionality for Client Software Distribution. Allows users to select the start and end dates of software leases and to request an extension of a lease.**Note:** This plugin is not automatically enabled when Orchestration is active.

</td><td>

None

</td></tr><tr><td>

Orchestration - Azure Active Directory \[com.snc.orchestration.azure.ad\]

</td><td>

Installs the [Azure AD](../../../administer/orchestration-activities/concept/c_AzureADActivityPack.md) activity pack. These activities automate employee onboarding and offboarding functions on Azure Active Directory and manage Office 365 licensing.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - Client Software Distribution \[com.snc.orchestration.client\_sf\_distribution\]

</td><td>

Allows the [distribution of software](../concept/c_ClientSoftwareDistribution.md) from the service catalog using third party management systems, such as Microsoft System Center Configuration Manager \(SCCM\)**Note:** This plugin is not automatically enabled when Orchestration is active.

</td><td>

-   Orchestration - System Center Configuration Manager
-   Orchestration - Asset Lease Management
-   Service Catalog Scoped API
-   Software Asset Management

</td></tr><tr><td>

Orchestration - Exchange \[com.snc.orchestration.exchange\]

</td><td>

Installs the [Exchange](../../../administer/orchestration-activities/concept/c_OrchestrationExchangeActivities.md) activity pack. These activities manage Microsoft Exchange mail systems.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - F5 network management \[com.snc.orchestration.f5\]

</td><td>

Installs the [F5 Network Management](../../../administer/orchestration-activities/concept/c_OrchF5LoadBalancerActivities.md) activity pack. These activities configure elements of an F5 load balancer, including pools, pool members, and the virtual servers contained in the pool.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - Infoblox DDI Activity Pack \[com.snc.orchestration.infoblox\]

</td><td>

Installs the [Infoblox DDI](../../../administer/orchestration-activities/concept/c_InfobloxDDIActivityPack.md) activity pack. These activities support Infoblox DDI management.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - PowerShell \[com.snc.orchestration.powershell\]

</td><td>

Installs the [PowerShell](../../../administer/orchestration-activities/concept/c_OrchestrPwrshellActivityPack.md) activity pack. These activities control and automate the administration of Windows machines and applications, using the Windows .NET Framework.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - Probe \[com.snc.orchestration.probe\]

</td><td>

Installs the [Probe](../../../administer/orchestration-activities/concept/probe_activity-pack.md#) activity pack. These activities run ServiceNow® probes on target hosts to return specific information.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - ROI \[com.snc.runbook\_automation.roi\]

</td><td>

Installs an Orchestration application that estimates savings resulting from automated tasks in an instance and computes actual savings. [Orchestration - ROI](../concept/c_OrchestrationROI.md) is activated automatically with a base Orchestration subscription.

</td><td>

-   Performance Analytics
-   Cost Management

</td></tr><tr><td>

Orchestration - ROI Premium \[com.snc.runbook\_automation.roi\_premium\]

</td><td>

Installs a premium dashboard that displays detailed reports on calculated savings for automated tasks over time. The [Orchestration - ROI Premium](r_OrchestrationROIPremiumDashboard.md#) plugin requires purchase and activation of the Performance Analytics - Premium plugin to display its reports.**Note:** This plugin is not automatically enabled when Orchestration is active.

</td><td>

-   Orchestration - ROI
-   Performance Analytics - Premium

</td></tr><tr><td>

Orchestration - Runtime \[com.snc.runbook\_automation.runtime\]

</td><td>

Enables other applications on the ServiceNow® platform to distribute and use orchestration content without requiring an Orchestration subscription. The [Orchestration - Runtime](orchestration-runtime-plugin.md) plugin displays the Orchestration activities shipped with these applications in the Workflow Editor and allows customers to modify the activities without requiring an Orchestration license.

</td><td>

-   Workflow Runtime Engine
-   Core Automation

</td></tr><tr><td>

Orchestration - SFTP \[com.snc.orchestration.sftp\]

</td><td>

Installs the [SFTP File Transfer](../../../administer/orchestration-activities/concept/c_OrchestrationSFTPActivityPack.md) activity pack. These activities manage files and directories on an SFTP server and move files from one SFTP server to another.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - SSH \[com.snc.orchestration.ssh\]

</td><td>

Installs the [SSH](../../../administer/orchestration-activities/concept/c_OrchestrationSSHCustomActivities.md) activity pack. These activities read, write, and copy files, and reset user passwords on Linux computers.

</td><td>

Orchestration

</td></tr><tr><td>

Orchestration - System Center Configuration Manager \[com.snc.orchestration.sccm\_mgnt\]

</td><td>

Installs the [System Center Configuration Manager \(SCCM\)](../../../administer/orchestration-activities/concept/c_SCCMActivityPack.md) activity pack. These activities manage software deployments and collections on an SCCM server.

</td><td>

Orchestration

</td></tr></tbody>
</table>**Parent Topic:**[Activate Orchestration](../task/t_ActivateOrchestration.md)


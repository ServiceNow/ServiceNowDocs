---
title: Client software distribution from SCCM
description: You can use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Client software distribution from SCCM

You can use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.

The [SCCM activity pack](../../../administer/orchestration-activities/concept/c_SCCMActivityPack.md) contains Orchestration activities that CSD uses to deploy software from a service catalog request and manage user and device collections on SCCM servers. In addition, CSD can manage license counts for deployed software using ServiceNow Software Asset Management, revoke software deployed by SCCM without user interaction, and manage lease periods.

-   **[Configuring SCCM](configuring-sccm.md)**  
Follow the SCCM configuration procedures in the order shown.
-   **[SCCM deployment](../reference/r_SCCMDeploymentProcessWorkflow.md)**  
Ordering an SCCM application from a client software distribution \(CSD\) catalog item in the service catalog triggers the Order Client Software workflow.
-   **[Client software distribution validation process](c_ClientSWDistValidProcess.md)**  
After SCCM deploys software to a target computer, client software distribution \(CSD\) detects the installation and validates its status.
-   **[SCCM software revocation](c_SCCMSoftwareRevocation.md#)**  
An administrator can revoke software without any user interaction using Microsoft System Center Configuration Manager \(SCCM\) if the software configuration specifies an SCCM uninstall collection, even if the software was installed by some other process or user.

**Parent Topic:**[Client Software Distribution](c_ClientSoftwareDistribution.md)


---
title: Client Software Distribution
description: The Client Software Distribution \(CSD\) application allows administrators to distribute software from the service catalog using third-party management systems.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Client Software Distribution

The Client Software Distribution \(CSD\) application allows administrators to distribute software from the service catalog using third-party management systems.

CSD allows an administrator to create all the records necessary to deploy software from service catalog requests, including software models and catalog items. You can use the CSD application to automate the deployment and [revocation](c_SCCMSoftwareRevocation.md#) of software from an SCCM host using the custom [SCCM activity pack](../../../administer/orchestration-activities/concept/c_SCCMActivityPack.md). You can define lease periods for software distributed from the Service Catalog and allow lease extensions in some cases, pending approvals. Deployment is accomplished using Orchestration activities and workflows.

CSD also integrates with [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SAMOverview&version=australia&pubname=australia-it-asset-management&ft:locale=en-US) to manage license counts for deployed software.

![Client Software Distribution process flow using SCCM](../image/CSDProcessFlowDiagram.png "CSD process flow using SCCM")

-   **[Request client software distribution](../task/t_ActivateClientSWDistribution.md)**  
Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Orchestration.
-   **[Installed with client software distribution](../reference/r_IWClientSWDist.md#)**  
Several types of components are installed with client software distribution \(CSD\).
-   **[Create licenses and counters for distributed software](../task/t_CreateLicsAndCountsForDistSW.md#)**  
Licenses and software counters are associated with the software model and must be created if you want to track the license for software deployed by client software distribution \(CSD\).
-   **[Extend a software lease](../task/extend-software-lease.md)**  
Users of software deployed by Client Software Distribution \(CSD\) can request the extension of a lease window, if the software is revocable by a software distribution system.
-   **[Client software distribution from SCCM](c_CSDFromAnSCCMHost.md)**  
You can use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.
-   **[Client software distribution dashboard](c_ClientSWDistributionDash.md)**  
The CSD dashboard provides a collection of visual reports for the Client Software Distribution application.
-   **[Client software distribution extension framework](c_CSDExtensionFramework.md)**  
Client software distribution \(CSD\) provides built-in extension points for integrating a ServiceNow instance with client software distribution providers, such as Casper, Altiris, or LANDesk.

**Parent Topic:**[Orchestration applications](c_OrchestrationApplications.md)


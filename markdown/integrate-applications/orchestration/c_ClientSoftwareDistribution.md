---
title: Client Software Distribution
description: The Client Software Distribution \(CSD\) application allows administrators to distribute software from the service catalog using third-party management systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/orchestration/c\_ClientSoftwareDistribution.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Client Software Distribution

The Client Software Distribution \(CSD\) application allows administrators to distribute software from the service catalog using third-party management systems.

CSD allows an administrator to create all the records necessary to deploy software from service catalog requests, including software models and catalog items. You can use the CSD application to automate the deployment and revocation of software from an SCCM host using the custom [SCCM activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_SCCMActivityPack.md). You can define lease periods for software distributed from the Service Catalog and allow lease extensions in some cases, pending approvals. Deployment is accomplished using Orchestration activities and workflows.

CSD also integrates with Software Asset Management to manage license counts for deployed software.

\[Omitted image "CSDProcessFlowDiagram.png"\] Alt text: Client Software Distribution process flow using SCCM

-   **[Request client software distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_ActivateClientSWDistribution.md)**  
Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Orchestration.
-   **[Installed with client software distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/r_IWClientSWDist.md)**  
Several types of components are installed with client software distribution \(CSD\).
-   **[Create licenses and counters for distributed software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateLicsAndCountsForDistSW.md)**  
Licenses and software counters are associated with the software model and must be created if you want to track the license for software deployed by client software distribution \(CSD\).
-   **[Extend a software lease](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/extend-software-lease.md)**  
Users of software deployed by Client Software Distribution \(CSD\) can request the extension of a lease window, if the software is revocable by a software distribution system.
-   **[Client software distribution from SCCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_CSDFromAnSCCMHost.md)**  
You can use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.
-   **[Client software distribution dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_ClientSWDistributionDash.md)**  
The CSD dashboard provides a collection of visual reports for the Client Software Distribution application.
-   **[Client software distribution extension framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_CSDExtensionFramework.md)**  
Client software distribution \(CSD\) provides built-in extension points for integrating a ServiceNow instance with client software distribution providers, such as Casper, Altiris, or LANDesk.

**Parent Topic:**[Orchestration applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationApplications.md)


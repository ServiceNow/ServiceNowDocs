---
title: Client Software Distribution using Integration Hub
description: Use Client Software Distribution \(CSD\) to distribute software from the Service Catalog using third-party management systems.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Client Software Distribution using Integration Hub

Use Client Software Distribution \(CSD\) to distribute software from the Service Catalog using third-party management systems.

Create all the records necessary to deploy software from Service Catalog requests, including software models and catalog items. You can use the CSD application to automate the deployment and [revocation](sccm-revocation-ihub.md) of software from an SCCM host using the [Microsoft SCCM spoke](microsoft-sccm-spoke.md). You can define lease periods for software distributed from the Service Catalog and allow lease extensions in some cases, pending approvals. Deployment is accomplished using Integration Hub flows, subflows, and actions.

Integrates with [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SAMOverview&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) to manage license counts for deployed software.

![CSD process flow using SCCM](../images/CSDProcessFlowDiagram.png "CSD process flow using SCCM")

-   **[Request client software distribution](../tasks/request-csd-ihub.md)**  
Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Integration Hub.
-   **[Components installed with client software distribution](../reference/comp-installed-csd-ihub.md)**  
Several types of components are installed with client software distribution \(CSD\).
-   **[Create licenses and counters for distributed software](../tasks/csd-license.md#)**  
Licenses and software counters are associated with the software model and must be created if you want to track the license for software deployed by client software distribution \(CSD\).
-   **[Extend a software lease](../tasks/csd-extend.md)**  
Users of software deployed by Client Software Distribution \(CSD\) can request the extension of a lease window, if the software is revocable by a software distribution system.
-   **[Client software distribution from SCCM](csd-from-sccm-ihub.md)**  
Use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.
-   **[Client software distribution dashboard](csd-dashboard.md)**  
The CSD dashboard provides a collection of visual reports for the Client Software Distribution application.
-   **[Client software distribution extension framework](csd-ext-framewrk.md)**  
Client software distribution \(CSD\) provides built-in extension points for integrating a ServiceNow instance with client software distribution providers, such as Casper, Altiris, or LANDesk.

**Parent Topic:**[Building integrations in Integration Hub](building-integrations-ih.md)


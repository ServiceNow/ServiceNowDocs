---
title: Client Software Distribution using Integration Hub
description: Use Client Software Distribution \(CSD\) to distribute software from the Service Catalog using third-party management systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/csd-integrationhub.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Client Software Distribution using Integration Hub

Use Client Software Distribution \(CSD\) to distribute software from the Service Catalog using third-party management systems.

Create all the records necessary to deploy software from Service Catalog requests, including software models and catalog items. You can use the CSD application to automate the deployment and [revocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/sccm-revocation-ihub.md) of software from an SCCM host using the [Microsoft SCCM spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/microsoft-sccm-spoke.md). You can define lease periods for software distributed from the Service Catalog and allow lease extensions in some cases, pending approvals. Deployment is accomplished using Integration Hub flows, subflows, and actions.

Integrates with [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/software-asset-management/c_SAMOverview.md) to manage license counts for deployed software.

\[Omitted image "CSDProcessFlowDiagram.png"\] Alt text: CSD process flow using SCCM

-   **[Request client software distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/request-csd-ihub.md)**  
Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Integration Hub.
-   **[Components installed with client software distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/comp-installed-csd-ihub.md)**  
Several types of components are installed with client software distribution \(CSD\).
-   **[Create licenses and counters for distributed software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/csd-license.md)**  
Licenses and software counters are associated with the software model and must be created if you want to track the license for software deployed by client software distribution \(CSD\).
-   **[Extend a software lease](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/csd-extend.md)**  
Users of software deployed by Client Software Distribution \(CSD\) can request the extension of a lease window, if the software is revocable by a software distribution system.
-   **[Client software distribution from SCCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/csd-from-sccm-ihub.md)**  
Use Client Software Distribution \(CSD\) to deploy and revoke software deployments from Microsoft System Center Configuration Management \(SCCM\) and manage distributions on SCCM hosts.
-   **[Client software distribution dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/csd-dashboard.md)**  
The CSD dashboard provides a collection of visual reports for the Client Software Distribution application.
-   **[Client software distribution extension framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/csd-ext-framewrk.md)**  
Client software distribution \(CSD\) provides built-in extension points for integrating a ServiceNow instance with client software distribution providers, such as Casper, Altiris, or LANDesk.

**Parent Topic:**[Building integrations in Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/building-integrations-ih.md)


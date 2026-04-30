---
title: Digital integrations in Enterprise Architecture Workspace
description: Manage all your digital integrations in the Enterprise Architecture Workspace.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with an application portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Digital integrations in Enterprise Architecture Workspace

Manage all your digital integrations in the Enterprise Architecture Workspace.

The digital integration functionality in Enterprise Architecture Workspace helps you to understand the business purposes for your applications, for their connection, and for their interaction. Install the Digital Integration Management \(sn\_apm\_di\) plugin from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/71e7ac97a33251109eb0cc4a66fcda0c/).

You can do the following:

-   Proactively find out the issues of the integrations at one place.
-   Manage the information flows across your organization.
-   Have complete governance over the use of interfaces for internal and external APIs.

The digital integration represents the integration between two business applications. In a typical scenario there would be a consuming business application, a provider business application, and an interface that is provided by the provider business application. The digital integration contains the metadata on the integration, including name, version, type, data flow direction, middleware used, owners, and so on.

An easy form for digital integration enables the creation of a digital integration from a single page, including the introduction of a new digital interface if it doesn’t exist. The digital integrations are saved in the Digital Integration \[sn\_apm\_di\_digital\_integration\] table. After a digital integration is created, a CI relationship link gets created between the two business applications with the type of interface. This link enables you to access the integration as part of the node map for any business application. A new catalog entry is provided to request an approval for a new digital integration. After the request is approved, the integration gets created.

The Digital Integrations page displays a list of existing digital integrations and their related information. You can access the Digital Integrations page by navigating to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Portfolio** &gt; **Application Portfolio** &gt; **Digital Integrations**![Digital Integrations in Enterprise Architecture Workspace](../../image/eaw-image/eaw-digital-integrations.png).

-   **[Digital integration management data model](../../reference/eaw-reference/eaw-dig-intg-data-model.md)**  
This section shows the digital integration management data model.
-   **[View all digital integrations](../../task/eaw-task/eaw-view-all-dig-integ.md)**  
View the list of all your digital integrations in the Enterprise Architecture Workspace.
-   **[Add or edit a digital integration in the EA Workspace](../../task/eaw-task/eaw-create-digital-integ.md)**  
Add a digital integration or edit an existing digital integration in the EA Workspace. The digital integration is a design object used by the Enterprise Architects. It describes a connection between two business applications or between a business application and an external service \(for example: AWS, Yahoo, a TimeZone Conversion service\) that provides an interface \(API\) to interact with.
-   **[Manage architectural artifacts of a digital integration in EA Workspace](../../task/eaw-task/eaw-assoicate-artifact-dig-intgn.md)**  
You can create new, add, or remove the artifacts that are associated with a digital integration.

**Parent Topic:**[Working with an application portfolio](eaw-app-portfolio.md)


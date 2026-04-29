---
title: Exploring digital integrations in Enterprise Architecture Workspace
description: Manage all your digital integrations in the Enterprise Architecture Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring the application portfolio, Exploring Portfolio list view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exploring digital integrations in Enterprise Architecture Workspace

Manage all your digital integrations in the Enterprise Architecture Workspace.

The digital integration functionality in Enterprise Architecture Workspace helps you to understand the business purposes for your applications, for their connection, and for their interaction. Install the Digital Integration Management \(sn\_apm\_di\) plugin from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/71e7ac97a33251109eb0cc4a66fcda0c/).

You can do the following:

-   Proactively identify integration issues in one location.
-   Manage the information flows across your organization.
-   Govern interface usage for internal and external APIs.

The digital integration represents the integration between two business applications. In a typical scenario, there's a consuming business application, a provider business application, and an interface provided by the provider business application. The digital integration contains integration metadata, including name, version, type, data flow direction, middleware used, and owners.

An easy form for digital integration enables the creation of a digital integration from a single page, including the introduction of a new digital interface if it doesn't exist.The digital integrations are saved in the Digital Integration \[sn\_apm\_di\_digital\_integration\] table. After you create a digital integration, a CI relationship link is created between the two business applications with the interface type. This link enables you to access the integration as part of the node map for any business application. A catalog entry is provided to request approval for a digital integration. After the request is approved, the integration gets created.

The Digital Integrations page displays a list of existing digital integrations and their related information. You can access the Digital Integrations page by navigating to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Portfolio** &gt; **Application Portfolio** &gt; **Digital Integrations**![Digital Integrations in Enterprise Architecture Workspace](../../image/eaw-image/eaw-digital-integrations.png).

-   **[Digital integration management data model](../../reference/eaw-reference/eaw-dig-intg-data-model.md)**  
This section shows the digital integration management data model.

**Parent Topic:**[Exploring the application portfolio](eaw-app-portfolio.md)

**Related topics**  


[Digital integration management data model](../../reference/eaw-reference/eaw-dig-intg-data-model.md)

[View all digital integrations](../../task/eaw-task/eaw-view-all-dig-integ.md)

[Add or edit a digital integration in the EA Workspace](../../task/eaw-task/eaw-create-digital-integ.md)

[Manage architectural artifacts of a digital integration in EA Workspace](../../task/eaw-task/eaw-assoicate-artifact-dig-intgn.md)

[Associate an information object to a digital integration](../../task/eaw-task/eaw-dig-integ-add-info-object.md)


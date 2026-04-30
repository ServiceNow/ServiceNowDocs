---
title: Digital integrations
description: Manage digital integrations in Enterprise Architecture \(formerly Application Portfolio Management\).
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage digital integrations, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Digital integrations

Manage digital integrations in Enterprise Architecture \(formerly Application Portfolio Management\).

**Important:**

Starting with the Xanadu release, the legacy digital integrations module is moved to the Enterprise Architecture Workspace. To learn more, see [Exploring digital integrations in Enterprise Architecture Workspace](eaw-concept/eaw-digital-integration.md).

The digital integration represents the integration between two business applications. In a typical scenario there would be a consuming business application, a provider business application, and an interface that is provided by the provider business application. The digital integration contains the metadata on the integration, including name, version, type, data flow direction, middleware used, owners, and so on.

An easy form for digital integration enables the creation of a digital integration from a single page, including the introduction of a new digital interface if it doesn’t exist. The digital integrations are saved in the Digital Integration \[sn\_apm\_di\_digital\_integration\] table. After a digital integration is created, a CI relationship link gets created between the two business applications with the type of interface. This link enables you to access the integration as part of the node map for any business application. A new catalog entry is provided to request an approval for a new digital integration. After the request is approved, the integration gets created.

The Digital Integrations page displays a list of existing digital integrations and their related information. You can access the Digital Integrations page by navigating to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **Digital Integrations**.

![Digital Integrations page.](../image/digital-integrations.png "Digital Integrations page")

**Related topics**  


[View all digital integrations](../task/eaw-task/eaw-view-all-dig-integ.md)

[Add or edit a digital integration in the EA Workspace](../task/eaw-task/eaw-create-digital-integ.md)


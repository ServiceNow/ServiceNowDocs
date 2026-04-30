---
title: Digital interfaces in Enterprise Architecture Workspace
description: Manage all your digital interfaces from the Portfolio page of the Enterprise Architecture Workspace.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Working with an application portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Digital interfaces in Enterprise Architecture Workspace

Manage all your digital interfaces from the Portfolio page of the Enterprise Architecture Workspace.

Digital interfaces represent the logical contracts through which a business application or application service exposes functionality or data to other applications. A digital interface is modeled as a design‑time object to describe how other services or business applications can interact with the provider.

A single business application can expose multiple digital interfaces. Each interface represents a distinct API, service endpoint, or event stream and can define which information objects are provided or updated through that interaction.

The Digital Interfaces page displays a list of existing digital interfaces and their related information. You can access the Digital Interfaces page by navigating to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Portfolio** &gt; **Application Portfolio** &gt; **Digital Interfaces**.

## Digital Interfaces

![Digital Interfaces in Enterprise Architecture Workspace](../../image/eaw-image/eaw-digital-interfaces.png)

-   **[View all digital interfaces](../../task/eaw-task/eaw-view-all-dig-interfaces.md)**  
View the list of all your digital interfaces in the Enterprise Architecture Workspace.
-   **[Add or edit a digital interface in the EA Workspace](../../task/eaw-task/eaw-create-digital-interface.md)**  
Add or edit a digital interface for an integration to describe how business applications can interact.
-   **[Connect a digital interface with the CMDB API in the EA Workspace](../../task/eaw-task/eaw-relate-dig-interface-api.md)**  
Create a relationship between a digital interface and a CMDB API. The relationship helps you find out which digital integration uses which API, which APIs are built out of the design specs of the digital interface, and what environments are deployed. The relationship helps to group the deployed APIs.
-   **[Manage architectural artifacts of a digital interface in EA Workspace](../../task/eaw-task/eaw-manage-artifacts-digital-interface.md)**  
You can create new, add, or remove the architectural artifacts that are associated with a digital interface.
-   **[Relate an SDLC component to a digital interface](../../task/eaw-task/eaw-dig-interface-add-sdlc-comp.md)**  
Associate an SDLC component to a digital interface in the Enterprise Architecture Workspace. The SDLC components represent the artifacts or configurations that are used to implement an Interface.
-   **[Relate an information object to a digital interface](../../task/eaw-task/eaw-dig-interface-add-info-object.md)**  
Associate an information object to a digital interface in the Enterprise Architecture Workspace. You can also define how the information object should be consumed within the digital interface.
-   **[Relate credentials to a digital interface](../../task/eaw-task/eaw-dig-interface-add-credential.md)**  
Relate and manage integration user and account for a digital interface to track which user is assigned to which digital interface.

**Parent Topic:**[Working with an application portfolio](eaw-app-portfolio.md)

**Related topics**  


[View all digital interfaces](../../task/eaw-task/eaw-view-all-dig-interfaces.md)

[Add or edit a digital interface in the EA Workspace](../../task/eaw-task/eaw-create-digital-interface.md)


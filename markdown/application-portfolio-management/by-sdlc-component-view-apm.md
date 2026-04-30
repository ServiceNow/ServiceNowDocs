---
title: By SDLC Component view - Legacy
description: The By SDLC Component view displays the  SDLC Components Application Services Hardware Models and  Software Models  structure in a succession. Also, the business applications are shown with the same indentation level of application services in the Business Application section.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Multiple views in TPM - Legacy, Technology risks in timeline - Legacy, Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# By SDLC Component view - Legacy

The By SDLC Component view displays the  **SDLC Components** &gt; **Application Services** &gt; **Hardware Models** and  **Software Models ** structure in a succession. Also, the business applications are shown with the same indentation level of application services in the Business Application section.

With this view, you can view all the SDLC components along with the associated application services and business applications. You can also view the underlying software and hardware models that are associated to the application services. When you expand the software and hardware models, you can view their sources. The By SDLC Component view is available when ServiceNow® Common Service Data Model v4.0 is implemented.

The SDLC component is a configuration item that represents a unique code development effort. The purpose of the SDLC component is to represent the parts of a larger business application or digital product broken down into its individually developed components. An SDLC component is a software part or element of a larger whole for an application or technology.

There are two SDLC component types, Application and Infrastructure. Examples for type “Application” could be micro services and examples for type “Infrastructure” could be database configurations and security configurations. A deployed instance of an SDLC component of type “Application” would be an Application Service. A deployed instance of an SDLC component of type “Infrastructure” would be any infrastructure CI for which the SDLC component represents that snapshot of its configuration details.

A CMDB relationship between a business application, application service, and SDLC component can be created using the CI relationship \[cmdb\_rel\_ci\] table. To create a CMDB relationship with the compliance of CSDM v4.0, a relationship between an application service and an SDLC component and then between the SDLC component and the business application must be created.

The advantage of the By SDLC Component view is that you can directly view all the application services and business applications that are related to an SDLC component. For information on how to create a CMDB relationship, see [Relate business application to application service using CI relationship editor - Legacy](../task/relate-business-application-to-business-service.md).

**Note:** With this view, you can only view the application services that have at least one SDLC component associated.

With the By SDLC Component view, you can perform the following search:

Use the **Enter Search SDLC Component** field to enter the name and search an SDLC component from the list in the SDLC Component column.

**Parent Topic:**[Multiple views in TPM - Legacy](tpm-timeline-views.md)


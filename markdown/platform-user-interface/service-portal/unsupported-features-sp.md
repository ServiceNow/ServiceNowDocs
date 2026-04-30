---
title: Supported features in Service Portal
description: Service Portal is an alternative presentation layer for the platform. As such, not all features of the platform are extended to Service Portal. Consider your full application and the abilities of Service Portal before making considerable investments.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Supported features in Service Portal

Service Portal is an alternative presentation layer for the platform. As such, not all features of the platform are extended to Service Portal. Consider your full application and the abilities of Service Portal before making considerable investments.

## Not currently supported

Domain separation at Levels 1-3. However, Service Portal does include support for domain separation at the **Data only** level. For more information, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) and [Domain separation and Service Portal](../concept/domain-separation-service-portal.md).

## No plans to support

-   @ Mentions
-   Click-through/pop-ups
-   Embedded HTML outside of HTML fields
-   Embedded lists
-   UI macros
-   Formatters
-   UI actions marked as **Client**
-   Nested container Catalog variables
-   Survey wizards
-   [OpenFrame](https://www.servicenow.com/docs/access?context=c_OpenFrameOverview&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)

-   **[Service Catalog forms in Service Portal](../concept/sc-forms-in-sp.md)**  
Service Catalog forms are rendered within Service Portal widgets in a two-column layout. Complex forms may not display as expected.
-   **[Service Portal and client scripts](../concept/unsupported_client_scripts.md)**  
You can use client scripts and catalog client scripts in the Service Portal if the UI Type is set to **Mobile / Service Portal** or **All**. Client scripts and catalog client scripts are used with the Form widget and SC Catalog Item widget, as opposed to a widget client controller.
-   **[Antivirus Scanning in Service Portal](../concept/av-sp.md)**  
View the health status of file attachments in Service Portal. Antivirus Scanning scans files in the Attachments \[sys\_attachments\] table by default. When viewed from a Service Portal page, attachments may not be available for download depending on their health status.

**Parent Topic:**[Exploring Service Portal](../concept/exploring-service-portal.md)


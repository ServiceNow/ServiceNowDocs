---
title: Enterprise Model and Asset Classes release notes
description: Version history for the ITAM Enterprise and Asset Classes application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-enterprise-model-asset-classes.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Asset Management release notes, ServiceNow Store release notes]
---

# Enterprise Model and Asset Classes release notes

Version history for the ITAM Enterprise and Asset Classes application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.16.1 - May 2026**

    In this version, an issue has been resolved where the Activity log displayed only the new value of a field \(such as State\) after an update, without showing the previous value or the change history.

-   **Version 2.16.0 - March 2026**
    -   New tables added:
        -   CMDB Asset CI Model Interoperability Configuration, where asset/CI and product model interoperability is defined.
        -   CMDB Model Interoperability Type, which contains the list of interoperability types that can be selected when defining the relationships between assets/Cis and product models.
    -   Changed: The existing Model Compatibility table now includes an optional reference to the CMDB Model Interoperability Type.
    -   Fixed: Editing the Parent field on the Asset record is now restricted.
-   **Version 2.15.0 - December 2025**

    New: The Investigative service model is added to classify investigative cases by offense type, such as fraud, assault, or cybercrime, based on standardized taxonomies like the FBI’s NIBRS offense codes. This model is purpose-built for investigative case classifications. It aids in routing, reporting, and analytics, and supports both national standards and local agency needs.

-   **Version 2.14.0 - November 2025**
    -   What's New:
        -   1. Introduced new Multimedia production equipment model categories. These model categories improve visibility, tracking, and management of complex assets used by broadcasters, studios, and production houses.
        -   -   Multimedia Production Equipment
-   Media Control and Routing Equipment
-   Contribution Equipment
-   Audio Production Equipment
-   Video Production Equipment
-   Video Playout Equipment
-   Video Precision Monitor
-   Signal Processor and Amplifier
-   Broadcast Sync Generator
-   Teleprompter
-   Production Camera
-   Stage and Studio Lighting
        -   2. Created the new Multimedia Production Equipment Model \(sn\_ent\_mm\_prod\_equip\_model\) class and Multimedia Production Equipment Asset \(sn\_ent\_mm\_prod\_equip\_asset\) class.
-   **Version 1.0.1 - September 2022**

    App name was updated from Enterprise Model and Asset Classes to Expanded Model and Asset Classes

-   **Version 1.0.0 - August 2022**

    The Enterprise Model and Asset Classes app is the single source for all new, out-of-the-box, Enterprise model classes, asset classes, and model categories defined by ServiceNow. This app requires the installation of the Asset Management plugin \(com.snc.asset\_management\).


**Parent Topic:**[ServiceNow Store - IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itam-highlight.md)


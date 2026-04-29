---
title: Incident Management considerations
description: Consider these points while implementing the CSDM framework.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Applying CSDM guidelines to Incident Management, Configuring Incident Management, Incident Management, IT Service Management]
---

# Incident Management considerations

Consider these points while implementing the CSDM framework.

## Incident Management considerations

-   **Business applications are not referenced in Incident Management**

    Business applications are portfolio objects used for designing and planning your enterprise architecture. Business applications don't contain attribute-level details such as version, environment, and localization \(for any deployments using one or more applications\).

-   **Application service**

    An application service is an operational CI and a unique instance of an application.

    An application service is the logical representation of the underlying hardware and software CIs that work together to implement a business application or system. The application service represents an instance of the business application or system.

-   **Using application service on an Incident form**

    You can use the application service CI on the Incident form in scenarios like the following:

    -   The incident is for an application-related issue. On the Incident form, you can enter Application Service in the **Configuration Item** field to represent the application. For example, you can report the application service called MyApp 3.0 Production as unavailable.
    -   The incident is for an infrastructure CI that is affecting one or more services. On the Incident form, the **Impacted Services/CIs** related list identifies the application service affecting services. For example, the Server Acme42 CI might be identified as affecting the MyApp 3.0 Production and other related services.

**Parent Topic:**[Applying CSDM guidelines to Incident Management](itsm-incident-use-case-product-view.md)


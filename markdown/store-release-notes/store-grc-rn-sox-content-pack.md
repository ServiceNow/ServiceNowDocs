---
title: GRC: SOX content pack release notes
description: Version history for the GRC Sarbanes-Oxley \(SOX\) content pack on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-sox-content-pack.html
release: store
topic_type: reference
last_updated: "2023-05-04"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: SOX content pack release notes

Version history for the GRC Sarbanes-Oxley \(SOX\) content pack on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version - May 2023**

    Fixed: Reduction in size of the application jar file.

-   **Version 11.0.0 - October 2020**

    Changed: Enabled report\_view\_acl by default

-   **Version 10.1.0 - June 2020**

    Fixed: Fixed report\_view ACLs for sensitive platform tables

-   **Version 9.0.1 - November 2019**
    -   The Sarbanes-Oxley \(SOX\) Content Pack includes the following content elements:
        -   Pre-defined entity type and entities
        -   SOX policies
        -   Control objectives and controls
        -   SOX control attestation template
        -   Risk statements and risks
        -   Indicator templates and indicators
        -   SOX audit engagement
        -   Audit tasks
        -   Test templates and test plans
        -   Reports and dashboards
    -   The following relationships are also established:
        -   Control objectives to policies
        -   Controls to policies \(through control objectives\)
        -   Indicators to controls
        -   Risks to risk statements
        -   Risks to entities
        -   Risks to controls \(mitigating controls\)
        -   Test plans to controls for control testing
    -   Other GRC roles:
        -   Compliance Reader \(sn\_compliance\_reader\) can read **SOX Compliance Dashboard** and **SOX Processes**
        -   Compliance Manager \(sn\_compliance\_manager\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard** and edit **SOX Processes**
        -   Compliance Admin \(sn\_compliance\_admin\) can read **SOX Risk Dashboard** and edit **SOX Compliance Dashboard** and **SOX Processes**
        -   Risk Reader \(sn\_risk\_reader\) can read **SOX Risk Dashboard** and **SOX Processes**
        -   Risk Manager \(sn\_risk\_manager\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard,** and edit **SOX Processes**
        -   Risk Admin \(sn\_risk\_admin\) can read **SOX Compliance Dashboard** and edit **SOX Risk Dashboard** and **SOX Processes**
        -   Audit User \(sn\_audit\_user\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard**, and **SOX Processes**
        -   Audit Admin \(sn\_audit\_admin\) can read **SOX Compliance Dashboard**, **SOX Risk Dashboard**, and edit **SOX Audit Dashboard** and **SOX Processes**

**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)


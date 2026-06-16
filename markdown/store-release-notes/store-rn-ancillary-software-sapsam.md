---
title: SAP ABAP for Software Asset Management release notes
description: Version history for the SAP ABAP for Software Asset Management in ancillary software on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-ancillary-software-sapsam.html
release: store
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Ancillary software release notes, ServiceNow Store release notes]
---

# SAP ABAP for Software Asset Management release notes

Version history for the SAP ABAP for Software Asset Management in ancillary software on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.1.0 - August 2025**
    -   Support to optimize roles based on USMM optimizations
    -   Support for S/4HANA named user and engine licensing
    -   Support for self-declared engines
    -   Support for digital access using the passport tool \(supported in ECC and S/4HANA systems only\)
    -   Support for SAP HANA database licenses
-   **Version 6.0.1 - March 2025**
    -   Support to optimize roles based on USMM optimizations
    -   Support for S/4HANA named user and engine licensing
    -   Support for self-declared engines
    -   Support for digital access using the passport tool \(supported in ECC and S/4HANA systems only\)
-   **Version 5.0.2 - December 2024 \(Washington DC\)**
    -   New:
        -   Support to optimize roles based on USMM optimizations
        -   Support for S/4 HANA named user and engine licensing
        -   Support for self-declared engines
-   **Version 6.0.0 - August 2024 \(Xanadu\)**
    -   -   Support to optimize roles based on USMM optimizations
-   Support for S/4 HANA named user and engine licensing
-   Support for self-declared engines
-   Support for digital access
-   **Version 5.0.1 - June 2023**

    New:

    -   Support to optimize roles based on USMM optimizations.
    -   Support for S/4 HANA named user and engine licensing.
    -   Support for self-declared engines.
-   **Version 4.0.2 - March 2023**
    -   New:
        -   Support for S/4 HANA named user and engine licensing.
        -   Support for self declared engines.
-   **Version 5.0.0 - February 2023**
    -   New
        -   Support for S/4 HANA named user and engine licensing
        -   Support for self declared engines
-   **Version 4.0.1 - November 2022**
    -   New:
        -   Support for S/4 HANA named user and engine licensing
        -   Support for self declared engines
-   **Version 3.1.0 - August 2022**

    New: To help optimize user transaction activity, additional ABAP code has been added to fetch SAP transaction codes and user transaction codes from SAP clients. Compatibility with the ServiceNow Quebec release

-   **Version 4.0.0 - August 2021**
    -   New
        -   Support for S/4 HANA named user and engine licensing
        -   Support for self declared engines
-   **Version 2.1.0 - June 2021**
    -   New:
        -   Additional ABAP code has been added to fetch SAP engines and engine usage data from SAP clients for engine measurements
        -   Compatible with the ServiceNow Paris release
-   **Version 3.0.0 - December 2020**
    -   New
        -   Additional ABAP code has been added to fetch SAP user Tcode and User tcode from SAP clients for optimizing user transaction activity.
        -   Compatible with the ServiceNow Quebec release
-   **Version 2.0.0 - July 2020**
    -   New:
        -   Additional ABAP code has been added to fetch SAP engines and engine usage data from SAP clients for engine measurements
        -   Compatible with the ServiceNow Paris release
-   **Version 1.0.0 - June 2020**

    Steps to set up in the SAP system:

    1.  Compatible for Servicenow New York and Orlando release.
    2.  Activate the SAM SAP plugin \(com.sn\_samp\_sap\) in a ServiceNow instance.
    3.  Download SAP transport files into your SAP system. Check all the objects are activated.
    4.  Navigate to SOAMANAGER to set up web-service http connection for the service definition /NOW/SAMP.
    5.  For additional help, please follow "Deploy ABAP program for SAP" in supporting links and docs section.

        Note: Central SAP client \(in which our product files are imported\) will connect to other RFC SAP clients based on provided selection from /NOW/SAMP\_RFC transaction code.

-   **Version 0.0.1 - May 2020**

    Steps to set up in the SAP system:

    1.  Activate the SAM SAP plugin \(com.sn\_samp\_sap\) in a ServiceNow instance.
    2.  Download SAP transport files into your SAP system. Check all the objects are activated.
    3.  Navigate to SOAMANAGER to set up web-service http connection for the service definition /NOW/SAMP.
    4.  For additional help, please follow "SAP technical setup details" document from the provided attachments.

        Note: Indicating Central SAP will connect to other RFC clients once you choose from /NOW/SAMP\_RFC transaction code.


**Parent Topic:**[ServiceNow Store - Ancillary software release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-ancillary-software.md)


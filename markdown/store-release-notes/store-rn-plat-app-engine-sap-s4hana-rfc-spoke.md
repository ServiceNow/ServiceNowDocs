---
title: SAP S/4HANA RFC Spoke Dependencies release notes
description: Version history for SAP S/4HANA RFC Spoke Dependencies on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-sap-s4hana-rfc-spoke.html
release: store
topic_type: reference
last_updated: "2024-04-04"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# SAP S/4HANA RFC Spoke Dependencies release notes

Version history for SAP S/4HANA RFC Spoke Dependencies on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - April 2024**

    Added more actions for SAP S/4HANA RFC Spoke.

-   **Version 1.0.1 - September 2023**

    Fixed: Updated the SAP Transport Request files to allow the SAP S/4HANA Spoke v1.4 or beyond to integrate with SAP S/4HANA version EHP0 - EHP8.

-   **Version 1.0.0 - August 2023**
    -   This dependency file is built by Bristlecone Inc.
    -   To fully get advantage of the latest SAP S/4HANA RFC Spoke capabilities, customers will be required to import these dependency files into the SAP S/4HANA system before using the SAP S/4HANA RFC Spoke v1.4 or beyond. Simply follow the steps below:
        -   Download and unzip the attached zip file
        -   Import a Transport Request into SAP that involves ingesting:
            -   A CO file: K901358.S4H
            -   A Data file: R901358.S4H


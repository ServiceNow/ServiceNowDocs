---
title: Workplace Connectors release notes
description: Version history for the Workspace Service Delivery Workplace Connectors application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-connectors.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Connectors release notes

Version history for the Workspace Service Delivery Workplace Connectors application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.1 - June 2026**
    -   Fixed:
        -   Workplace Admins were not able to view metric values while creating a new provider connector configuration.
        -   Security fixes
-   **Version 2.2.5 - April 2026**

    Increasing version number to align with the releases.

-   **Version 2.2.4 - March 2026**

    Fixed: In some cases, events processing could fail for correctly mapped spaces.

-   **Version 2.2.1 - December 2025**
    -   Fixed:
        -   In some cases, a null-error was in the Metrikus occupancy API response.
        -   Data summarization was failing when campus is added as location in the Wi-Fi data table.
        -   Choice dependencies were not updated after upgrade.
        -   Improved support for translations in messages.
        -   Security fixes
-   **Version 2.1.0 - August 2025**
    -   Fixed:
        -   Performance improvements
        -   Security fixes
-   **Version 2.0.0 - May 2025**
    -   New:
        -   Added support for data summarization and roll-up for badging, occupancy, environmental, and Wi-Fi data.
        -   Adopted MetricBase \(a time-series database\) for efficient data storage and retrieval, enabling customers to create triggers and custom workflows.
    -   Fixed:
        -   Data handler handle method was failing when invoked via the webhook extension point.
        -   Added support for backward compatibility in Location Directory.
        -   Locations were shown as occupied based on old sensor readings in Location Directory.
        -   Translation fixes.
-   **Version 1.5.2 - February 2025**

    Fixed bug: Unable to post data via webhook with giving user credentials using postman.

-   **Version 1.5.1 - November 2024**
    -   New: Support for wifi data: Wifi data obtained from WAPs\(Wifi Access Points\) can now be pushed to WSD via the webhook.
    -   Fixed: Few minor bug fixes
-   **Version 1.4.0 - August 2024**
    -   New:
        -   Table to support environmental data \(Air Quality &amp; Temperature\)
        -   Table to store units for environmental data parameters
-   **Version 1.3.2 - May 2024**
    -   New:
        -   Support for Occupancy Sensor data
        -   New Providers table to store list of all hardware/sensor vendors
        -   New Provider Space Type Mapping table to store mapping between space types of WSD and hardware vendors
        -   New Provider Space Mapping table to store vendor unique ID for spaces on vendor application
        -   New Action Configuration table to store the flow actions
    -   Changed:
        -   Renamed a few tables - Provider Configuration to Provider Connector Configuration
        -   Fix script to extract the provider data from existing Provider Connector Configuration table to new Provider table
-   **Version 1.1.2 - February 2024**

    No significant updates.

-   **Version 1.1.0 - November 2023**
    -   New:
        -   Support to push badging data into WSD in near real time
        -   New webhook/Rest API using which badging events data can be sent to WSD
-   **Version 1.0.2 - August 2023**

    Workplace Connectors is a generic framework using which data from different kinds of workplace hardware/sensors \(such as badging systems, occupancy sensors etc.\) can be brought into WSD product via the respective spokes.


**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)


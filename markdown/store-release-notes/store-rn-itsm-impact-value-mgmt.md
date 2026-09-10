---
title: Impact Value Management - ITSM release notes
description: Version history for the Impact Value Management - ITSM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-impact-value-mgmt.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Service Management version history release notes, ServiceNow Store version history release notes]
---

# Impact Value Management - ITSM release notes

Version history for the Impact Value Management - ITSM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.1.0 - September 2026**

    Compatible: Zurich, Australia, Brazil

-   **Version 5.0.0 - August 2026**
    -   This release upgrades the Data Collection App for ITSM with an expanded set of value-measurement metrics.
    -   All existing metrics remain unchanged. No modifications have been made to current functionality. This release only adds net-new metrics that extend value-measurement capabilities across the supported products.
    -   For the complete list of new metrics, please refer to the Supporting Document.
    -   Enhanced Metrics:
        -   Any new metric introduced with this release is classified as an Enhanced Metric. Enhanced Metrics can be collected, and their data will be visible on the data dashboard included with the Data Collection App.
        -   Important: Automatic data transfer of Enhanced Metrics to ServiceNow's centralized Impact Delivery Instance is not supported.
        -   To make Enhanced Metric data available on the Impact Delivery Instance, customers must:
            -   Install the Impact In-Platform App, and
            -   Enable ServiceBridge.
        -   Both steps are mandatory for Enhanced Metric data to appear on the Impact Delivery Instance.
-   **Version 3.0.1 - December 2025**
    -   The ITSM Data Definition "Impact VM - ITSM - \# of Unplanned Outages This Month" &amp; "Impact VM - ITSM - Mean Time to Restore - Unplanned Outages \(hrs\)" in ITSM Performance Analytics Data Collection Apps was using an incorrect filter, which led to non-outage events \(such as service degradations\) being included in the calculation. The definition has now been updated to apply the correct outage criteria, ensuring that only valid outage events are counted. This fix improves the accuracy and reliability of the reported performance metrics.
    -   Compatible: Yokohama, Zurich
-   **Version 2.1.1 - August 2025**
    -   Experience the platform analytics dashboard, accessible via Platform Analytics \(PA\).
    -   Dashboards, designed to improve functionality similar to the previous performance analytics dashboard.
    -   Compatible: Xanadu, Yokohama, Zurich
-   **Version 2.1.0 - February 2025**
    -   Fixed: Metrics involving active user counts \(or other queries that rely on a change of state\) are now excluded from historical data collection for periods exceeding one month. This change ensures data accuracy, as such metrics cannot be reliably captured using point-in-time queries.
    -   Compatible: Washington DC, Xanadu, Yokohama
-   **Version 2.0.0 - December 2024**
    -   The Impact Value Management Data Collection Dashboard for IT Service Management \(ITSM\) gives Impact customers an automated solution for gathering standard ServiceNow value metrics, enhancing their value journey.
    -   Sharing Metrics with ServiceNow ServiceNow's integration gathers value metrics from customer instances on a monthly basis. Please note that integration with ServiceNow's centralized Impact instance is not available for Regulated customers \(Standalone and SSP\) and may necessitate granting user access for instances using the ServiceNow SNC security plugin. The Data Collection Apps will remain functional even if the integration with ServiceNow is unavailable; however, Metrics Data will need to be transferred manually in such cases.

**Parent Topic:**[ServiceNow Store - IT Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

